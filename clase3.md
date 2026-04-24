## apuntes clase 3

- prompt de la IA usado: hey necesito mis apuntes para el dia 3, estuve en la clase y logre entender lo de la clase con
 respecto a la creacion de cuentas github y el ssh pero por cuestiones de tiempo debo usar un prompt con la ia debido
 a que este dia tuve 3 parciales :(, se que no es una gran escusa pero debo asegurar esas materias y tuve que priorizar eso
 disculpe, agrega este prompt al principio chat,
 https://www.youtube.com/watch?v=DSE7zzaMdlA  de este link de toyutube necesito que lo veas y hagas apuntes
 para ese dia con el formato que habiamos establecid

Ignacio Alex Escobar Vasquez
Carrera: Ingeniería en Sistemas

### github y para que sirve

github es como llevar git a internet, osea ya no solo tienes tu repositorio en tu pc sino que tambien lo puedes subir a la nube

sirve para:

* guardar tus repositorios en internet
* no perder nada aunque se dañe tu pc
* trabajar en grupo
* compartir codigo

git = local
github = nube

flujo:
primero haces commits en tu pc → luego haces push → y se sube a github

para usar github necesitas crear una cuenta y conectar tu pc con github


### conexion con github usando ssh

para conectar tu pc con github usamos ssh, porque es mas seguro que usar usuario y contraseña

pasos:

1. generar clave ssh:

```bash
ssh-keygen -t ed25519 -C "tu_correo"
```

2. iniciar el ssh agent:

```bash
eval "$(ssh-agent -s)"
```

3. agregar la clave:

```bash
ssh-add ~/.ssh/id_ed25519
```

4. copiar la clave publica:

```bash
cat ~/.ssh/id_ed25519.pub
```

5. ir a github → settings → ssh keys → pegar la clave

esto hace que github reconozca tu pc

---

### subir repositorio a github

para conectar tu repo local con github:

```bash
git remote add origin git@github.com:usuario/repositorio.git
```

luego subir:

```bash
git push -u origin master
```

o si usas main:

```bash
git push -u origin main
```

cosas importantes:

* `origin` = nombre del repo remoto
* `push` = subir cambios
* necesitas internet

si todo sale bien tu repo ya esta en github

en resumen:
github sirve para no perder tus cosas y trabajar mejor, y ssh es la forma segura de conectar tu pc con github
