COMANDOS DE CONFIGURACIÓN INICAL
git config --global user.name <"Nombre">    ->  Asigna un nombre de usuario
git config --global user.email <"correo">   ->  Asigna el correo quien manipula git
git config --list               ->  Muestra la lista de parámetros de configuración

CONFIGURACIÓN DE COLOR DE TERMINAL
git config color.status.branch <color>      ->  Cambio de color del texto de branch
git config color.status.added <color>       ->  Cambio de color del texto de added
git config color.status.untracked " <color> blond"  ->  Cambio de color del texto en blond de los cambios del área de trabajo

CONFIGURACION SSH KEYS
ssh-keygen -t ed25519 -C "comentario"   ->  Genera una llave sshh
eval "$(ssh-agen -s)            ->  inicializa la interfaz ssh para gestionar las keys
ssh-add <~/.ssh/id_ed25519>     ->  Añade la key ssh al agen
clip < ~/.ssh/id_ed25519.pub    ->  Copia la llave ssh al portapapeles

COMANDOS DE TERMINAL LINUX
mkdir <nombre de carpeta>       ->  Crea carpeta
cd  <nombre de la carpeta>      ->  Ir a una carpeta
touch   <nombre del arcivo>     ->  Crea un archivo
ls                              ->  Muestra los archivos y carpetas dentro de una carpeta
ls -a                           ->  Muestra todos los archivos y carpetas uncluyendo los ocultos
clear                           ->  Limpia la terninal

COMANDOS DE REPOSITORIO
git init                        ->  Inicializar el repositorio git

git status                      ->  Ver si hay un cambio en el repositorio git 
git status -s                   ->  Ver los cambios en un formato corto

git log                         ->  Ver el historial de commits de forma extensa
    git log --oneline           ->  Ver el histrial de los commits en una sola línea
    git log -n <numero>         ->  Ver el historial limitada por un numeral (ver los último 'numero' commits)
    git log --oneline -n <número>   ->  Ver el historia limitada en una sola línea
    git log format = <short-medium-full>    ->  Ver el historial de forma corta, regular o extendida

git add <Nombre del archivo>    ->  Añade archivo al staging
    git add *.js                ->  Añade todos los archivos .js con cambios al staging (.js es un ejemplo)
    git add src/component-*     ->  Agrega todo los archivos que empiecen con el patron "src/component-"
    git add --all               ->  Añade todos los archivos al staging 
    git add -A                  ->  Agrega todos los archivos con cambios en el proyecto
    git add .                   ->  Agrega los cambios de todos los archivos a la dirección actual
    git add -u                  ->  Agrega todo los archivos modificado o eliminados

git reset                       ->  Devuelve cambios en archivos a la zona de trabajo (lo saca del staging)
    git reset --soft <hash del commit>  ->  Deshace el commit, pero mantiene los cambios en el área de stagin
    git reset --hard <hash del commit>  ->  Deshace el commit y deshace los cambios

git commit -m "Descripción"     ->  Commitar los cambios realizados por "git add"

git pull
git diff                        ->  Verifica los cambios realizados

git show <id commit>            ->  Mostrar el proyecto (archivo) en cada commit

git checkout <id commit - branch>               ->  Ir a un commit o branch en específico.
    git checkout <nombre del archivo>           ->  Descarta los cambios echos y muestra los cambios del archivo guradados en el repositorio
    git checkout .                              ->  Descarta los cambios del todo el proyecto
    git checkout --ours <nombre del archivo>    ->  Conserva los cambios de la rama padre (cuando hay un conflicto)
    git checkout --theirs <nombre del archivo>  ->  Conserva los cambios de la rama hija (cuando hay un conflicto)

git stash                       ->  Crea una instancia donde se almacena los cambios dentro del staging
    git stash clear             ->  Elimina la instancia
    git stash list              ->  Mustra las intancias creadas
    git stash apply <isntancia stash>   ->  Muestra la lineas almacendas en la instancia
    git stash pop               ->  Restablece los cambios guardados del stash
    git stash pop <id del stash>    ->  Muestra los cambios guardados en el stash
    git stash save <nombre>     ->  Crea la istancia stash y lo nombra
    git stash --include-untracked   ->  Agrega en el stash archivos nuevos no enlazados en git

git branch                      ->  Muestra una lista de las branches creadas
git switch -c <nombre de la rama>   ->  Crear nueva rama
git branch -D <nombre de la rama>   ->  Eliminar rama
git switch <nombre de la rama>  ->  Navegar tu area de trabajo a otra rama
git merge                       ->  FusioNa los cambias de una branch a otra

git remote add origin <dirección de GitHub>     -> Vinvula el repositorio local a GitHub
git branch -M main              ->  Cambio de nombre de la rama Master a Main
git push -u origin main         ->  Actualiza los cambios realiados al repositorio remoto, asocia la rama "main" para enviar los cambios
git pull                        ->  Actualiza el repositorio local con respecto al remoto

git clone   <URL HTTP - SHH>    ->  Clona el repositorio remoto

git restore --staged            ->  Pasar los cambios dentro del staged al área de trabajo

git revert                      ->  Revierte los cambios de un commit (ejem.: commit 'X' - elimina la linea 3, al usar git revert. coloca la    
                                    linea 2)

git rebase -i <nombre de la rama padre>   ->  Actualiza los cambios de una rama con respecto a la rama padre

git commit --amend              ->  Cambia la descripción del último commit
    """
    git add <nombre del archivo>
    git commit --amend          ->  Guarda el cambio en el último commit; se requiere tener los cambios en área de stagin
    """

git cherry-pick <hash del commit>   ->  Actualiza los cambios de una rama a otra rama (copiar los cambios)