#	Curso Git (HolaMundo)
##	Para ver la versión instalada (no es necesiario si tienes el sistema acutalizado)
❯ git --version
git version 2.45.0

##	Configuración Global
	- git config --global user.name "Oscar Flores"	//configura el nombre de usuario
	- git config --global user.email anscaryo@gmail.com	//configura el email
	- git config --global core.editor "code --wait"	//Configura el editor por defecto
	- git config --global core.editor "nvim -f"	//Configura el editor por defecto
	- git config --global -e	//muestra la configuración en el editor.
	- git config --global core.autocrlf input (mac y linux) true (windows)

##	Primeros pasos.
	- git init	//inicializa git para controlar todo lo que este en la carpeta.
	- git status (gss)	//nos muestra el estado de los archivos que estan en el directorio.
	- git add  (los nombres de los archivos que se van a seguir)
	- git add --update (gau)	//Actualiza el estado de los archivos ya añadidos
	- git commit -m "Comit inicial del curso"	//Los archivos ya se han comiteados
	- git commit	//Nos abre el editor para añadir el texto del commit
	- git rm 'nombre del archivo' elimina el archivo indicado y lo añade al estado. Solo quedaria hacer un commit -m "texto descriptivo"
	- git restore --staged 'nombre del archivo'
	- git mv 'nombre' 'nuevo_nombre'	//Renombra el achivo y lo añade a git
	- .gitignore se incluyen los archivos y carpetas que no queremos que sean controlados
	- git diff	//nos muestra las diferencias en los archivos modificados
	- git log --oneline --decorate --graph	(glog)
	- git log --oneline --decorate --graph --all	(gloga)
	
##	Branch (Ramas)
	- git branch 	// muestra las ramas presentes
	- git checkout -b {nombre branch}
	- git merch {nombre rama}	// trae los cambios de la rama secundaria a la *actual*.


##	Volver a un estado anterior (rollball)
### 	(eliminar un archovo o hacer una modificacion que no funciona y ya se ha hecho el commit correspondiente)
	- git reset --hard (tabulador y aparecen los commit con sus respectivos comentarios, completa el comando con el numero de HEAD que corresponda)
	╭─    ~/Documentos/miweb  on   main
	╰─ git reset --hard 1bf79e5
	HEAD       main       ORIG_HEAD
	1bf79e5  -- [HEAD]    Agregando una modificación (15 minutes ago)
	5eae20f  -- [HEAD^]   Commit inicial del proyecto (16 minutes ago)

