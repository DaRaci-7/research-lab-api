# **Alumno: Eduardo Andres Lizama Delgado  Cohorte: 22**

# 1. Diferencia entre HTTP y HTTPS


### ---SIGNIFICADOS---
### -HTTP:  Protocolo de Transferencia de Hipertexto (Hypertext Transfer Protocol)
### -HTTPS: Protocolo de Transferencia de Hipertexto Seguro (Hypertext Transfer Protocol Secure)

## ***Investiga cómo funciona el cifrado SSL/TLS en HTTPS.***

### "El cifrado SSL/TLS en HTTPS funciona mediante un proceso de "handshake" (saludo) que autentica al servidor y establece una conexión segura. Luego, utiliza una combinación de cifrado asimétrico (una clave pública para cifrar y una clave privada para descifrar) durante el saludo y cifrado simétrico (una clave de sesión secreta y temporal) para la transmisión de datos posteriores. Esto asegura que los datos transmitidos sean privados (cifrados) y que no hayan sido manipulados (integridad)." 

## ***¿Por qué HTTPS es más seguro?***

### Basicamente porque usa el cifrado de datos y un protocolo que verifica que la comunicacion entre nuestro dispositivo y el servidor es segura gracias a las llaves simetricas y asimetricas.

<!-- ## Muestra un ejemplo visual (puede ser una captura del candado del navegador).-->

<p align="center">
  <img src="ejemplohttps.png" width="450" style="border-radius:25px" />
</p>


## ***¿Qué sucede si un sitio no usa HTTPS?***

### "Si un sitio no usa HTTPS, los datos de los usuarios se transmiten sin cifrar, lo que los hace vulnerables a la interceptación por parte de atacantes, especialmente en redes Wi-Fi públicas." 
### Todo esto quiere decir que al no usar HTTPS nos encontramos vulnerables sufrir un robo de informacion, ya que no tenemos ninguna barrera de seguridad frente a posibles ataques de ciberdelincuentes.


# 2. Puertos de comunicación

## ***Explica qué es un puerto en redes y por qué es importante para HTTP.***

### Los puertos vendrian siendo las entradas o salidas(virtuales) por donde se va a comunicar nuestro pc. Son importantes para http porque nos ayudan a identificar con que tipo de aplicacion nos estamos comunicando, permiten la comunicacion con el servidor, sin puertos no podriamos enviar ni recibir datos y por ultimo facilita que se realicen multiples servicios a la vez porque cada uno usa su propio puerto de comunicacion de manera simultanea (por ejemplo, el puerto 25 para SMTP o el puerto 443 para HTTPS).

## ***Investiga el propósito de los puertos 80 y 8080, y qué tipo de tráfico suelen manejar.***

### Puerto 80
### Propósito: Es el puerto predeterminado para el protocolo HTTP. Se utiliza para la comunicación web no cifrada entre navegadores y servidores web.

### Puerto 8080

### Propósito: Funciona como un puerto HTTP alternativo. Es muy común en entornos de desarrollo local para probar sitios web antes de publicarlos.


### Ambos puertos manejan tráfico HTTP, pero el puerto 80 es el más habitual para la navegación web estándar.


## ***Menciona otros puertos conocidos (por ejemplo: 21, 22, 443, 3306) y su función.***

### Puerto 25 (SMTP): Se utiliza para el Protocolo Simple de Transferencia de Correo, principalmente para enviar correos electrónicos de un servidor a otro.
### Puerto 53 (DNS): El Sistema de Nombres de Dominio lo usa para convertir nombres de dominio como google.com en direcciones IP que las computadoras pueden entender.
### Puerto 110 (POP3): El Protocolo de Oficina de Correos versión 3 se usa para recuperar correos electrónicos de un servidor.
### Puerto 143 (IMAP): El Protocolo de Acceso a Mensajes de Internet se utiliza para acceder a correos electrónicos en un servidor remoto.
### Puerto 3389 (RDP): El Protocolo de Escritorio Remoto permite la conexión a un equipo a través de un escritorio remoto. 

## ***Ejemplo: ¿Qué puerto utiliza HTTPS por defecto?***

### HTTPS utiliza por defecto el puerto 443. Este es el puerto estándar para conexiones seguras en la web

# 3. Códigos de estado de respuesta HTTP

