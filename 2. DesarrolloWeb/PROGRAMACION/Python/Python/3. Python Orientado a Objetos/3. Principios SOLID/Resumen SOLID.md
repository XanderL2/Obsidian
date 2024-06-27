
---
## Solid

- **SRP:** Una clase debe tener una razon, solo una razon para cambiar
- **OCP:** Una clase debe estar abierta para su extension pero cerrada para su modificacion.
- **LSP:** Nuestras clases derivadas deben conservar el comportamiento de las superclases solo extendiendo su funcionalidad.
- **ISP:** Las interfaces no deben depender de metodos que no utilizan, son preferibles las interfaces pequeñas a las grandes y genericas.
- **DIP:**  Es preferible depender de Interfaces o Clases abstractas que engloben todo (Abtstracciones generales) y no algo en especifico.

## Complementos:
- **Es preferible lanzar errores, ya que estos hacen mas verboso pero entendible el codigo, en vez de retornar falso o null en caso de errores.**
- **Es mejor manejar errores dentro de las funciones y en el except lanzar un error.**
- **Manejar errores específicos dentro de la función si tienen sentido en ese contexto**
- **Propaga errores que no puedas manejar adecuadamente dentro de la función hacia el nivel superior**.
- **Utiliza el bloque `finally` para asegurar que se liberen los recursos, como cerrar el socket**.
