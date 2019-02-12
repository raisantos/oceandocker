# Introducão ao Docker

## Exemplo Vue.js simples

Pode ser compilado com o comando: `docker build -t vue-example .`

E o container pode ser lancado como mostrado a seguir: `docker run -it -p 8080:8080 --rm --name vue vue-example`