
###"git log" muestra el historial de commits
`git log --pretty=format:"%h - %an, %ar : %s"`
Muestra el historial con el formato que indiquemos.

###Limitar la salida del hitorial
`git log -n` : Cambiamos la n por cualquier otro numero entero.
`git log --after="2018-02-25 00:00:00"` Muestra los commits realizados despues de la fecha especificada
`git log --before="2018-02-25 00:00:00"` Muestra los commits realizados antes de la fecha especificada

Las banderas del comando `git log` se pueden usar juntas segun nos convenga
