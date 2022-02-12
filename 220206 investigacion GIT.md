# Investigación sobre GIT #

## Oscar Melchor i594201 ##


#¿Qué es GIT?#

Git es un **sistema de control de versiones distribuido**.

Esto significa que un clon local del proyecto es un repositorio de control de versiones completo (es decir 
en Git, la copia de trabajo del código de cada desarrollador es también un repositorio que puede albergar el historial completo de todos los cambios).

**Estos repositorios locales** plenamente funcionales **permiten trabajar sin conexión o de forma remota fácilmente**. Los desarrolladores confirman su trabajo localmente y, a continuación, sincronizan su copia del repositorio con la copia en el servidor. Este paradigma es distinto del control de versiones centralizado, donde los clientes deben sincronizar el código con un servidor antes de crear nuevas versiones.

**Git es**, con diferencia, **el sistema de control de versiones moderno más utilizado del mundo**.

Git tiene la funcionalidad, el rendimiento, la seguridad y la flexibilidad que la mayoría de los equipos y desarrolladores individuales necesitan.

**Git es un estándar de facto** Git es la herramienta con el mayor índice de adopción de su clase, lo que la hace muy atractiva

## Sus Origenes ##

Git es un proyecto de código abierto maduro y con un mantenimiento activo que desarrolló originalmente **Linus Torvalds**, el famoso creador del kernel del sistema operativo Linux, en 2005.


## Conceptos Básicos ##

Cada vez que se guarda el trabajo, Git crea una confirmación. Una confirmación es una instantánea de todos los archivos en un momento dado. 

Si un archivo no ha cambiado de una confirmación a la siguiente, Git usa el archivo almacenado anteriormente. Este diseño difiere de otros sistemas que almacenan una versión inicial de un archivo y mantienen un registro de diferencias a lo largo del tiempo.

Las confirmaciones crean vínculos a otras confirmaciones, formando un gráfico del historial de desarrollo.

## **Ramas** ##

Cada desarrollador guarda los cambios en su propio repositorio de código local. Como resultado, puede haber muchos 
cambios diferentes basados en la misma confirmación. 

Git proporciona herramientas para aislar los cambios y combinarlos posteriormente. Las ramas, que son punteros ligeros para trabajar en curso, administran esta separación. 

Una vez finalizado el trabajo creado en una rama, se puede combinar de nuevo en la rama principal (o tronco) del equipo. 


## **Archivos y Confirmaciones**

Los archivos de Git se encuentran en uno de estos tres estados: 
1. modificados, 
2. por fases o
3. confirmados. 

Cuando se modifica por primera vez un archivo, los cambios solo existen en el directorio de trabajo. Aún no forman parte de una confirmación ni del historial de desarrollo. 

El desarrollador debe realizar una fase de los archivos modificados para incluirse en la confirmación. 

El área de ensayo contiene todos los cambios que se incluirán en la siguiente confirmación. Una vez que el desarrollador está satisfecho con los archivos staged, se empaquetan como una confirmación con un mensaje que describe lo que ha cambiado. 

Esta confirmación se convierte en parte del historial de desarrollo.

## **Ventajas de GIT**

1. Desarrollo Simultaneo
2. Versiones más rápidas
3. Integración integrada
4. Sólido soporte de la comunidad técnica
5. Solicitudes de incorporación de cambios
6. Directivas de Rama : Las directivas de rama protegen ramas importantes al evitar inserciones directas, requerir revisores y garantizar compilaciones limpias.
7. Git funciona con cualquier equipo

## **Rendimiento** ##

Las características básicas de rendimiento de Git son muy sólidas en comparación con muchas otras alternativas. 

La confirmación de nuevos cambios, la ramificación, la fusión y la comparación de versiones anteriores se han optimizado en favor del rendimiento. Los algoritmos implementados en Git aprovechan el profundo conocimiento sobre los atributos comunes de los auténticos árboles de archivos de código fuente, cómo suelen modificarse con el paso del tiempo y cuáles son los patrones de acceso.

