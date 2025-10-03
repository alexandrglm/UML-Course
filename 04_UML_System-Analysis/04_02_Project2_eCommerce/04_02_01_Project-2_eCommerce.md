# Project 2: eCommerce Application

## GOAL

Design a complete eCommerce platform using UML diagrams, focusing on complex HasMany and BelongsTo relationships. This project emphasises database normalisation and modelling behaviour that accounts for system failures and edge cases.

The eCommerce system has unique complexities different from social networks—primarily around nested parent-child relationships, inventory management, and payment processing workflows.

---

## REQUIREMENTS

### A. Activity Diagram (Behavioural)

**Purpose:** Model the complete user journey from arriving at the site through to completed purchase, with particular attention to what happens when things go wrong.

**Process to Model:** Full eCommerce flow (8-12 activities minimum)

**Required Activities:**

- Search
- View based on categories
- Viewing products
- Customising products (update quantity, style, etc.)
- Add to cart
- User registration
- View cart
- Update cart
- Checkout
- Payment

**Critical Requirement:** Include validation points throughout. Model what happens when:

- Credit card is declined
- Product is out of stock
- User abandons cart
- Payment processing fails

**Key Principle:** The complexity isn't in the "happy path" where everything works—it's in modelling all the potential failure points and alternative flows.

---

### B. Class Diagram (Structural)

**Purpose:** Design a robust, normalised database structure for an eCommerce system that can scale.

**Required Classes:**

1. User
2. Address
3. City
4. Country
5. Cart
6. CartItem
7. Inventory
8. InventoryItem
9. InventoryOption
10. Taxonomy (or Category)
11. Join table: Inventory ↔ Taxonomy relationship
12. Payment
13. CreditCard
14. PayPal
15. PaymentStatus
16. Order
17. OrderStatus
18. OrderItem

**Key Focus Areas:**

**Database Normalisation:**

- Why separate Address, City, Country into different tables?
- How to prevent data duplication
- Validation benefits of normalised structure

**Complex Relationships:**

- Order hasMany Products (via OrderItems)
- Product belongsTo Inventory
- Many-to-many between Inventory and Taxonomy
- One-to-many between User and Address (critical: many users can share same address)

**Parent-Child Nesting:**

- How does an Order contain multiple OrderItems?
- How does Inventory relate to InventoryOptions?
- The relationship chain: User → Order → OrderItem → Inventory

---

## A. ACTIVITY DIAGRAM

![]()

### Overview

This diagram models the complete shopping and checkout process, with multiple decision points that reflect real-world scenarios where users don't follow the perfect path.

### Starting Point

The user arrives at the application. From here, three immediate branches are possible:

1. Search for a product
2. Browse categories
3. View previously saved cart items

**Note:** A fourth option (selecting featured products on homepage) could be added, but the solution focuses on core functionality.

### Flow Breakdown

**Search Path:**

```
Search for product → Found? 
  └─ Yes → View product page
  └─ No → Browse categories → Select product → View product page
```

**Category Path:**

```
Browse categories → Select product → View product page
```

**Saved Items Path:**

```
View saved cart items → Directly to cart page
```

### Product Interaction

Once at the product page:

```
Set product parameters (size, quantity, colour, etc.)
  ↓
Add to cart
  ↓
Check: Is user registered?
  ├─ No → Registration page → View cart
  └─ Yes → View cart
```

**Design Decision:** Registration is required before proceeding to cart. This is a business logic choice—some sites allow guest checkout, but this model requires registration.

### Cart Management

```
View cart
  ↓
Is cart OK?
  ├─ No → Update cart → Checkout
  └─ Yes → Checkout
```

**What "cart OK" means:**

- Correct quantities
- All desired items present
- Prices acceptable
- No items removed due to stock issues

### Checkout Process

The checkout stage may occur on one page or multiple pages (depends on UX design):

