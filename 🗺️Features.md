# Gestión de ordenes de compra

COMO jefe de mantenimiento DESEO gestionar ordenes de compra PARA coordinar la adquisión de activos

## Escenario:

DADO que existen activos que han superado el punto de reorden 
Y proveedores
Y ordenes de requisición generadas por el sistema 
Y ordenes de compra generadas por el sistema 
Y ordenes de compra enviadas al jefe de mantenimiento
CUANDO el jefe de mantenimiento apruebe las ordenes de compra 
ENTONCES el sistema enviará las ordenes de compra al proveedor 

## Escenario:

DADO que existen activos que han superado el punto de reorden 
Y proveedores
Y ordenes de requisición generadas por el sistema 
Y ordenes de compra generadas por el sistema 
Y ordenes de compra enviadas al jefe de mantenimiento
Y el jefe de mantenimiento solicite cotizaciones
y el jefe de mantenimiento recibe cotizaciones
CUANDO  el jefe de mantenimiento apruebe una cotización
ENTONCES el sistema enviará las ordenes de compra al proveedor 