# Comandos Docker - Professor Lucas

## Comandos Básicos

- `docker --version`: Verifica a versão do Docker instalada.
- `docker info`: Mostra informações detalhadas sobre o Docker, como número de containers e imagens.
- `docker pull <image_name>`: Baixa uma imagem do Docker Hub.
- `docker images`: Lista todas as imagens locais disponíveis.
- `docker run <image_name>`: Executa um container baseado em uma imagem.
- `docker ps`: Lista todos os containers em execução.
- `docker ps -a`: Lista todos os containers, incluindo os parados.
- `docker stop <container_id>`: Para um container em execução.
- `docker start <container_id>`: Inicia um container parado.
- `docker restart <container_id>`: Reinicia um container.
- `docker rm <container_id>`: Remove um container parado.
- `docker rmi <image_name>`: Remove uma imagem local.

## Comandos Intermediários

- `docker exec -it <container_id> <command>`: Executa um comando dentro de um container em execução.
- `docker logs <container_id>`: Mostra os logs de um container.
- `docker inspect <container_id>`: Detalha um container: IP, volume e configurações de rede.
- `docker commit <container_id> <new_image_name>`: Cria uma nova imagem a partir de um container modificado.
- `docker tag <image_id> <new_repo:tag>`: Marca uma imagem com um novo nome e tag.
- `docker build -t <image_name> .`: Constrói uma nova imagem a partir de um `Dockerfile`
- `docker volume ls`: Lista volumes Docker criados.
- `docker volume rm <volume_name>`: Remove um volume não utilizado.
- `docker network ls`: Lista as redes Docker configuradas.
- `docker network create <network_name>`: Cria uma nova rede Docker.
- `docker network connect <network_name> <container_id>`: Conecta um container a uma rede existente.

## Comandos Avançados

- `docker-compose up`: Inicia containers configurados no arquivo `docker-compose.yml`.
- `docker-compose down`: Para e remove todos os containers definidos no `docker-compose.yml`.
- `docker-compose build`: Constrói imagens definidas no `docker-compose.yml`.
- `docker-compose logs`: Mostra os logs de todos os containers gerenciados pelo Docker Compose.
- `docker system df`: Mostra o uso de disco pelo Docker, incluindo imagens, containers e volumes.
- `docker system prune`: Limpa imagens, containers, redes e volumes não utilizados.
- `docker save -o <file.tar> <image_name>`: Salva uma imagem como um arquivo `.tar`.
- `docker load -i <file.tar>`: Carrega uma imagem de um arquivo `.tar`.
- `docker export -o <file.tar> <container_id>`: Exporta o sistema de arquivos de um container como um `.tar`.
- `docker import <file.tar>`: Cria uma imagem a partir de um arquivo `.tar`.
- `docker checkpoint create <container_id> <checkpoint_name>`: Cria um ponto de verificação (checkpoint) de um container em execução.
- `docker stack deploy -c <compose-file> <stack_name>`: Faz deploy de um grupo de serviços usando Docker Swarm.
- `docker stack rm <stack_name>`: Remove um stack criado com o Docker Swarm.
- `docker service create --name <service_name> <image>`: Cria um serviço no modo Swarm.
- `docker service scale <service_name>=<num_replicas>`: Escala um serviço para o número desejado de réplicas no Swarm.