```
Checkout: Enter shipping information
  ↓
Checkout: Enter billing information
  ↓
Checkout: Choose payment type
  ↓
Process payment
  ↓
Payment successful?
  ├─ Yes → Payment success page → END
  └─ No → Payment failure page
           ↓
           Try again?
           ├─ Yes → Return to "Choose payment type"
           └─ No → Update cart (remove items, try different products)
```

### Critical Decision Points

**1. Product Search Validation** If product not found, don't dead-end the user—redirect to categories.

**2. Registration Gate** User must be registered to proceed. This prevents abandoned carts from anonymous users and enables order tracking.

**3. Cart Validation** Give users opportunity to review and modify before committing to purchase.

**4. Payment Failure Handling** **Most Important:** When payment fails, users need two options:

- Retry with different payment method
- Go back and modify cart (perhaps remove expensive items)

Never leave users stranded at a failed payment screen with no clear path forward.

### Why This Matters

This activity diagram could take pages of written requirements to explain. With the visual diagram, a developer can immediately see:

- What pages need to be built
- What validation checks are required
- What error handling must be implemented
- Where users can loop back or exit the flow

Real-world application: This same pattern applies to any workflow with validation steps—expense approval systems, document review processes, multi-stage applications.

---

## B. CLASS DIAGRAM

### Overview

This is a larger, more complex class diagram than the Twitter project. The focus is on proper database normalisation and breaking tables into appropriate pieces for enterprise-level efficiency.

### Database Normalisation: The Address Example

**Why separate User, Address, City, Country?**

**The Problem with One Table:** If you store everything in the User table:

```
User
────────────
id
name
street
city
country
```

Issues:

1. No history of previous addresses
2. Cannot handle multiple shipping addresses
3. Typos in city/country names cause shipping failures
4. Data duplication (thousands of users in "London")

**The Solution: Normalised Structure**

```
User (1) ←→ (*) Address (*) ←→ (1) City (1) ←→ (1) Country
```

**Why many-to-many for User ↔ Address?**

Real-world scenario (using Amazon as example):

- User A lives at 123 Main St
- User A moves away
- User B moves into 123 Main St
- System should NOT say "address already taken"

Multiple users can legitimately share an address (families, roommates, office buildings). The system must accommodate this.

**Why separate City and Country tables?**

**Validation Benefits:**

- Prevent typos ("Lodnon" vs "London")
- Enable auto-complete functionality
- Zip code lookup can auto-populate city/country
- Shipments don't get returned due to address errors

**Data Integrity:** City and Country become **controlled vocabularies**. Users select from a list rather than free-form typing, dramatically reducing errors.

### Taxonomy: Abstract Classes and Inheritance

**The Setup:**

```
        Taxonomy (abstract)
              |
        ┌─────┴─────┐
        |           |
    Category       Tag
```

**What is Taxonomy?**

An **abstract class** that provides foundational rules for child classes but is never instantiated directly.

**Taxonomy attributes:**

- `id`
- `name`
- `description`

These are common to all children. You will never create a "Taxonomy" object—only Category and Tag objects.

**Category Example:**

- "South American Coffee Blends"
- "Organic Products"
- "Fair Trade"

Used for primary product organisation.

**Tag Example:**

- "Over 1 pound"
- "Under £10"
- "New Arrivals"

Used for secondary filtering and sorting.

**Why separate them?**

Both are taxonomies at a high level, but they serve different purposes and have different attributes. Category might have `left` and `right` values for nested set model. Tag might have `weight` for sorting priority.

**Visibility: Protected Attributes**

```
Tag
────────────
# weight
# calculateWeight()
```

The `#` symbol means **protected**:

- Tag class can access these
- Any class inheriting from Tag can access these
- External systems and objects CANNOT access these
- Different from `+` (public) and `-` (private)

### The Payment Architecture: Interface Pattern

**The Challenge:**

Users need two payment options:

1. Credit card (via Stripe/Authorize.Net)
2. PayPal

These are fundamentally different integrations with different APIs and different error handling.

**The Solution: Interface Pattern**

