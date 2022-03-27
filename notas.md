*Curso de Git y GitHub*
git init » Inicializa el repositorio
git add archivo » agrega un archivo a los cambios
git add . » Agrega todos los archivos a los cambios
git commit -m "Mensaje" » Envía los cambios al repositorio con un mensaje
git status » Muestra el status del repositorio
git show » Muestra todos los cambios historicos
git log archivo » Muestra la historia de un archivo.
git rm -f archivo » Elimina un archivo de los cambios y de la computadora
git rm --cache archivo » Elimina un archivo de los cambios, pero lo mantiene en la computadora.

git diff id1 id2 » Nos muestra la diferencia entre dos commits enviados al repositorio. La id la obtenermos con: git log archivo » y ahí podremos ver la id/hash de cada commit.

Ramas:
La rama master es donde se tiene la versión principal del proyecto.
La rama development es donde se hacen los experimentos de desarrollo (donde se trabaja)
La rama hotfix es donde se hacen los arreglos de errores urgentes.

Reset:
git reset IDdelCommit --hard » Restaura absolutamente todo el repositorio al estado del IDCommit seleccionado.
git reset IDdelCommit --soft » Restaura el proyecto, pero el staging de la memoria se mantiene, lo que había en el último commit aún está ahí disponible para agregarse y se agregará en el siguiente commit.
git reset HEAD » Este comando saca los archivos del area de staging. Para que los ultimos cambios de estos archivos no se envíen en el último commit. Para re-agregar esos cambios al staging, usamos git add .


git log --stat » muestra cambios detalladamente que han tenido los archivos en su historia.

checkout:
git checkout idCommit archivo » Restaura un archivo a la versión del commit seleccionada.

git checkout master commit » Restaura un archivo a la versión de la linea actual de master.

Para obtener un repositorio remoto » git clone url
Para enviar mis cambios a un repositorio remoto » git push
Para obtener una actualización del repositorio remoto » git fetch
Git Fetch no copia el repositorio en mis archivos para fusionarlo, necesito hacer un git merge.
git merge » fusiona el código.
git pull » Copio el repositorio local y el remoto actualizado para fusionarlos.

git commit -am "mensaje" » Agrega los cambios (como un add) y además realiza el commit con un mensaje. Esto solo funciona con archivos que ya habían sido agregados antes. Un archivo untracked no se agregaría.

//CREAR RAMAS
git branch NombreDeLaRama » Crea una nueva rama
git checkout NombreDeLaRama » Nos cambia hacia esa nueva rama.
git branch » Nos muestra la lista de ramas, y resalta la rama en la que estamos.

El merge se debe hacer desde la rama principal, pues la rama desde la que se hace el merge se vuelve la rama principal.

git merge RamaQueQuieroFusionar(No la principal)
El merge requiere un mensaje

Una forma de actualizar una rama despues de que el maste avanza, es haciendo un merge desde la rama que querémos actualizar.

Para solucionar los conflictos, es necesario ir a los archivos y resolverlos manualmente, aparecen como:
<<<<<< Master
	cambio 1
====== 
	cambio 2
>>>>>> OtraRAma

En este punto solo dejamos un cambio y borramos el otro junto con los simbolos. Esto se puede hacer manualmente, o dejar que VS code lo haga diciendole que cambio queremos aceptar.

Para importar nuestro repositorio hacía > GitHub usamos el comando:
git remote add origin URL

git remote » nos muestra que tenemos un origin.
git remote -v » nos muestra que tenemos un origin para hacer fetch y un origin para hacer push.

git push origin master » nos permite enviar los cambios de nuestro repositorio, al repositorio remoto.

git pull origin main » Nos permite traer los archivos desde el repositorio remoto, hacia nuestro repositorio local (origin)

git pull origin main --allow-unrelated-histories » Esto permite que se el pull fucione cuando las historias de las ramas son diferentes.

git remote set-url origin URL » sirve para cambiar la url del repositorio Remoto en el repositorio local

git push origin master:main » sirve para decirle a GitHub que nuestra rama master es igual a su rama main.

git config -l » nos enlista las configuraciones de git.

//LAVES PUBLICAS Y PRIVADAS
Comando para llave privada:
ssh-keygen -t rsa -b 4096 -C "correo@correo.com"

eval $(ssh-agent -s) » Comando para sabér si el agente de ssh está corriendo.
