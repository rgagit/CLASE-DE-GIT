layout: true
background-image: url(bg1.png)
background-position: left bottom

---
class: center, middle

# Git

Daniel Varela

[dan@nearsoft.com](http://nearsoft.com)

---

.left-column[
# Agenda
]
.right-column[
### 1. ¿Qué es git?
### 2. ¿Por qué debería usarlo?
### 3. Principales características
### 5. Comandos
### 6. Repos remotos
]

---
.left-column[
### ¿Qué es git?
]
.right-column[
**Git** permite a a los equipos trabajar usando el **mismo conjunto de archivos**. También ayuda al equipo a enfrenetar la confusión 
que se genera cuando multiples personas estan editando el mismo archivo.

- Software para control de versiones

- Historia de mí código

- Mí código esta seguro (lost code)

- Arquitectura distribuída 

- ¡Rápido!

- Cada desarrollador tiene su propia copia del código

- Linus Torvalds (2005)
]

---
.left-column[
### ¿Qué es git?
### ¿Por qué usarlo?
]
.right-column[
- Código **roto** o **deficiente**

- Código **perdido**

- **Diferentes** versiones en tu producto

- **Multiples personas** trabajando sobre la misma caracteristica de producto

]
---
.left-column[
### ¿Qué es git?
### ¿Por qué usarlo?
### Características
]
.right-column[

- Cada vez que que realizas un  **`'commit'`** o guardas el esado de tu proyecto, git toma una foto de tus archivos en ese momento y guarda una referencia a ese punto de la historia en tu proyecto.


- No almacena **duplicados** solo **referencias**  🤓

- Git fue pensado como una **cadena de fotos (deltas)** de los archivos

- Git no necesita ir a un **servidor externo** para obtener el historial

]

---
.left-column[
### ¿Qué es git?
### ¿Por qué usarlo?
### Características
### Comandos 
]
.right-column[
#### `git init`
#### `git clone <repo>`
#### `git status`
#### `git add <dir>`
#### `git commit`
#### `git branch`
#### `git checkout <branch>`
]

---
.left-column[
### Comandos
#### `git init`
]
.right-column[
  #### `git init`
  Inicializa tu directorio actual para el control de versiones con git

  .dark-red[`ejemplo:`]

  ```shell
  $ git init
  ```

  Creará una carpeta llamada **`.git/`** en el directorio actual que contiene las información necesaria para el control de versiones


]

---
.left-column[
### Comandos
#### `git init`
#### `git clone`
]
.right-column[
  #### `git clone`
  En caso de que tu repositorio (proyecto) ya exista, puedes copiarlo (clonarlo) con el comando `git clone`

  .dark-red[`ejemplo:`]

  ```shell
  $ git clone project-dir/
  ``` 

  **`project-dir/`** puede ser un repositorio local o remoto.red[*]

]

---
.left-column[
### Comandos
#### `git init`
#### `git clone`
#### `git status`
]
.right-column[
  #### `git status`
  Muesrta el estatus de mi repositorio:
    - Archivos modificados
    - Archivos nuevos
    - Achivos fuera del controll de versiones 
      ('untracked files')
    - Branch actual

.dark-red[`ejemplo:`]
```shell
$ git status
```

```shell
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

  bg1.png
  index.html
```

]

---
.left-column[
### Comandos
#### `git init`
#### `git clone`
#### `git status`
 #### `git add`
]
.right-column[
  #### `git add`
  Agrega archivos nuevos y modificados a el area de staging del repositorio
  
  Acepta como parametro archivos o directorios que se desean agregar


  .dark-red[`ejemplo:`]

  agrega el archivo **`app.rb`** a la zona de `staging`
  ```shell 
  $ git add ruby-school/app.rb 
  ```

  agrega los archivos del **`directorio actual`** a la zona de `staging`
  ```shell
  $ git add .
  ``` 

  ]

---
.left-column[
### Comandos
#### `git init`
#### `git clone`
#### `git status`
#### `git add`
#### `git commit`
]
.right-column[
  #### `git commit`
  Registra los cambios en la zona de .dark-red[`'staging'`] al repositorio y los hace **`rastreables`**, **`recuperables`** y **`revisables`**

  .dark-red[`ejemplo:`]

  ```shell
  $ git commit -m 'mensaje corto y descriptivo'
  ```
  
  
  despues, revisa los cambios en el log del repo
  ```shell
  $ git log
  ```
  
  ```shell
  commit 10aa66125f1539f78245d657174efda4efe3dc99
  Author: dvarela <dan@nearsoft.com>
  Date:   Tue Jun 1 16:24:45 2017 -0600

      mensaje corto y descriptivo
  ```
]

---
.left-column[
### Comandos
#### `git init`
#### `git clone`
#### `git status`
#### `git add`
#### `git commit`
#### `git branch`
]

.right-column[
  #### `git branch`
  Un .dark-red[`branch`] es un apuntador a un **`commit`** específico de otro branch (rama base `master`).
  Representa una división del código base y permite realizar cambios sin afectar los cambios originales 

  Es útil para mantener multiples versiones del mismo proyecto (`v1.0`, `v1.5`)

  .dark-red[`ejemplo:`]
  
  lista todos los branches de este repositorio
  ```shell
  $ git branch  
  ```
  crea un nuevo branch
  ```shell
  $ git branch v1.5.0
  ```       

]


---

.left-column[
### Comandos
#### `git init`
#### `git clone`
#### `git status`
#### `git add`
#### `git commit`
#### `git branch`
#### `git checkout`
]

.right-column[
#### `git checkout`
Una vez creados los branches necesarios, **`git checkout`** permite moverme entre estos brachnes 

.dark-red[`ejemplo:`]

```shell
$ git checkout v1.5 
```

```shell
Switched to branch 'v1.5'
```
]


---
.left-column[
### ¿Qué es git?
### ¿Por qué usarlo?
### Características
### Comandos 
### Repos remotos
]
.right-column[
#### `git push`
#### `git pull`
]


---
class: center, middle
# ¿Preguntas?