
Uno de los estudiantes del equipo crea un repositorio privado a partir de este
repositorio plantilla haciendo clic en el botón `Use this template` y luego en
el comando `Create new repository`.

El estudiante que creó el repositorio agrega a los demás integrantes del equipo
haciendo clic en `Settings`, `Collaborators and Teams`, `Add people` para cada
uno de los miembros del equipo, usando sus nombres de usuario.

Todos clonan el repositorio creado a sus equipos.

Todos crean una rama con el nombre que quieran, la única condición es que deben
ser diferentes para cada miembro del equipo.

Distribuyan las siguientes clases entre los miembros del equipo. Cada miembro
implementa una clase diferente.

El código no va a funcionar hasta que integren el trabajo en la rama `main`, por
lo que deberán unir los cambios con frecuencia.

A continuación la descripción de las clases, sus responsabilidades de hacer y de
conocer, y sus colaboraciones.

## 1. **Clase [`Dish`](./src/Dish.cs)**

Representa un platillo individual en el menú del restaurante.

* Responsabilidades de conocer:
  * **Name**: Conoce el nombre del platillo.
  * **Price**: Conoce el precio del platillo.
  * **IsVegetarian**: Conoce si el platillo es vegetariano o no.

* No tiene responsabilidades de hacer.

## 2. **Clase [`Menu`](./src/Menu.cs)**

Representa el conjunto de platillos Dish disponibles en el restaurante.

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
> apropiada. También puedes recorrer los platillos en esa variable de instancia
> con la estructura repetitiva condicional `foreach`.

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

## 4. **Clase [`Waiter`](./src/Waiter.cs)**

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