Su arquitectura distribuida también permite disfrutar de importantes ventajas en términos de rendimiento.

## **Seguridad** ##

Git se ha diseñado con la principal prioridad de conservar la integridad del código fuente gestionado.

El contenido de los archivos y las verdaderas relaciones entre estos y los directorios, las versiones, las etiquetas y las confirmaciones, todos ellos objetos del repositorio de Git, están protegidos con un algoritmo de hash criptográficamente seguro llamado "SHA1". 

De este modo, se salvaguarda el código y el historial de cambios frente a las modificaciones accidentales y maliciosas, y se garantiza que el historial sea totalmente trazable.

## Flexibilidad ##

Git es flexible en varios aspectos: en la capacidad para varios tipos de flujos de trabajo de desarrollo no lineal, en su eficiencia en proyectos tanto grandes como pequeños y en su compatibilidad con numerosos sistemas y protocolos.

Git se ha ideado para posibilitar la ramificación y el etiquetado como procesos de primera importancia (a diferencia de SVN) y las operaciones que afectan a las ramas y las etiquetas (como la fusión o la reversión) también se almacenan en el historial de cambios. 

No todos los sistemas de control de versiones ofrecen este nivel de seguimiento.


## Críticas de Git ##

Una crítica habitual sobre Git es que puede resultar difícil aprender a utilizarlo. 

Los usuarios nuevos y los procedentes de otros sistemas desconocerán parte de la terminología de Git, ya que esta puede ser diferente; por ejemplo, revert en Git tiene un significado distinto que en SVN o CVS. 

No obstante, Git es una herramienta muy competente y ofrece multitud de posibilidades a sus usuarios. 

Aprender a aprovechar estas posibilidades puede llevar un tiempo, pero una vez asimilados los nuevos conocimientos, el equipo puede hacer uso de ellos para acelerar su desarrollo.

Para los equipos que provienen de un sistema de control de versiones no distribuido, el hecho de contar con un repositorio central puede parecer una buena funcionalidad que no quieren perder. 

Sin embargo, aunque Git se ha diseñado como un sistema de control de versiones distribuido (DVCS), con él puedes seguir teniendo un repositorio oficial convencional donde se almacenen todos los cambios del software. 

En Git, como el repositorio de cada desarrollador lo incluye todo, no es necesario que su trabajo se vea limitado por la disponibilidad y el rendimiento del servidor "central". Durante las interrupciones o la ausencia de conexión, los desarrolladores pueden continuar consultando todo el historial del proyecto. 

Gracias a la flexibilidad y la arquitectura distribuida de Git, puedes trabajar como de costumbre, pero disfrutando de las ventajas adicionales de Git, algunas de las cuales puede que ni siquiera supieras que necesitabas.


## Conclusiones ##

1. Git es un sistema de control de versiones que presenta mejores características en comparacion a otros como SVN o CVS.
2. Ha sido criticado principalmente por los usuarios de sistemas anteriores ya que su concepto innovador requiere nuevos aprendizajes.
3. Su uso es extendido alrededor del mundo por su seguridad y caracteristicas que aseguran y facilitan el control de versiones.
4. Gracias a su aceptación extendida cuenta con amplio soporte de la comunidad técnica.
5. La implementación del algoritmo criptográfico SHA1 permite que los archivos y sus verdaderas relaciones esten protegidas.

## Comandos GIT ##

## Configuración Básica ##

Configurar Nombre que salen en los commits

	git config --global user.name "dasdo"
Configurar Email

	git config --global user.email dasdo1@gmail.com
Marco de colores para los comando

	git config --global color.ui true

## Iniciando repositorio ##

Iniciamos GIT en la carpeta donde esta el proyecto

	git init
Clonamos el repositorio de github o bitbucket

	git clone <url>
Añadimos todos los archivos para el commit

	git add .
Hacemos el primer commit

	git commit -m "Texto que identifique por que se hizo el commit"
subimos al repositorio

	git push origin master

## GIT CLONE ##
Clonamos el repositorio de github o bitbucket

	git clone <url>
