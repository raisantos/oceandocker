# Introducão ao Docker

## Exemplo Vue.js para producao (Build em duas etapas)

Pode ser compilado com o comando: `docker build -t vue-example-prod .`

E o container pode ser lancado como mostrado a seguir: `docker run -it -p 8080:8080 --rm --name vue-prod vue-example-prod`