---
[comment]: to build just run `docker run --rm -v $PWD:/home/marp/app/ -e MARP_USER="$(id -u):$(id -g)" -e LANG=$LANG marpteam/marp-cli *.md`
theme: default
_class: lead
paginate: true
backgroundColor: #F8F9E7
marp: true
---

<!--
footer: Repositório desta apresentação https://github.com/andreyev/docker-para-iniciantes
-->
![bg left:40% 80%](./images/docker-baby.png)

# **Imersão docker para iniciantes no LHC**

## Parte 1

<!--
header: Imersão docker para iniciantes no LHC
footer: Repositório desta apresentação https://github.com/andreyev/docker-para-iniciantes
-->

---

_Disclaimer_ #0:
- Uma GIA(ChatGPT-4) auxiliou a confecção desta apresentação e das imagens.
- As opiniões expressas neste documento são de responsabilidade exclusiva do autor e não refletem necessariamente as opiniões ou posições de quaisquer organizações, instituições ou entidades com as quais o autor esteja associado. As informações e visões apresentadas são de caráter pessoal e não devem ser interpretadas como uma representação oficial ou endosse de quaisquer organizações ou partes externas.

---

_Disclaimer_ #1:
> _TIMTOWTDI_

---

_Disclaimer_ #2:
>  docker ~ container

---

## Referências
* https://livro.descomplicandodocker.com.br/
* https://www.docker.com/play-with-docker/

---

## Agenda
* Conceitos
* Dockerfile
* Comandos
* Docker compose

---

## Conceitos
* Dockerfile + arquivos da aplicação
* Build
* Imagem
* Deploy
* Container

---

![bg 90%](https://livro.descomplicandodocker.com.br/media/image3.png)

---

### index.html

```
<h1>Olá, Docker!</h1>
<p>Minha primeira aplicação em um container.</p>
```

---

### Dockerfile

```
FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

EXPOSE 8080
```
---

![bg 70%](./images/layers.png)

---

# Comandos
## 1. Conhecendo o Docker

* `help`: `docker help`
* `info`: `docker info`
* `login`: `docker login`

---

# Comandos
## 2. Trabalhando com imagens

* `pull`: `docker pull nginx:alpine`
* `images`: `docker images`
* `build`: `docker build -t meu-site:1.0 .`
* `history`: `docker history nginx:alpine`
* `tag`: `docker tag meu-site:1.0 usuario/meu-site:1.0`
* `push`: `docker push usuario/meu-site:1.0`
* `manifest`: `docker manifest inspect nginx:alpine`

---

# Comandos
## 3. Criando e executando containers

* `run`: `docker run hello-world`
* `run`: `docker run -d --name web -p 8080:80 nginx:alpine`
* `ps`: `docker ps`
* `ps -a`: `docker ps -a`
* `port`: `docker port web`
* `logs`: `docker logs web`

---

# Comandos
## 3. Criando e executando containers
* `exec`: `docker exec -it web sh`
* `top`: `docker top web`
* `stats`: `docker stats web`
* `inspect`: `docker inspect web`
* `events`: `docker events`

---

# Comandos
## 4. Controlando o ciclo de vida

* `pause`: `docker pause web`
* `unpause`: `docker unpause web`
* `stop`: `docker stop web`
* `start`: `docker start web`
* `restart`: `docker restart web`
* `update`: `docker update --cpus 1 web`
* `rm`: `docker rm -f web`

---

# Comandos
## 5. Gerenciando recursos

* `container`: `docker container ls -a`
* `image`: `docker image ls`
* `network`: `docker network ls`
* `volume`: `docker volume ls`
* `plugin`: `docker plugin ls`
* `system`: `docker system df`

---

# Comandos
## 6. Limpando o ambiente

* `docker container prune`: Remove containers parados
* `docker image prune`: Remove imagens não utilizadas
* `docker volume prune`: Remove volumes não utilizados
* `docker network prune`: Remove redes não utilizadas
* `docker system prune`: Limpa recursos não utilizados

---

# docker compose

---

# docker swarm

---

<!-- _class: docker-return -->

# DOCKER WILL RETURN

<style>
section.docker-return {
  background: #000 !important;
  color: #fff !important;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

section.docker-return h1 {
  color: #fff !important;
  font-size: 64px;
  border: none;
}
</style>

---
<!--
footer: Repositório desta apresentação https://github.com/andreyev/docker-para-iniciantes
-->
![bg left:40% 80%](./images/docker-teen.png)

# **Imersão docker para iniciantes no LHC**

## Parte 2

---
Repositório desta apresentação https://github.com/andreyev/docker-para-iniciantes
![](https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://github.com/andreyev/docker-para-iniciantes)
<!--
header: Template de apresentação em MARP
footer: Repositório desta apresentação https://github.com/andreyev/docker-para-iniciantes
-->
