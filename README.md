Se probó la imagen de la base de datos MongoDB y se ejecuto el contenedor en Docker. 
Imagen: cristian-mongo:202010495

## 1. Construcción d ela imagen personalizada

Se creó un Dockerfile basado en la imagen oficial de MongoDB:

```dockerfile
FROM mongo:4.4
```
Después con el tag personalizado:

***docker build -t cristian-mongo:202010495***
<img width="739" height="70" alt="image" src="https://github.com/user-attachments/assets/ca6d7487-1c58-4340-b008-6bc40c51e1b3" />

Hice un volumen para persistir datos

***docker volume create mongo-data***

 y ejecuté el contenedor

 ***docker run -d --name mongodb \ -p 27017:27017 \ -v mongo-data:/data/db \ cristian-mongo:202010495***

 <img width="1595" height="305" alt="image" src="https://github.com/user-attachments/assets/8c77c61e-e9a1-4563-8c92-764bd214a5c1" />

Luego se revisan los logs (Pruebas en los archivos .txt) y se verifica que aparezca "waiting for connections"

Luego debido a que se usó una versión de mongo "antigua" se utilizo el cliente de mongo dentro del contenedor para probar el ping al servidor de la BD.

<img width="837" height="264" alt="image" src="https://github.com/user-attachments/assets/29aca9e2-0f09-4f40-be70-c153951a8284" />

Con eso ya se podían insertar y hacer consulta al documento json de la base de datos nosql.

Foto de la carpeta:
<img width="878" height="545" alt="image" src="https://github.com/user-attachments/assets/2ea82b84-9cf7-48cb-a772-80098f26d85b" />

***Cristian Andrés Basto Largo - 202010495***. 