```
        Payment (interface)
              |
        ┌─────┴─────┐
        |           |
   CreditCard    PayPal
```

**Payment Interface Attributes:**

- `payment_type`
- `total`
- `order_id`
- `status`

**Why CreditCard and PayPal don't inherit from Payment:**

CreditCard is not a **type** of payment—it's a **payment source**. Same with PayPal. They **implement** the Payment interface rather than inherit from it.

**Benefits of This Architecture:**

**Separation of Concerns:**

- CreditCard class handles Stripe/Authorize.Net API
- PayPal class handles PayPal API
- They never interfere with each other

**Scalability:**

- Want to add Apple Pay? Create new class implementing Payment interface
- Want to add cryptocurrency? Same pattern
- Existing code doesn't break

**Maintainability:** If you merged both into one Payment module with if/else logic:

```
if payment_type == 'credit_card'
  # Stripe logic here
elsif payment_type == 'paypal'
  # PayPal logic here
end
```

This becomes unmaintainable quickly. Any change risks breaking both payment methods.

**The Separate Class Approach:**

```
class CreditCard implements Payment
  # All Stripe/Authorize.Net logic isolated here
end

class PayPal implements Payment
  # All PayPal logic isolated here
end
```

Changes to one don't affect the other. This is **loose coupling**—the goal of good architecture.

### PaymentStatus: Mission-Critical Security

**Why a separate class?**

```
PaymentStatus
─────────────
id
status
timestamp
order_id
```

**Financial Transaction Security:**

You must track payment status meticulously. Holes in your system could allow:

- Declined cards still receiving shipments
- Double-charging users
- Orders shipping without payment confirmation

**The Status Workflow:**

```
pending → processing → completed
                     → failed → retry
                              → cancelled
```

Every state change must be logged. Every transition must be validated. This class wraps all that critical functionality in one auditable place.

### Parts and MaintenanceParts: Scalability Example

**The Question:** Why separate `Part` and `MaintenancePart`?

**The Short-term View:** Technically, you could connect `Part` directly to `ServiceList`. It would work.

**The Long-term Problem:** Coffee shop does well. Expands services. Now needs to track:

- Maintenance parts (current system)
- Inventory parts (for sale to customers)
- Wholesale parts (for B2B clients)

If `MaintenancePart` is your only option, you'd have to:

1. Create `InventoryPart`
2. Create `WholesalePart`
3. Refactor all existing code

**The Scalable Solution:**

```
Part (generic)
  └─ MaintenancePart (specific)
  └─ InventoryPart (future)
  └─ WholesalePart (future)
```

Separation now prevents massive refactoring later.

**Key Principle:** In enterprise applications, assume success and plan for growth. Structure your database so adding features doesn't require rebuilding foundations.

---

## KEY TAKEAWAYS

### Activity Diagram

**Model Failures, Not Just Success:**

- Happy path is easy
- Complexity is in error handling
- Users don't follow perfect flows
- System must handle edge cases gracefully

**Decision Points Define Complexity:**

- More branches = more complex system
- Each decision requires validation logic
- Map out ALL possible user paths

### Class Diagram

**Database Normalisation Matters:**

- Prevent data duplication
- Enable data validation
- Support multiple relationships (addresses)
- Plan for scale from day one

**Separation of Concerns:**

- Payment interface pattern
- Keep different functionalities isolated
- Loose coupling enables maintainability

**Think Long-term:**

- Structure for growth
- Don't paint yourself into architectural corners
- Small decisions now have big impacts later

### Universal Principles

**Break Systems into Smallest Pieces:** The more granular your design, the easier implementation becomes. Each class diagram element translates to a specific database table and model. Each activity becomes a specific validation check.

**Visual Communication:** These diagrams replace dozens of pages of written requirements. A developer can look at them and immediately understand what needs to be built.

**Start High-Level, Then Detail:** Activity diagram first (understand behaviour), then class diagram (implement structure). Never jump straight to code.
