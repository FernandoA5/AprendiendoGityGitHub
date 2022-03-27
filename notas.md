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

