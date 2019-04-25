/////////////////////////////
///configurar git (entorno)//
/////////////////////////////
git config --global user.email -> sch.damian@hotmail.com
git config --global user.name  -> damian_devops
git config --global color.ui true

/////////////
///terminal//
////////////
mostrar y crear carpetas

cd :-/

mkdir <nombre de la carpeta> -> crear carpetas en la terminal

ls -> muetra todas las carpetas

clear -> limpiar terminal

touch <nombre del archivo> -> crea archivos

rm <nombre del archivo> -> borra el archivo

rm -rf <nombre de la carpeta> -> borra la carpeta

////////////////
//comandos git//
///////////////
stage: es la parte quedan los archivos pendientes a subir
se guardar en x carpeta del directorio proyecto

git init <nombre_del_repositorio>opcional -> crea una carpeta he inicia el repositorio

para borrar el repositorio local borrar la carpeta .git(esta como archivos ocultos)

git s --> muestra el estado de los archivos

git add .--> agrega los archivos al stage

git add -A --> agrega todos los archivos al stage

git rm --cached <nombre del archivo> --> quita el archivo del stage

git rm -f <nombre del archivo> --> quieta el archivo del stage y lo borra fisicamente

git add -n <nombre del archivo> --> agrega los archivos y omite el especificado

git add <nombre del archivo> --> agrega el archivo especificado

git commit -m <nombre del commit> --> agregar un nuevo commit 

git commit -m <nombre del commit> --amed --> agrega archivos previos al commit y los anexa al ultimo commit

git log --> muestra los commit a subir

git tag --> -a <version> -m "<nombre del tag>"

git tag -l --> version actual de proyecto

git tag <version> <38b88ac7fad1cd1043ce4bb2d5ef00833ae45313>(hash del proyecto) --> añade una version al commit especificado

git tag -d <version> --> borra la version especificada

git tag -f -a <version> -m "<texto>" <hash> --> renombra la version del commit especificado

git log --oneline --> muestra los log en una sola linea sin la fecha,nombre y email

git log -3 --> cantidad de commit a mostrar

git diff <hash del commit> --> muestra que cambios hubo en el commit especificado

git diff <hash del commit> <hash del commit> --> compara las versiones o commit 

git diff [version 1] vs  [version 2] --> compara las versiones o commit 

git reset --soft [hash del commit] --> quita los cambios apartir del especificado, pero lo mantiene preparado para el commit, los mantiene en el stage

git reset --mixed [hash del commit] --> quita los cambios apartir del especificado, saca los archivos y modificaciones en el stage 

git reset --hard  --> borra los archivos agregados al proyecto y quita las modificaciones,
solo los archivos que estan en el stage o commit.

git reset --hard [hash del commit] --> borra los archivos agregados al proyecto y quita las modificaciones,
solo los archivos que estan en el stage o commit.(guardar los log en un archivo antes de hacer un --hard)

git config --global core.editor "code --wait" --> cuando ingresamos un commit sin descripcion abre el editor seleccionado por nosotros.

#ramas

git branch -l --> lista todas las ramas actuales

git branch <nombre de la rama que se va crear>

git branch -d <nombre de la rama que se va a borrar>

git branch -D <nombre de la rama que se va a borrar por mas que tenga commits>

git branch -m <nombre de la rama a reemplazar> <nombre nuevo>

git checkout <nombre de la rama a trabajar>

git checkout -b <nueva-imagen> --> crea una nueva rama y se pasa a la misma

git checkout <nombre del archivo> --> este comando saca las modificaciones echas en el archivo a su ultimo estado guardado en el stage.

git merge <nombre de la rama> --> lo que hace esta funcion es mesclar la rama seleccionada con la que estamos posicionados actualmente aplica los cambios del seleccionado sobre la cual estamos en este caso (master)

git rebase <nombre de la rama> --> lo hace de forma ordenada la mescla (solo se recomienda hacerlo localmente
porque reescribiria los cambios de los demas repositorios)

git cherry-pick <nombre del commit> --> lo que hace es pasar este commit de una rama a la que estamos actualmente