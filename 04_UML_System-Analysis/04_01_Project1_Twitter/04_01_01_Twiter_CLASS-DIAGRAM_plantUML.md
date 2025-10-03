@startuml Project 1: Twitter - CLASS DIAGRAM

!theme plain
skinparam classAttributeIconSize 0
skinparam classFontSize 25

folder "uc PROJECT 1 - TWITTER" {
    class User {

        - userId: int
        - username: string
        - email: string
        - password: string
        - displayName: string
        - bio: string
        - profileImageUrl: string
        - createdAt: DateTime
        - isVerified: bool
        - followersCount: int
        - followingCount: int
        
        + createTweet(content: string): Tweet
        + followUser(user: User): void
        + unfollowUser(user: User): void
        + likeTweet(tweet: Tweet): void
        + retweetTweet(tweet: Tweet): void
        + getUserId(): int
        + getUsername(): string
        + setUsername(username: string): void
        + getEmail(): string
        + setEmail(email: string): void
    }

    class Tweet {

        - tweetId: int
        - content: string
        - authorId: int
        - createdAt: DateTime
        - likesCount: int
        - retweetsCount: int
        - repliesCount: int
        - isRetweet: bool
        - originalTweetId: int
        - hasMedia: bool
        
        + addReply(content: string, author: User): Reply
        + addLike(user: User): void
        + removeLike(user: User): void
        + addRetweet(user: User): Retweet
        + addHashtag(hashtag: Hashtag): void
        + getAuthor(): User
        + getTweetId(): int
        + getContent(): string
        + getLikesCount(): int
        + getRetweetsCount(): int
    }

    class Reply {

        - replyId: int
        - content: string
        - authorId: int
        - originalTweetId: int
        - createdAt: DateTime
        - likesCount: int
        - repliesCount: int
        - parentReplyId: int
        
        + addLike(user: User): void
        + addReply(content: string, author: User): Reply
        + getOriginalTweet(): Tweet
        + getAuthor(): User
        + getReplyId(): int
        + getContent(): string
    }

    class Hashtag {

        - hashtagId: int
        - name: string
        - createdAt: DateTime
        - usageCount: int
        - isBlocked: bool
        
        + incrementUsage(): void
        + getTweets(): List<Tweet>
        + getTrendingScore(): int
        + block(): void
        + unblock(): void
        + getName(): string
        + getUsageCount(): int
    }

    class Like {

        - likeId: int
        - userId: int
        - tweetId: int
        - createdAt: DateTime
        
        + getUser(): User
        + getTweet(): Tweet
        + remove(): void
        + getLikeId(): int
    }

    class Retweet {

        - retweetId: int
        - userId: int
        - originalTweetId: int
        - createdAt: DateTime
        - comment: string
        - isQuoteTweet: bool
        
        + getUser(): User
        + getOriginalTweet(): Tweet
        + addComment(comment: string): void
        + remove(): void
        + getRetweetId(): int
        + getComment(): string
    }

    class Message {

        - messageId: int
        - senderId: int
        - receiverId: int
        - content: string
        - createdAt: DateTime
        - isRead: bool
        - hasMedia: bool
        - isDeleted: bool
        
        + markAsRead(): void
        + getSender(): User
        + getReceiver(): User
        + delete(): void
        + addMedia(image: Image): void
        + getMessageId(): int
        + getContent(): string
        + isReadMessage(): bool
    }

    class Security {

        - securityId: int
        - userId: int
        - passwordHash: string
        - salt: string
        - lastLogin: DateTime
        - failedLoginAttempts: int
        - isAccountLocked: bool
        - twoFactorEnabled: bool
        - recoveryEmail: string
        - sessionToken: string
        
        + validatePassword(password: string): bool
        + lockAccount(): void
        + unlockAccount(): void
        + resetFailedAttempts(): void
        + generateSessionToken(): string
        + enableTwoFactor(): void
        + sendRecoveryEmail(): void
        + getSecurityId(): int
        + isLocked(): bool
    }

    class Location {

        - locationId: int
        - latitude: double
        - longitude: double
        - city: string
        - country: string
        - placeName: string
        - isPublic: bool
        - createdAt: DateTime
        
        + getCoordinates(): string
        + getDistance(otherLocation: Location): double
        + setPublic(isPublic: bool): void
        + getFullAddress(): string
        + getLocationId(): int
        + getCity(): string
        + getCountry(): string
    }

    class Image {

        - imageId: int
        - fileName: string
        - fileUrl: string
        - fileSize: int
        - mimeType: string
        - width: int
        - height: int
        - altText: string
        - uploadedAt: DateTime
        - uploadedBy: int
        
        + resize(width: int, height: int): Image
        + compress(): void
        + getUploader(): User
        + setAltText(text: string): void
        + delete(): void
        + getImageId(): int
        + getFileUrl(): string
        + getFileSize(): int
    }

    ' Relaciones principales
    User ||--o{ Tweet : "Crea"
    User ||--o{ Reply : "Crea"
    User ||--o{ Message : "Envía"
    User ||--o{ Message : "Recibe"
    User ||--|| Security : "Tiene"
    User ||--o| Location : "Está localizado en"
    User ||--o| Image : "Tiene de Foto de Perfil"

    Tweet ||--o{ Reply : "Tiene"
    Tweet ||--o{ Like : "Recibe"
    Tweet ||--o{ Retweet : "Es de Retweet"
    Tweet ||--o| Location : "Escrito en"
    Tweet ||--o{ Image : "Contiene"

    ' Relaciones many-to-many
    User }|--|| Like : "Da"
    Tweet }|--|| Like : "Recibe"
    User }|--|| Retweet : "Hace"
    Tweet }|--|| Retweet : "Es de Retweet"
    Tweet }|--|{ Hashtag : "Contiene"

    ' Relaciones de seguimiento
    User ||--o{ User : "Sigue a"

    ' Relaciones con mensajes e imágenes
    Message ||--o{ Image : "Contiene"

    ' Relación jerárquica de replies
    Reply ||--o{ Reply : "Respuesta de"
}


@enduml
