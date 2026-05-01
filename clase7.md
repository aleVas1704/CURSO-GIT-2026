## apuntes clase 7

Ignacio ALex Escobar Vasquez
Ing. Sistemas

### pull request (PR)

los pull request (PRs) son como una forma mas pro de trabajar con git y github.  
Basicamente es como pedir permiso para meter tus cambios al codigo principal.

Hacemos una rama luego hacemos cambios  y en github hacemos PR
y ahi los demas pueden ver que hicimos antes de aceptarlo :v

### ¿como crear un PR?

primero:

git push origin rama

luego vamos  a github y ahi sale la opcion para crear el pull request

### flujo de trabajo (con PR)

git checkout develop
git fetch 
git pull origin develop 

git checkout rama  # o -b 

git merge develop  # por si hubo cambios

# Aqui cuando trabajamos en nuestra rama

git push origin rama  # -u si es primera vez 

git checkout develop 
git fetch 

git checkout rama 
git merge develop  # otra vez por si hubo cambios 

# si hay conflictos:
lo arreglamos a mano 

git add . 
git commit 

(si usamos nano:) 
ctrl + o 
enter 
ctrl + x 

git push origin rama 

### ¿por que usariamos PRs?

porque si no, cualquiera puede subir cosas al repo sin avisar 
- pueden romper el codigo 
- meter cosas mal hechas 

los PRs hacen que:
- todos revisen los cambios 
- haya control 
- se pueda opinar antes de aceptar 

es como un filtro basicamente

### proteger el repositorio

aunque uses PRs, igual la gente podria subir cosas directo 
entonces se puede configurar github para obligar a usar PRs 

asi nadie puede mergear sin revision 

### colaborar sin ser invitado

si no eres colaborador igual puedes ayudar
- haces fork del repo
- haces tus cambios 
- y mandas un PR desde tu fork 
y ya el dueño decide si lo acepta o no 


