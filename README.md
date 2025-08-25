Imagen: \'$TAG\'
Contenedor: \'mongodb\'
- \'docker build -t $TAG .\'
- \'docker volume create mongo-data\'
- \'docker run -d --name mongodb -p 27017_27017 -v mongo-data:/data/db $TAG\'
- imagen_tag.txt
- docker_ps.txt
- logs.txt
- ping.txt
- query.txt
