| Guía       | Título                                                                                        |
| ---------- | --------------------------------------------------------------------------------------------- |
| **06-164** | **Visión General de Elementos del Diagrama de Clases**                                        |
| 06-165     | Asociaciones, Multiplicidad y Navegabilidad en Diagramas de Clases UML (y Roles)              |
| 06-166     | Ejemplo: Construir Twitter Usando Diagramas de Clases **(Personalización UML para Claridad)** |

---
# 06-164: Fundamentos del Diagrama de Clases 
---


## ***1. Visión General***
---
Los diagramas de clases son los diagramas estructurales más populares en UML.   

Proporcionan un plano para tu sistema orientado a objetos mostrando la estructura estática de las clases y sus elementos básicos.



## ***2. Estructura/Elementos del Diagrama de Clases***
---
Cada diagrama de clases consiste en **TRES secciones principales**:

![large](./06-164_IMG1.png)

---

### 1. ***Sección de Nombre***

### Propósito

- Identifica la clase
- Debe ser un **sustantivo** representando la entidad
- Sigue la convención **PascalCase**

### Mejores Prácticas

- Usar nombres descriptivos y significativos
- Evitar abreviaciones a menos que sean universalmente entendidas
- Mantenerlo conciso pero claro

### Ejemplos

```
Usuario
CuentaBancaria
CarritoCompras
ServicioEmail
```

---

### 2. ***Sección de Atributos***

Los atributos representan los **datos** o **propiedades** que los objetos de esta clase contendrán.

### Componentes Requeridos

Cada atributo debe incluir **tres elementos**:

1. **Visibilidad**
2. **Nombre**
3. **Tipo de Datos**

### Símbolos de Visibilidad

|Símbolo|Visibilidad|Significado|
|---|---|---|
|`+`|Público|Accesible desde cualquier lugar|
|`#`|Protegido|Accesible dentro de la clase y subclases|
|`-`|Privado|Accesible solo dentro de la clase|

### Formato de Sintaxis

```
[visibilidad][nombre]: [tipoDatos]
```

### Ejemplos

```
+ primerNombre: String
+ apellido: String
+ edad: Integer
- saldoCuenta: Double
# idUsuario: Long
```

### Ejemplo de Clase del Mundo Real

![large](./class-map.png)
---

## 3. Sección de Operaciones

Las operaciones representan el **comportamiento**, los **métodos** que la clase puede realizar.

### Características

- Siempre seguidas por **paréntesis** `()`
- Usan **símbolos de visibilidad** (los mismos que los atributos)
- Representan lo que la clase **puede hacer**

### Reglas de Visibilidad

- `+` (Público): Puede ser llamado desde **fuera** de la clase
- `-` (Privado): Puede **solo** ser llamado desde **dentro** de la clase
- `#` (Protegido): Puede ser llamado desde la clase y **subclases**

### Formato de Sintaxis

```
[visibilidad]   [nombreMetodo](): [tipoRetorno]
```

### Ejemplos

```
+ depositar(): void
+ retirar(): boolean
+ obtenerSaldo(): Double
- validarCuenta(): boolean
# generarReporte(): String
```


---


## 3. Mapeo de Lenguajes de Programación***
---
### Ejemplo JavaScript/TypeScript

```typescript
class CuentaBancaria {

    public numeroCuenta: string;
    public nombreTitular: string;
    private saldo: number;
    protected tipoCuenta: string;
    
    public depositar(): void { }
    public retirar(): boolean { }
    public obtenerSaldo(): number { }
    private validarCuenta(): boolean { }
    protected generarReporte(): string { }
}
```

### Ejemplo Python

```python
class CuentaBancaria:
    
    def __init__(self):
        self.numero_cuenta = ""     # público
        self.nombre_titular = ""    # público
        self.__saldo = 0.0          # privado
        self._tipo_cuenta = ""      # protegido
    
    
    def depositar(self):            # público
        pass
    
    def retirar(self):              # público
        pass
    
    def obtener_saldo(self):        # público
        pass
    
    
    def __validar_cuenta(self):     # privado
        pass
    
    def _generar_reporte(self):     # protegido
        pass
```

---


## ***4. Tipos de Datos Comunes***
---
### Tipos Primitivos

- `String` - Cadenas, caracteres, texto.
- `Integer` - Números enteros
- `Double/Float` - Números decimales
- `Boolean` - Valores verdadero/falso
- `Date` - Valores de fecha/hora

### Tipos de Objeto

- Nombres de clases personalizadas (ej., `Usuario`, `Direccion`)
- Colecciones (ej., `List<String>`, `Array<Integer>`)

---

## ***5. Plantilla de Referencia Rápida***
---
```
┌─────────────────────────┐
│       NombreClase       │  ← Sustantivo en PascalCase
├─────────────────────────┤
│ + attr1: Tipo           │  ← Atributo público
│ # attr2: Tipo           │  ← Atributo protegido  
│ - attr3: Tipo           │  ← Atributo privado
├─────────────────────────┤
│ + metodo1(): TipoRetorno│  ← Método público
│ # metodo2(): TipoRetorno│  ← Método protegido
│ - metodo3(): TipoRetorno│  ← Método privado
└─────────────────────────┘
```

---
