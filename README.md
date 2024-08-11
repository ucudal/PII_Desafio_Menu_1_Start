<img alt="UCU" src="https://www.ucu.edu.uy/plantillas/images/logo_ucu.svg"
width="150"/>

# Universidad Católica del Uruguay

## Facultad de Ingeniería y Tecnologías

### Programación II

# Desafío menú #1: Restaurante simple

## Objetivo

Implementar en C# las clases indicadas a continuación, con sus responsabilidades
y colaboraciones también indicadas a continuación. Cada clase debe ser agregada
por un estudiante diferente y deben trabajar en ramas diferentes.

## Pasos

1. Uno de los estudiantes del equipo crea un repositorio privado a partir de
este repositorio plantilla haciendo clic en el botón `Use this template` y luego
en el comando `Create new repository`.

2. El estudiante que creó el repositorio agrega a los demás integrantes del
equipo haciendo clic en `Settings`, `Collaborators and Teams`, `Add people` para
cada uno de los miembros del equipo, usando sus nombres de usuario.

3. Todos clonan el repositorio creado a sus equipos.

4. Todos crean una rama con el nombre que quieran, la única condición es que
deben ser diferentes para cada miembro del equipo.

5. Distribuyan las siguientes clases entre los miembros del equipo. Cada miembro
implementa una clase diferente.

6. El código no va a funcionar hasta que integren el trabajo en la rama `main`,
por lo que deberán unir los cambios con frecuencia.

> [!IMPORTANT]
> Para compilar el código en Rider usen el comando `Build Solution` del menú
> `Build`.
>
> Aunque todavía no vamos a ver cómo hacer casos de prueba, este repositorio usa
> casos de prueba para comprobar la implementación. Para ejecutar los casos de
> prueba ejecuten el comando `Run All Tests from Solution` en el menú `Tests` de
> Rider. Deberían ver una imagen como la siguiente si todo funcionó bien:
> <img src="/assets/image.png" alt="Resultado de las pruebas" width="345" />

## Clases a implementar

A continuación la descripción de las clases, sus responsabilidades de hacer y de
conocer, y sus colaboraciones.

## 1. **Clase `Dish`**

Representa un platillo individual en el menú del restaurante.

* Responsabilidades de conocer:
  * **Name**: Conoce el nombre del platillo.
  * **Price**: Conoce el precio del platillo.
  * **IsVegetarian**: Conoce si el platillo es vegetariano o no.

* No tiene responsabilidades de hacer.

> [!IMPORTANT]
> Debe ser posible crear una instancia de `Dish` e inicializar sus propiedades
> en una sola operación.

Aquí está el código provisto de la clase [`Dish`](./src/Dish.cs).

## 2. **Clase `Menu`**

Representa el conjunto de platillos disponibles en el restaurante.

* Responsabilidades de conocer:
  * `dishes`: Conoce la lista de platillos disponibles en el restaurante;
    esta responsabilidad está ya implementada con la variable de instancia
    `dishes` en el código provisto.

* Responsabilidades de hacer
  * `AddDish(Dish)`: Agrega un platillo a la lista de platillos del menú.
  * `RemoveDish(Dish)`: Elimina un platillo de la lista del menú
    basado en su nombre.
  * `Dish GetDishByName(string)`: Busca y devuelve un platillo específico del
    menú basado en su nombre; retorna `null` si no encuentra en platillo.

> [!TIP]
> Puedes acceder al i-ésimo elemento de la variable de instancia `dishes` con
> `dishes[i]` y las estructuras de repetición condicional que consideres
> apropiadas. También puedes recorrer los platillos en esa variable de instancia
> con la estructura repetitiva condicional `foreach`.

Aquí está el código provisto de la clase [`Menu`](./src/Menu.cs).

## 3. **Clase [`Table`](./src/Table.cs)**

Representa una mesa en el restaurante.

* Responsabilidades de conocer:
  * `Number`: Conoce el número identificador de la mesa.
  * `IsOccupied`: Conoce si la mesa está ocupada o no.
  * `Order`**`: Conoce la lista de platillos que han sido pedidos en la mesa;
    esta responsabilidad está ya implementada con la variable de instancia
    `order` en el código provisto.

* Responsabilidades de hacer:
  * `Occupy()`: Marca la mesa como ocupada.
  * `Free()`: Libera la mesa y vacía la lista de pedidos.
  * `AddOrder(Dish)`: Agrega un platillo a la lista de pedidos.
  * `bool HasOrders()`: Returna `true` si la mesa tiene pedidos y `false` en
    caso contrario.

> [!TIP]
> El método `Clear()` de la clase `ArrayList` vacía la lista.

> [!IMPORTANT]
> Debe ser posible crear una instancia de `Table` e inicializar sus propiedades
> en una sola operación.

Aquí está el código provisto de la clase [`Table`](./src/Table.cs).

## 4. **Clase `Waiter`**

Representa un mozo en el restaurante, encargado de atender mesas.

* Responsabilidades de conocer:
  * `Name`: Conoce el nombre del mozo.
  * `assignedTables`: Conoce las mesas asignadas al mozo; esta responsabilidad
    está ya implementada con la variable de instancia `assignedTables` en el
    código provisto.

* Responsabilidades de hacer:
  * `AssignTable(Table)`: Asigna una mesa al camarero.
  * `TakeOrder(Table, Dish)`: Toma un pedido para una mesa específica
    y agrega el platillo a la orden de esa mesa.

> [!IMPORTANT]
> Debe ser posible crear una instancia de `Waiter` e inicializar sus propiedades
> en una sola operación.

Aquí está el código provisto de la clase [`Waiter`](./src/Waiter.cs).
