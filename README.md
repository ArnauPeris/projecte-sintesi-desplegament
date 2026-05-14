# Projecte de Síntesi – Desplegament d’Aplicacions Web (DAW)

[![Status](https://img.shields.io/badge/status-actiu-success)]()
[![Module](https://img.shields.io/badge/module-Desplegament%20d'Aplicacions%20Web-blue)]()
[![Level](https://img.shields.io/badge/level-2n%20DAW-orange)]()
[![Optional](https://img.shields.io/badge/CI/CD-opcional-lightgrey)]()


Projecte acadèmic del mòdul de Desplegament d’Aplicacions Web (DAW) centrat en convertir una aplicació React en un projecte més proper a un entorn professional.

L’objectiu principal no era crear una aplicació complexa, sinó treballar aspectes reals de:

- Git i treball amb branques
- Simulació d’un workflow col·laboratiu
- Resolució de conflictes
- Dockerització
- Reproduïbilitat del projecte
- Documentació

## Autor

**Arnau González Peris**

Maig 2026

## Requisits previs

Cal tenir instal·lat:

- Git
- Docker
- Docker Compose


## Instal·lació i execució

1. Clonar el repositori

`git clone https://github.com/ArnauPeris/projecte-sintesi-desplegament.git`

2. Entrar al projecte

`cd projecte-sintesi-desplegament`

3. Construir i iniciar Docker

`docker compose up --build`

4. Obrir al navegador
  
`http://localhost:8080`




## Tecnologies utilitzades

- React
- Vite
- Docker
- Docker Compose
- Nginx
- Git + GitHub

## Descripció del projecte

El projecte parteix d’una plantilla React + Vite molt simple.

L’aplicació mostra:

- Una pantalla inicial amb logos de React i Vite
- Informació bàsica de documentació
- Un botó contador interactiu

No existeix backend ni base de dades perquè el focus del projecte és el desplegament i no la lògica de negoci.



## Workflow Git utilitzat

S’ha simulat un entorn col·laboratiu amb diferents tipus de branques:

| Tipus         | Exemple                        | Objectiu             |
| ------------- | ------------------------------ | -------------------- |
| main          | `main`                         | branca estable       |
| feature       | `feat/downgrade-react`         | noves funcionalitats |
| fix           | `fix/traduccio-catala`         | correccions          |
| dockeritzacio | `dockeritzacio/docker-setup`   | configuració Docker  |
| documentacio  | `documentacio/report`          | documentació         |




## Estratègia de merge

S’ha utilitzat `git merge` en lloc de rebase per conservar:

- historial complet
- commits originals
- evidència dels conflictes
- merges explícits

Per tal de facilitar la documentació i seguiment dels canvis.



## Dockerització

L’aplicació s’executa amb Docker utilitzant:

- Node.js per generar el build
- Nginx per servir el frontend  

### Docker compose

El projecte utilitza un únic servei: `react-app`

### Variables d’entorn

- APP_NAME=projecte-sintesi-react

- APP_ENV=production

### Persistència

S’ha afegit persistència per als logs de Nginx:

```
volumes:
  - nginx_logs:/var/log/nginx
```
Això permet mantenir els logs encara que el contenidor es destrueixi.



## Aprenentatges

Aquest projecte ha servit per entendre millor:

- com treballa Git internament
- com apareixen conflictes reals
- la importància de comunicar-se en equip
- el funcionament bàsic de Docker
- la diferència entre “funciona localment” i “és desplegable”



## Filosofia del projecte


> **"It works on my machine"**  
> és desenvolupament.
>
> **"It is ready to deploy"**  
> és enginyeria.

---