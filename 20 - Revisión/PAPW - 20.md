<!-- $theme: default -->

PAPW
===

##### Alberto Benavides
###### Ago - Dic 2018

<!-- footer: Universidad Autónoma de Nuevo León | Facultad de Ciencias Físico Matemáticas | Multimedia y Animación Digital -->

---

# 20. Revisión segundo parcial

---

### 1. ¿Qué imprime en consola el siguiente programa escrito en `Java`?
```
public class Main {
  public static void main(String[] args) {
    String cadena = "reconocer";
    int longitud = cadena.length();
    for (int i = 0; i < longitud; i++) {
      if(i % 2 == 0){
        System.out.print(cadena[i]);
      }
    }
  }
}

// rcncr
```

---

### 2. Declara una instancia de la clase `Ejemplo` a la que le asignes tu primer apellido como valor para el atributo `s` y tu matrícula como valor para `i`.
```java
public class Ejemplo{
  public String s;
  private int i;
  
  public void setI(int i){
    this.i = i;
  }
}

Ejemplo e = new Ejemplo();
e.s = "Benavides";
e.setI(1373079);
```
---

### 3. Inicializa una instancia de la clase `Alumno` cuyo atributo `nombre` sea igual a tu primer nombre y `puntos` igual a la calificación que esperas obtener en este examen.

```java
public class Alumno{
  private String nombre;
  private float puntos;

  public Alumno(float puntos, String nombre){
    this.nombre = nombre;
    this.puntos = puntos;
  }
}

Alumno yo = new Alumno(100, "Alberto");
```

---

### 4. Completa los incisos el siguiente código `MySQL` para crear una tabla de usuario que permita registrar el nombre de usuario, correo electrónico, contraseña y un identificador como su llave primaria.

```sql
create table usuario(
  idUsuario /* int */ not null auto_increment, 
  nombreUsuario /* varchar */(50),
  correo /* varchar */ (50) unique,
  claveAcceso binary(20),
  primary key(/* idUsuario */)
);
```
---

### 5. Completa los códigos `MySQL` para poder:
a) Insertar un registro:
```sql
/* insert into */ 'usuario' // [...]
```

b) Editar el registro con `idUsuario = 1`:
```sql
update usuario set nombre = 'Al' /* where */ idUsuario = 1;
```

c) Seleccionar solamente el nombre de usuario y correo de todos los usuarios:
```sql
/* select nombreUsuario, correo */ from usuario;
```
---

### 6. Completa correctamente los incisos de este modelo de usuario en `Java` y cuida que además coincidan con la convención establecida.
```java
public class User {
  /* private */ Integer age;
  
  /* public */ void setAge(Integer age) {
        /* this */.age = age;
    }
  /* public */ Integer getAge() {
      /* return */ age;
  }
```

---

### 7. Menciona la diferencia entre las etiquetas `@GetMapping('example')` y `@PostMapping('setExample')`, usadas generalmente en un controlador de aplicación web de `Java`.

La primera recibe peticiones `GET` solicitadas a la `URL` `example` y la segunda recibe peticiones `POST` solicitadas a la `URL` `setExample`.