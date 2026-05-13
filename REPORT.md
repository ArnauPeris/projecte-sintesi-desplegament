# REPORT – Projecte de Síntesi

## 1. Dades generals

Nom del projecte: projecte-sintesi-desplegament

Integrants: Arnau Gonzalez

Tecnologia principal (Laravel / React / Fullstack): React

Enllaç al repositori: https://github.com/ArnauPeris/projecte-sintesi-desplegament

Data d’entrega: maig 2026

## 2. Estat inicial del projecte

Descriviu la situació del projecte abans de començar el treball de desplegament.

El projecte "plantilla" utilitzat s'ha clonat del repositori:  https://github.com/mattburrell/vite-react-docker

Incloeu:

- Estructura inicial del repositori

```
├── compose.yaml
├── Dockerfile
├── eslint.config.js
├── index.html
├── LICENSE
├── node_modules
│   ├── acorn
│   ├── ...
│   └── zod-validation-error
├── package.json
├── package-lock.json
├── public
│   ├── favicon.svg
│   ├── icons.svg
│   └── vite.svg
├── README.md
├── REPORT.md
├── src
│   ├── App.css
│   ├── App.jsx
│   ├── App.tsx
│   ├── assets
│   ├── index.css
│   ├── main.jsx
│   ├── main.tsx
│   └── vite-env.d.ts
├── tsconfig.json
├── tsconfig.node.json
├── vite.config.js
└── vite.config.ts
```
- Problemes detectats (si n’hi havia)
  
  No tenia .gitignore ni .dockerignore, mix de JavaScript i TypeScript.

- Existència o no de .gitignore

  No existía.

- Existència o no de Docker

  Tenía un dockerfile.

- Problemes de configuració o dependències

  He hagut de fer ```npm create vite@latest``` .

Reflexió breu:

Què faltava perquè aquest projecte es pogués considerar “professional”?

  Dockeritzar, treball col·laboratiu, .gitignore, .dockerignore, decidir-se per JavaScript o TypeScript.

## 3. Workflow Git aplicat

Expliqueu:

- Model de branques utilitzat



- Convencions de noms


- Estratègia de merge utilitzada



- Ús (o no) de rebase



- Incloeu exemples reals de commits rellevants (amb missatge i explicació del canvi).




## 4. Conflicte 1 – Mateixa línia

### 4.1 Com s’ha provocat

Expliqueu exactament quins canvis ha fet cada membre.

### 4.2 Missatge d’error generat

Incloeu la sortida real de Git.

### 4.3 Marcadors de conflicte

Mostreu el fragment amb:
```
<<<<<<< HEAD
=======
>>>>>>> branch
```
### 4.4 Resolució aplicada

Expliqueu:

- Quina decisió s’ha pres
- Per què s’ha escollit aquesta opció
- Com s’ha validat que funciona

### 4.5 Reflexió

Què heu après d’aquest conflicte?

## 5. Conflicte 2 – Dependències o estructura

### 5.1 Descripció del conflicte

### 5.2 Error generat

### 5.3 Resolució aplicada

### 5.4 Diferències respecte al conflicte anterior

## 6. Dockerització

### 6.1 Arquitectura final

Descriviu els serveis definits a docker-compose.yml.



### 6.2 Variables d’entorn

Expliqueu quines variables són necessàries i per què no es versiona el .env.

### 6.3 Persistència (si s'escau)

Expliqueu l’ús de volums.

###  6.4 Problemes trobats

Al treballar Docker amb maquina virtual fins ara i treballar per primer cop en el meu ubuntu personal, he trobat el problema:

```permission denied while trying to connect to the docker API socket```

Per no tenir permisos dins del grup Docker, en Bash. I el següent problema també: tampoc existeix el grup Docker. 

He creat el grup amb ```sudo groupadd docker``` i m'he donat permisos amb ```sudo usermod -aG docker agonzalezperis```.

## 7. Prova de desplegament des de zero

  Expliqueu els passos exactes que hauria de seguir una persona externa:
- Clonar repositori
- Executar comanda
- Accedir a l’aplicació  

Indiqueu també:
- Ports utilitzats
- Credencials de prova (si n’hi ha)

## 8. Repartiment de tasques

Descriviu què ha fet cada membre de l’equip.

## 9. Temps invertit

Indiqueu aproximadament:
- Temps dedicat a Git
- Temps dedicat a Docker
- Temps dedicat a documentació

## 10. Reflexió final

Responeu breument:

- Quina ha estat la part més complexa?
- Què faríeu diferent en un projecte real?
- Heu entès realment com funcionen els conflictes i Docker?