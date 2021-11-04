# Git, github, ramas y pull requests

Todos estos ejercicios asumen que ya conocés los comandos para crear nuevos repos, nuevas ramas, para ir a una rama ya creada, etc. Si alguno de los puntos te genera dudas, y no estás segura de cómo hacerlo, escribinos a Ivi o a mí!

## Ramas locales

1. Creá una nueva carpeta llamada `git-prueba-ramas`. 
2. Dentro de esa carpeta, agregá un archivo `README.md` que tenga el texto "Estoy en la rama main". 
3. Creá un nuevo repo de git en esa carpeta. 
4. Agregá los cambios y hacé un commit con el mensaje `primer commit`. 
5. Creá una nueva rama con el nombre `rojo`. 
6. En esa rama, modifica el mensaje del README para que diga "Estoy en la rama rojo". 
7. Guardá los cambios y agregalos en un commit cuyo mensaje sea `cambios en la rama rojo`. 
8. Volvé a la rama `main`. 
9. Confirmá que el mensaje de readme sea "Estoy en la rama main". 
10. Creá la rama `azul`. 
11. Modificá el README para que diga "Estoy en la rama azul". 
12. Agregá los cambios y hacé un commit con el mensaje `cambios en la rama azul`. 
13. Volvé a la rama `main`. 
14. Confirmá que el mensaje de readme sea "Estoy en la rama main". 
15. Andá a la rama `rojo`. 
16. Confirmá que el mensaje de readme sea "Estoy en la rama rojo".
17. Andá a la rama `azul`. 
18. Confirmá que el mensaje de readme sea "Estoy en la rama azul".
19. Desde la rama azul, creá una nueva rama `verde`. 
20. Confirmá que el mensaje dice "Estoy en la rama azul" ---> ¡Una nueva rama siempre se crea con los cambios de la rama desde donde se creó!
21. Modificá el mensaje para que diga "Estoy en la rama verde".
22. Agregá los cambios y hacé un commit que diga `cambios en la rama verde`. 
23. Volvé a la rama `main`. 
24. Confirmá que el mensaje de readme sea "Estoy en la rama main". 

### Comentarios

- Notá que siempre que creamos una rama, la nueva rama se crea **con los cambios de la rama desde donde la creamos**. 
  - Si creamos una rama desde `main`, la nueva rama va a decir "Estoy en la rama main". 
  - Si creamos una rama desde `azul`, la nueva rama va a decir "Estoy en la rama azul". 

*¿Por qué es importante tener esto en cuenta?*

Supongamos que tenés dos tareas en las cuales tenés que trabajar: el maquetado de la sección Balances y la funcionalidad de agregar nuevas categorías. 
Creás la rama `categorías` y a mitad del trabajo, decidís comenzar a trabajar en el maquetado de Balances. Si creás la rama `balances` desde la rama `categorías`, tu nueva rama va a tener todos los cambios que hiciste en `categorías`!

Para evitar confusiones, cuando trabajamos en equipo **siempre** creamos nuevas ramas a partir de `main`. Cada rama tiene los cambios que corresponden a esa rama: no mezclamos código de dos funcionalidades distintas en la misma rama. 

Eso implica que si estabas trabajando en `categorías` y querés pasar a trabajar en una rama nueva `balances`, tenés que:

1. En `categorías`, agregar tus cambios y hacer un commit. (nunca olvides el commit antes de cambiar de rama)
2. Ir a `main`. 
3. Crear la nueva rama `balances`. desde `main`. 

## Trabajando con github

1. Andá a github.com y creá un nuevo repositorio que se llame `git-prueba-ramas`
2. Una vez creado, volvé a tu consola. 
3. Confirmá que estás parada en la rama `main`. 
4. Seguí las instrucciones que te da github para hacer el push desde tu local. 
5. Actualizá la página de github y confirmá que podés ver tu README en github.
6. Andá a la sección "Branches" de tu repo en github. ¿Ves alguna rama? ¿Por qué pensás que las ramas `rojo`, `verde` y `azul` no están en github? 
7. Volvé a tu consola. 
8. Andá a la rama `rojo`. 
9. Confirmá que no haya cambios que no están agregados a un commit. 
10. Hacé push de tu rama. (Recordá que en el primer push de una rama, git te va a decir el comando que tenés que escribir). 
11. Volvé a github. 
12. Confirmá que ahora la rama `rojo` se puede ver en github. 
13. Hacé lo mismo para las ramas `verde` y `azul`. 


### Comentarios

- Notá que siempre que hacemos push de una rama, solo esa rama va a subirse a github. 

*¿Por qué es importante tener esto en cuenta?*

Si estás trabajando en muchas ramas a la vez, a veces podés confundirte y olvidar en qué rama estás. Si hacés push de la rama incorrecta, puede ser confuso ver que no está subida a github. 

Siempre que vas a hacer cambios en una rama, escribí muchas veces `git status` para confirmar en qué rama estás. Recordá que cuando hagas push, sólo esa rama va a actualizarse. 


## Trabajando con ramas locales y github

1. Una vez que todas tus ramas estén subidas a github, volvé a la consola. 
2. Andá a la rama `verde`. 
3. Modificá el README para que diga "Cambio en la rama verde después de haberla subido a github". 
4. Agregá tus cambios y hacé un commit con el mensaje `cambio numero 2 en rama verde`.
5. No hagas push todavía. Andá a github. 
6. En github, localizá la rama `verde`. Confirmá que el mensaje del README sigue siendo "Estoy en la rama verde". 
7. Volvé a la consola y hacé `git push`. 
8. Volvé a github y confirmá que ahora en github el README dice "Cambio en la rama verde después de haberla subido a github". 

### Comentarios

Notá que los cambios en github sólo ocurren después de haber hecho un push.  

*¿Por qué es importante tener esto en cuenta?*

Cuando estás trabajando de manera local, tu rama local tiene todos tus commits guardados, pero la rama remota (la que está en github) sólo va a tener esos cambios si los enviás explícitamente con un `push`. 

Cuando trabajamos en equipo, a veces olvidamos de actualizar la rama remota. Eso hace que nuestras compañeras no puedan tener acceso a todo el trabajo que hicimos. También puede provocar que nuestros Pull Request sean incorrectos. 

Cada vez que hacés cambios en tu rama local, recordá actualizar también la rama remota. 

