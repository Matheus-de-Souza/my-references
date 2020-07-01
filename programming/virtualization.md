# Virtualization References

[Go Back](./)

## Docker

### Containers

* Ver containers ativos - `docker ps`
* Ver containers ativos e parados - `docker ps -a`
* Remover container - `docker rm ID_CONTAINER`
* Remover todos container não-ativos - `docker container prune`
* Para saber quais portas tal container usa -  `docker port id_container`
* Rodar container com porta mapeada, com nome e no modo _detached_ - `docker run -d NOME_IMAGEM -p 12345:8080 --name meu-site`
* Rodar/Parar container  - `docker start/stop ID_CONTAINER`
* Rodar container com terminal _attached_- `docker start -a -i ID_CONTAINER`
* Rodar container com variável de ambiente setada - `docker run -e AUTHOR="Fulano" dockersamples/static-site`
* Inspecionar valores do container - `docker inspect ID_CONTAINER`

### Imagens

* Rodar imagem e conectar o terminal nela - `docker run -it NOME_IMAGEM`
* Remover imagem - `docker rmi NOME_DA_IMAGEM`
* Para listar as imagens no sistema - `docker images`
* Para buildar uma imagem - `docker build -f node.dockerfile -t mwssouza/node .`
* Para entrar na conta do DockerHub - `docker login`
* Enviar imagem para DockerHub - `docker push NOME_IMAGEM_LOCAL`
* Baixar imagem do DockerHub - `docker pull NOME_IMAGEM_LOCAL`

### Volumes

* Rodar container com volume (bind mount) setado - `docker run -v "CAMINHO_VOLUME_LOCAL:CAMINHO_VOLUME_CONTAINER" NOME_IMAGEM`
* Rodar container com volume só no container - `docker run -v CAMINHO_VOLUME_CONTAINER NOME_IMAGEM`
* Rodar container com volume nomeado - `docker run -v NOME_VOLUME:CAMINHO_VOLUME_CONTAINER NOME_IMAGEM`
* Criar volume nomeado - `docker volume create NOME_VOLUME`
* Rodar container com volume tmpfs - `docker run --tmpfs CAMINHO_VOLUME_CONTAINER NOME_IMAGEM`

## Network

* Criar uma nova rede - `docker network create --driver bridge NOME_REDE`
* Listar redes docker - `docker network list`
* Inspecionar rede docker - `docker network inspect NOME_REDE`
* Rodar container em certa rede - `docker run -it --name meu-container --network NOME_REDE ubuntu`
* Identificar o próprio ip - `hostname -i`

### Docker Compose

* Fazer build dos serviços descritos no docker-compose.yml - `docker-compose build`
* Subir containers descritos no docker-compose.yml - `docker-compose up`
* Parar containers descritos no docker-compose.yml - `docker-compose down`
* Reiniciar containers descritos no docker-compose.yml - `docker-compose restart`
