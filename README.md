# Reto 3 Eli-Caro - Caso del restaurante
Durante la sesión número 8 de programación orientada a objetos se trato el tema de composición y se comparo con la herencia de clases, este reto propusó el modulado una situación de restaurante, haciendo uso de herencia y composición de clase, este repositorio tiene la finalidad de organizar mi código utilizando digramas UML.

# Creacion de la clase MenuItem
```mermaid
classDiagram

class MenuItem {
    name : str
    price : float

    total_price (self, quantity : int = 1)
}
```
# Relación de herenncia entre MenuItem - Beverage, Maincourse y Appetizer
```mermaid
classDiagram

Beverage --|> MenuItem
Maincourse --|> MenuItem
Appetizer --|> MenuItem

class MenuItem {
    name : str
    price : float

    total_price (self, quantity : int = 1)
}

class Beverage {
    size : str
    super ().__init__ (self, name: str, price: float)
}

class Maincourse {
    super ().__init__ (self, name: str, price: float)
}

class Appetizer {
    super ().__init__ (self, name: str, price: float)
}
```

# Creación de la clase order
```mermaid
classDiagram

class Order {
    Bill_items : list
    
    add_menuitems_to_bill (self, item: MenuItem)
    bill (self, discount: bool = False, discount_percentage : int = 0)
}
```
