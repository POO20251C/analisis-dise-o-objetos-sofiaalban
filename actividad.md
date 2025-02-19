# Actividad
## Sofia Albán
### Caso 4

#### 4. Caso Tienda de Música

Estás desarrollando una aplicación para gestionar una tienda de música. La tienda maneja información sobre álbumes, clientes y compras.

La tienda tiene un amplio catálogo de álbumes, cada uno con un título único, un código de identificación y una fecha de lanzamiento. Los clientes son personas registradas en la tienda con un número de identificación único y una fecha de registro.

Para gestionar las compras, es necesario registrar cada compra, incluyendo el álbum comprado, el cliente que realiza la compra y la fecha de la compra. Además, debe ser posible registrar cuando un álbum es devuelto, actualizando así el estado de la compra.

Los clientes pueden comprar varios álbumes a lo largo del tiempo. Sin embargo, una compra específica siempre corresponde a un solo álbum comprado por un solo cliente en una fecha específica.


#### Desarrollo del problema

1. Álbum
   -Atributos:
     - codigoIdentificación: String
     - titulo: String
     - fechaLanzamiento: String
     + mostrarDetalles():
     + actualizarTitulo()

2. Cliente
   - Atributos:  
     - idCliente: String
     - nombre: String
     - fechaRegistro:  
   - Métodos
     + mostrarHistorialCompras()
     +actualizarDatos()

3. Compra  
   - Atributos:
     - idCompra: String
     - cliente:
     - album:  
     - fechaCompra:
     - devuelto: Booleano
   - Métodos:
     + devolución()  
     + mostrarDetallesCompra()  

#### diagrama UML

``` mermeid
classDiagram
    class Cliente {
        - idCliente: String
        - nombre: String
        - fechaRegistro: Date
        + mostrarHistorialCompras(): void
        + actualizarDatos(): void
    }

    class Album {
        - codigoIdentificación: String
        - titulo: String
        - fechaLanzamiento: Date
        + mostrarDetalles(): void
        + actualizarTitulo(): void
    }

    class Compra {
        - idCompra: String
        - fechaCompra: Date
        - devuelto: Boolean
        + devolución(): void
        + mostrarDetallesCompra(): void
    }

    Cliente "1" --> "N" Compra : realiza
    Album "1" --> "N" Compra : pertenece
```

LINK : https://www.mermaidchart.com/app/projects/d1d98bc9-8b56-42f9-ad47-b4b1a7a45c4d/diagrams/50cc84a2-881c-4968-b671-539513eaafc3/version/v0.1/edit 