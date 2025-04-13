COMANDOS DE CONFIGURACIÓN INICAL
git config --global user.name <"Nombre">    ->  Asigna un nombre de usuario
git config --global user.email <"correo">   ->  Asigna el correo quien manipula git
git config --list               ->  Muestra la lista de parámetros de configuración

git init                        ->  Inicializar el repositorio git

git add <Nombre del archivo>    ->  Añadir archivo al stading
git add --all                   ->  Añadir todos los archivos al stading 
git add -A
git add .
git commit -m "Descripción"     ->  Commitar los cambios realizados por "git add"

git log                         ->  Ver el historial de commits
git status                      ->  Ver si hay un cambio en el repositorio git 
git diff                        ->  Verifica los cambios realizados

git show
git log --oneline

git checkout <id commit>

git stash
git stash clear
git stash lis
git stash apply

git merge
git branch