Clonamos el repositorio de github o bitbucket ?????

	git clone <url> git-demo

## GIT ADD ##
Añadimos todos los archivos para el commit

	git add .
Añadimos el archivo para el commit

	git add <archivo>
Añadimos todos los archivos para el commit omitiendo los nuevos

	git add --all 
Añadimos todos los archivos con la extensión especificada

	git add *.txt
Añadimos todos los archivos dentro de un directorio y de una extensión especifica

	git add docs/*.txt
Añadimos todos los archivos dentro de un directorios

	git add docs/

## GIT COMMIT ##
Cargar en el HEAD los cambios realizados

	git commit -m "Texto que identifique por que se hizo el commit"
Agregar y Cargar en el HEAD los cambios realizados

	git commit -a -m "Texto que identifique por que se hizo el commit"
De haber conflictos los muestra

	git commit -a 
Agregar al ultimo commit, este no se muestra como un nuevo commit en los logs. Se puede especificar un nuevo mensaje

	git commit --amend -m "Texto que identifique por que se hizo el commit"
## GIT PUSH ##
Subimos al repositorio

	git push <origien> <branch>
Subimos un tag

	git push --tags
GIT LOG
Muestra los logs de los commits

	git log
Muestras los cambios en los commits

	git log --oneline --stat
Muestra graficos de los commits

	git log --oneline --graph
## GIT DIFF ##
Muestra los cambios realizados a un archivo

	git diff
	git diff --staged

## GIT HEAD ##
Saca un archivo del commit

	git reset HEAD <archivo>
Devuelve el ultimo commit que se hizo y pone los cambios en staging

	git reset --soft HEAD^
Devuelve el ultimo commit y todos los cambios

	git reset --hard HEAD^
Devuelve los 2 ultimo commit y todos los cambios

	git reset --hard HEAD^^
Rollback merge/commit

	git log
	git reset --hard <commit_sha>
## GIT REMOTE ##
Agregar repositorio remoto

	git remote add origin <url>
Cambiar de remote

	git remote set-url origin <url>
Remover repositorio

	git remote rm <name/origin>
Muestra lista repositorios

	git remote -v
Muestra los branches remotos

	git remote show origin
Limpiar todos los branches eliminados

	git remote prune origin 
## GIT BRANCH ##
Crea un branch

	git branch <nameBranch>
Lista los branches

	git branch
Comando -d elimina el branch y lo une al master

	git branch -d <nameBranch>
Elimina sin preguntar

	git branch -D <nameBranch>
## GIT TAG ##
Muestra una lista de todos los tags

	git tag
Crea un nuevo tags

	git tag -a <verison> - m "esta es la versión x"
## GIT REBASE ##
Los rebase se usan cuando trabajamos con branches esto hace que los branches se pongan al día con el master sin afectar al mismo

Une el branch actual con el mastar, esto no se puede ver como un merge

	git rebase
Cuando se produce un conflicto no das las siguientes opciones:

cuando resolvemos los conflictos --continue continua la secuencia del rebase donde se pauso

	git rebase --continue 
Omite el conflicto y sigue su camino

	git rebase --skip
Devuelve todo al principio del rebase

	git reabse --abort
Para hacer un rebase a un branch en especifico

	git rebase <nameBranch>
## OTROS COMANDOS ##
Lista un estado actual del repositorio con lista de archivos modificados o agregados

	git status
Quita del HEAD un archivo y le pone el estado de no trabajado

	git checkout -- <file>
Crea un branch en base a uno online

	git checkout -b newlocalbranchname origin/branch-name
Busca los cambios nuevos y actualiza el repositorio

	git pull origin <nameBranch>
Cambiar de branch

	git checkout <nameBranch/tagname>
Une el branch actual con el especificado

	git merge <nameBranch>
Verifica cambios en el repositorio online con el local

	git fetch
Borrar un archivo del repositorio

	git rm <archivo> 
Fork
Descargar remote de un fork

	git remote add upstream <url>
Merge con master de un fork

	git fetch upstream
	git merge upstream/master