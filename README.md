***********************************************************************************
# Docker Documentaçao:
https://docs.docker.com/desktop/dashboard/
# Repositorios de imagens oficiais:
https://hub.docker.com/ 
# Imagens instaladas no computador: (Containers)
docker image ls
# Saber quais container docks estão rodando:
docher ps
# Saber quais container docks estão instalados e ocupando memória:
docker ps -a
# baixar a imagem oficial:
docker pull ubuntu/apache2:2.4-22.04_beta
# Levantar servidor de aplicação:
docker ningx
docker run -d -p 80:80 --name nginx-docker nginx
docker run ubuntu/apache2:2.4-22.04_beta
docker run -d ubuntu/apache2:2.4-22.04_beta
# Parar o container
docker stop 'id'
# Entrar no terminal do container
docker exec -it id /bin/sh
# Ver logs da aplicação
docker logs nginx-docker
# Excluir os containers:
docker rm 'id / ou name'
 *** Criar nossas proprias imagens: ***
 # Inicializar um projeto em node:
 npm init -y
 # Instalar express "framework para servir uma rota"
npm install express
# Arquivo pra executar a aplicação
index.js
# Excluir as instalações para usarmos no container onde serão instalados
- Pastas: node_modules e arquivo package-lock.json
# Buildar a imagem
docker build .
# Listar todas as imagens criadas no sistema
docker image ls
# Pega o id e rodar um container com base nessa imagem
docker run -p 3000:3000 -d 'id'
# Consulta que estará online
http://localhost:3000
# Para atualizar a imagem, deve-se parar o container (stop)
Altera-se o arquivo Dockfile e buildar novamente.
# Para nomear uma imagem no comando de buildar
docker build -t nome-image-node .
# Levantando o container pelo nome e também dando um nome a esse container
docker run -p 3000:3000 -d --name container-node nome-image-node
# Remover tudo que não está sendo utilizado:
docker system prune
# Docker daemon | docker client
daemon = processo rodando (Automático para o linux)
client = executável para comunicação no daemon