## ***Investiga qué son los status codes y para qué sirven.***

### Los status codes son mensajes de tres cifras que un servidor web envía a un cliente (como tu navegador) para indicar el resultado de una solicitud, informando si fue exitosa, si hubo un error o si se necesita alguna otra acción. 

## ***Crea una tabla organizada por categoría:***

### 1: Informativo (1XX)

| Código de estado | Función | 
|:----------:|:----------:|
| 100    | Continúa en   | 
| 101    | Protocolos de conmutación   | 
| 102    | Procesando  | 
| 103    | Primeras pistas   | 

### 2: Éxito (2XX)

| Código de estado | Descripción               |
|:----------:|:----------:|
| 200     | OK                        |
| 201     | Creado                    |
| 202     | Aceptado                  |
| 203     | Información no autorizada |
| 204     | Sin contenido             |
| 205     | Restablecer contenido     |
| 206     | Contenido parcial         |
| 207     | Multiestado               |
| 208     | Ya comunicado             |
| 226     | IM Utilizado              |

### 3: Redirección (3XX)

| Código de estado | Función | 
|:----------:|:----------:|
| 300     | Varias opciones             |
| 301     | Movido permanentemente      |
| 302     | Encontrado                  |
| 303     | Ver otros                   |
| 304     | No modificado               |
| 307     | Redireccionamiento temporal |
| 308     | Redireccionamiento permanente |


### 4: Error de cliente (4XX)

| Código de estado | Función | 
|:----------:|:----------:|
| 400     | Bad request                                                      |
| 401     | No autorizado                                                    |
| 402     | Pago requerido                                                   |
| 403     | Prohibido                                                        |
| 404     | No se ha encontrado                                              |
| 405     | Método no permitido                                              |
| 406     | No aceptable                                                     |
| 407     | Se requiere autenticación proxy                                  |
| 408     | Tiempo de espera de la solicitud                                 |
| 409     | Conflicto                                                        |
| 410     | Gone                                                             |
| 411     | Longitud requerida                                               |
| 412     | Condición previa fallida                                         |
| 413     | Contenido demasiado grande                                       |
| 414     | URI demasiado largo                                              |
| 415     | Tipo de soporte no compatible                                    |
| 416     | Alcance no satisfactorio                                         |
| 417     | Expectativa fallida                                              |
| 421     | Petición mal dirigida                                            |
| 422     | Contenido no procesable                                          |
| 423     | Bloqueado                                                        |
| 424     | Dependencia fallida                                              |
| 425     | Demasiado pronto                                                 |
| 426     | Actualización necesaria                                          |
| 428     | Condición previa requerida                                       |
| 429     | Demasiadas peticiones                                            |
| 431     | Los campos de la cabecera de la solicitud son demasiado grandes  |
| 451     | No disponible por motivos legales                                |


### 5: Error del servidor (5XX)

| Código de estado | Función | 
|:----------:|:----------:|
| 500     | Error interno del servidor               |
| 501     | No aplicado                              |
| 502     | Bad gateway                              |
| 503     | Servicio no disponible                   |
| 504     | Tiempo de espera de la puerta de enlace  |
| 505     | Versión HTTP no admitida                 |
| 506     | Variante también negociada               |
| 507     | Almacenamiento insuficiente              |
| 508     | Bucle detectado                          |
| 511     | Autenticación de red necesaria           |


## - Luego, profundiza **por qué debemos conocer y reconocer especialmente estos tres códigos:**
    - `200 OK` → cuando todo sale bien.
    - `404 Not Found` → cuando el recurso no existe o fue movido.
    - `500 Internal Server Error` → cuando el problema está en el servidor.

> 💬 Explica con tus palabras cómo podrías usar estos códigos para diagnosticar errores en una API o en un proyecto web.
>
### La importancia de conocer bien estos codigos es que nos entregan informacion basica que debemos manejar si estamos trabajando en la reparacion de una pg web, si obtenemos un codigo 200 como respuesta todo esta funcionando correctamente por lo que en teoria no deberiamos modificar nada, si obtenemos el codigo 404 podemos pensar primero que la url esta mal escrita, en caso de que este bien escrita podemos pensar que no hay nada en el servidor y que eliminaron la pg y por eso no obtenemos una respuesta, finalmente si obtenemos el codigo 500 significa que el servidor podria estar caido.
