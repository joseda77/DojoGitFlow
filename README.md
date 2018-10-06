# DojoGitFlow

Comandos usados:


Gir hub:


- Prohibido los push directos a master, solo se hace la primera vez y luego se restringe así: 

	-En settings -  branches - nueva regla  - Require pull request review 

- Crear rama develop o ingresar por primera vez:
	
	git checkout -b develop - git push -u origin develop

- Crear un nuevo feature que salga de develop, Ramas que salen de develop:

	-Ubicado en la rama develop: git checkout -b feature/sales  ->  Luego para subirla: git push -v origin feature/sales 

- Agregar un nuevo cambio a la rama:

	Estando en la ramma -> git add -> git commit -> git push -u 'branchName' 

- Hacer un merge a la rama develop:

	- Nos vamos a la rama develop git checkout 'develop' -> git merge --no-ff 'nameBranch' -> {Si es necesario git pull} -> git push



- Borrar rama:

	git branch -D 'nameBranch'

- Para hacer una salida a producción se crea una nueva rama ej. realease/0.1.0 luego se hace un merge a esta rama de lo que se tiene en develop y luego se hace un pull request para hacer un merge a la rama master. si durante el pull request se determina que se debn hacer cambios, se llevan a cabo y luego se debe actualizar el develop con lo que haya quedado en realese/0.1.0. Luego por convención en Git hub en la sección code se agrega un nuevo realese, se le pone el nombre asociado, en este caso realese-0.1.0 y se le asocia la rama master.

' Agregar un isssue:
	
	Desde github en la sección Issues se crea un nuevo issue hablando sobre qué se debe modificar y especificando en qué archivo, este va a generar un número, luego cuando se vaya a hacer el commit solucionando el issue solo se da commit para que salga el archivo, en la primera línea se agrega el título de la solución y en la segunda se pone close#{num} siendo num el número del issue. Luego se asocia el proyecto en el que se encuentre el issue al release en el que se vaya a pasar a producción dichos arreglos y git hub se encarga de carrarlos automáticamente



