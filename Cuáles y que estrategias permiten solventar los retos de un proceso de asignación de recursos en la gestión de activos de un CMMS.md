
Existe una entidad proveedor la cual está asociada con una entidad pieza. El sistema puede tener el plazo de entrega, número de pieza del fabricante, precio unitario y
cantidad de reorden de cada proveedor. Las ordenes de compra debe emitirse automáticamente.

CMMS necesita una pieza específica para la producción, como una válvula.

- Fabricante A la llama "VALV-100".
- Proveedor B la tiene registrada como "PV-B123".
- Tu empresa la maneja internamente como "PZ-001".

Todos estos números hacen referencia a la misma válvula, pero cada parte involucrada (fabricante, proveedor y CMMS) tiene su propia forma de identificarla.

Existen distintos tipos de informes que permiten gestionar y analizar el inventario desde múltiples perspectivas, como la ubicación, uso, costos, transacciones, obsolescencia, y asignaciones a órdenes de trabajo (WO)

Se debe generar una solicitud que debe ser aprobada antes de que se genere la orden de compra

El proceso es:
1. Generar orden de requisición(por pieza)
2. Se convierte en una solicitud de compra(Se compone de varias ordenes de requisición) de artículos
3. Alguien aprueba la solicitud de compra
4. Se convierte en una PO


## Generación normal de una orden de compra

```plantuml 

Sistema --> Sistema : Genera orden de requisición
Sistema --> "Jefe de mantenimiento" : Genera solicitud de compra
"Jefe de mantenimiento" --> Sistema : Aprueba orden de compra
Sistema --> Proveedor : Genera orden de compra
```

## Generación de una cotización
```plantuml 

Sistema --> Sistema : Genera orden de requisición
Sistema --> "Jefe de mantenimiento" : Genera solicitud de compra
"Jefe de mantenimiento" --> Proveedor : Solicita cotización
Proveedor --> "Jefe de mantenimiento" : Envía cotización
"Jefe de mantenimiento"  --> Sistema  : Aprueba orden de compra
Sistema --> Proveedor : Genera orden de compra
```



