##apuntes clase 6

Ignacio Alex Escobar Vasquez
Ing.sistemas

### git merge:

merge es mezclar, entonces git merge sirve para juntar ramas. 
osea tienes una rama con cambios y la unes con otra para que todo quede en una sola.

el flag --no-ff (no fast forward) hace que no se pierda el historial de ramas 
y te obliga a crear un commit del merge, aunque se podria hacer automatico. 

####  git fetch:

git fetch es como revisar si hay cambios en el repositorio remoto pero sin afectar tu codigo.
osea el flujo que sigue es este :
ve si hay cambios  pero no los descarga directamente
solo es como un "mirar nomas"

### ¿qué es git pull?
- descarga los cambios
- los aplica a la rama

se usa asi para evitar errores:

git pull origin rama

---
### ¿qué es git push?

git push sirve para subir tus cambios al repositorio remoto (github).

osea:
- lo que hacemos en nuestra pc lo subimos

git push origin rama
git push -u origin rama


### flujo de trabajo (sin pull request)

un flujo  seria:

git checkout develop
git fetch
git pull origin develop
git merge --no-ff rama 

luego:
git add . 
git commit 

(si usas nano:)
ctrl + o  
enter  
ctrl + x  

despues borras la rama:

git branch -D rama  
y finalmente subes todo:

git push origin develop  

---

