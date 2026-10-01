Gianluca rodrigues malachias
RA: da0b237f24936d20055e
Executei uma pagina web em um container docker chamado treinamento. Usei a imagem nginx:alpine e a porta 8083 do ambiente.
saida docker ps: root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS          PORTS                                     NAMES
aa1dd9a19f43   nginx:alpine   "/docker-entrypoint.…"   About a minute ago   Up 59 seconds   0.0.0.0:8083->80/tcp, [::]:8083->80/tcp   treinamento

resposta comando curl localhost:  curl http://localhost:8083
!DOCTYPE html
html lang="pt-BR"
head<meta charset="UTF-8"
title Treinamento/title
/head
body
h1 Treinamento/title
/head
body
h1 Treinamento ativo/h1
/body
html

RESPOSTAS;
Respostas
Qual a diferença entre nginx:alpine e o contêiner comunicado?
nginx:alpine é a imagem, ou seja, o modelo usado para criar o contêiner. Já comunicado é o contêiner em execução, criado a partir dessa imagem e contendo a página index.html que foi copiada para ele.

O que significa o mapeamento 8090:80?
Significa que a porta 8090 do ambiente/servidor está ligada à porta 80 dentro do contêiner, onde o Nginx está atendendo as requisições. Assim, ao acessar http://localhost:8090, a requisição chega ao Nginx na porta 80 do contêiner.
