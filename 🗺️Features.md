
 
```gherkin
# language: es

Característica: Generación de ordenes de compra 
  
  Como Jefe de mantenimiento
  Quiero que se generen ordenes de compra  
  Para agilizar el flujo de adquisición de activos
  
  Escenario: Generación de ordenes de compra periodicas
    Dado que hay almenos tres órdenes de compra que incluyen los mismos activos y los mismos proveedores
    Cuando el jefe de mantenimiento aprueba la plantilla de orden de compra
    Entonces el sistema debe enviar la orden de compra a los proveedores 
    
  Escenario: Generación de ordenes de compra manuales a partir de cotizaciones
    Dado que existen múltiples cotizaciones para una orden de compra con el formato:
	    |activo|cantidad|precio|
	    |activo1|10|10$|
	    3
    Cuando el jefe de mantenimiento aprueba la cotización
    Entonces el sistema debe generar y aprobar la orden de compra y enviar a los    proveedores 


Característica: Asignar activos requeridos por orden de trabajo 
  
  Como Jefe de mantenimiento
  Quiero que se asignen activos para ordenes de trabajo para 
  Para agilizar el flujo de aprobación de órdenes de compra
  
  Escenario: Selección automática de proveedores de confianza
    Dado que existe una lista de proveedores de confianza en el sistema
    Y se genera una nueva orden de requisición
    Cuando el proveedor asignado a la orden está en la lista de proveedores de confianza
    Entonces el sistema debe aprobar automáticamente la orden de compra para su envío


Característica: Levantamiento de activos móvil

  Como técnico de mantenimiento
  Quiero registrar activos de los clientes mediante un dispositivo móvil,
  Para (sin importar el lugar de la conexión) 
  Escenario: Registro de activos con conexión
    Dado que existe un técnico mantenimiento técnico
    Y el técnico tiene acceso a internet
    Cuando el técnico ingresa un nuevo activo del cliente
    Entonces el sistema debe guardar el activo de manera inmediata

  Escenario: Registro de activos sin conexión
    Dado el técnico está en la pantalla de registro de activos
    Y el técnico no tiene acceso a internet
    Cuando el técnico ingresa un nuevo activo del cliente
    Entonces el sistema debe almacenar los datos del activo de manera local en el dispositivo del técnico
    Y cuando la conexión se restablece, el sistema debe sincronizar los activos registrados de manera offline con la base de datos central en la nube
```
