Iniciar sesión en Heroku en la CLI

```
heroku login
```

Después de eso, agregue un control remoto a su repositorio local con:

```
heroku git:remote -a heroku-app-name
```

Luego presione el código usando:

```
git push heroku <github-branch-name>
```

Esto se hace para asegurarse de que todo funcione correctamente antes de automatizarlo. Puede hacer clic en la aplicación abierta en el panel de la aplicación Heroku para verificar si funciona correctamente.

### Inicia sesión en el aspecto contenedor de Heroku.

```
heroku container:login
```

### Crea aplicacion en heroku

```
heroku create APP_NAME
```

### Construye el contenedor docker localmente y envía la imagen a Heroku para que lo tenga.

```
heroku container:push web -a APP_NAME
```

### Dice a Heroku que libere ese contenedor

```
heroku container:release web -a APP_NAME
```
