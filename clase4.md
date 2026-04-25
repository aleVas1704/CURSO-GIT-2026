## Apuntes Clase 4

Ignacio Alex Escobar Vasquez
Carrera: Ingeniería en Sistemas
-prompt de la IA usado: https://www.youtube.com/watch?v=pTg7MOEYIrw,SCESI Postulaciones 2026: Git remote, SSH Multiple y 
Git checkout - Clase 4 necesito nuevmente el resumen de la clase ya que nuevamente no he podido priorizar el tiempo. el punto
bueno es que ya se acabaron gran parte de mis parciales :v

### git remote y para que sirve

git remote sirve para conectar nuestro repositorio local con uno en internet (como github), es basicamente decirle a git donde esta nuestro repositorio en la nube

un remote es como un alias o nombre, normalmente se usa origin
comandos importantes:

ver remotos:
git remote -v

 agregar remoto:
git remote add origin git@github.com:usuario/repositorio.git

cambiar url:
git remote set-url origin nueva_url


esto permite hacer push y pull con el repositorio remoto

---

### ssh multiple (varias cuentas github)

cuando tienes varias cuentas (por ejemplo personal y universidad), no puedes usar una sola clave ssh porque se mezclan

la solucion es crear varias claves ssh y configurarlas

cada clave tiene:

 clave publica (se sube a github)
 clave privada (se queda en la pc)

se crean varias claves y luego se configura el archivo:

~/.ssh/config

### git checkout (cambiar versiones o ramas)
git checkout sirve para cambiar entre ramas, archivos o versiones del proyecto

por ejemplo:

 cambiar de rama:

git checkout nombre_rama

crear y cambiar a una nueva rama:

git checkout -b nueva_rama

cuando haces checkout git cambia el estado del proyecto a esa version

tambien existe algo llamado detached HEAD, que es cuando no estas en una rama sino en un commit especifico
