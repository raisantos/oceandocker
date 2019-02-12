# Introducão ao Docker

## Instalando Docker:
```

```

https://docs.docker.com/install/linux/docker-ce/ubuntu/

## Comandos basicos da Docker CLI:

```
docker build -t <nome_da_imagem>  <caminho para Dockerfile> <- Cria uma imagem a partir de um Dockerfile
docker images <- lista as imagens que existem no host
docker version <- Exibe as versões de client e server docker instaladas no host
docker info <- Descreve as informações sobre nosso host e nossa instalação do Docker
docker pull <- Baixa uma imagem de um repositório remoto
docker run <nome_da_imagem> --name <nome_do_container> <- Executa o container definido por aquela imagem
docker ps  <- Lista os containers em execução
docker ps -a <- Lista todos os containers do host
docker status <nome_do_container> <- Mostra informações do container em execução(ID,CPU,MEM,MEM USAGE...)
docker exec <- Executa comandos dentro do container
docker stop <nome_do_container> <- Para um container em execução
docker rm <nome_do_container> <- Remove um container do host
docker start <nome_do_container> <-continua a execução de um container parado
```

## Instrucoes para Dockerfile

```
FROM — Especifica uma imagem pai/origem.
LABEL — Adiciona metadados a imagem.
ENV — Configura uma variavel de ambiente dentro do container.
RUN — Executa um comando dentro do container
COPY — Copia arquivos para dentro do container
ADD — Adiciona/Copia arquivos para dentro do container(Aceita mais fontes de arquivos que o COPY)
CMD — Prove comandos e argumentos para a execucao/inicializacao do container
WORKDIR — Configura o diretorio de trabalho para as instrucoes seguintes
ARG — Define uma variavel para um argumento que pode ser passando para o Dockerfile durante o build
EXPOSE — Expoe uma porta
VOLUME — Cria um diretorio como ponto de montagem para a persistencia de dados
```