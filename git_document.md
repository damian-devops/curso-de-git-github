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

git log --online --> muestra los log en una sola linea sin la fecha,nombre y email