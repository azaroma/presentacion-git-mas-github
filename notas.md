
## ¿Por qué Git?
Es un proyecto maduro, mantenido activamente. Fue creado por Linus Torvalds, el creador del kernel de Linux. Git es un sistema de control de versiones distribuido. Además, Git ha sido diseñado teniendo el desempeño, la flexibilidad y la seguridad en mente.

### Desempeño
Git tiene implementados algoritmos que maximizan su desempeño. También permite un flujo de trabajo más dinámico al ser distribuido.

### Seguridad
Git utiliza un algoritmo de criptográficamente seguro llamado SHA1 para proteger la integridad de la información.

### Flexibilidad
Git es flexible porque soporta varios tipos de flujos de trabajo no lineares, porque es eficiente en proyectos grandes y pequeños, y porque es compatible con muchos sistemas y protocolos.

## Repositorio
En los sistemas de control de versiones, un repositorio es una estructura de datos que almacena metadatos y/o un sistema de archivos.
Algunos de los metadatos que el repositorio almacena son, entre otros:
* Un registro histórico de los cambios en el repositorio
* Un conjunto de objetos _commit_
* Una serie de referencias a objetos _commit_, llamadas _heads_ 

## Inspección
`git log` permite ver la historia de commits de un repositorio.
`git status` muestra el estado del directorio en uso y el área de staging. Muestra los cambios que están en el área de staging y los que no están ahí, y cuuales archivos no están siendo rastreados por git.

## git add
Git add es un comando multipropósito porque sirve para rastrear nuevos archivos o para enviar al área de staging archivos que han sido modificados (sin importar si están o no en el área de staging).

## .gitignore
Hay veces que nuestro sistema genera archivos que no queremos que sean añadidos a nuestro repositorio, para eso contamos con la herramienta `.gitignore`; que es un archivo que mediante glob patterns le indica a git qué tipo de archivos debe ignorar.

## git commit
Una vez que tu staging area está como tú quieres, puedes hacer un commit. Pensemos en un commit como en un snapshot o un checkpoint, un estado determinado de nuestro proyecto que quisieramos recordar. Este es un nodo en la historia de cambios de nuestro proyecto.

## Branching
La historia de cambios de nuestro repositorio es una línea del tiempo seccionada en nodos (commits), que son referencias a un estado específico de nuestros archivos. Las ramas son bifurcaciones de esa línea del tiempo, con un sistema de archivos independiente.

## Merging
Es posible fusionar dos líneas del tiempo separadas; el comando que lo permite es `git merge <incoming-branch>`. Para hacerlo es necesario hacer un `checkout`de la rama a la que queremos traer la rama objetivo. Este mecanismo utiliza el mejor ancestro común de los últimos `commits` y dichos `commits` para crear un nuevo `commit` común a partir del cual ambas ramas comparten el contenido.

## Github
Github es una plataforma de desarrollo colaborativo para alojar proyectos utilizando el sistema de control de versiones Git. Su función más importante es la de servidor remoto para permitir el flujo de trabajo distribuido, es decir, Github alojará un repositorio remoto para nuestro proyecto. Además proporciona un wiki, una página y métricas de colaboración para cada proyecto. También proporciona rastreo de bugs, petición de características y administración de tareas.

## Repositorio remoto
El 90% del trabajo ocurre en los repositorios locales. Como ya dijimos, un repositorio remoto nos permite trabajar en colaboración con otros desarrolladores aunque estemos en distintas partes del planeta. Un repositorio remoto de Github se distingue de uno local porque no tiene los archivos como tal, únicamente contiene el directorio `.git`; esto es así porque el repositorio remoto sólo sirve para recibir y distribuir cambios, no para trabajar sobre sus archivos.
