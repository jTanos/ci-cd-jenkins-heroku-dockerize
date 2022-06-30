## Para ci/cd agregar webhooks en github

```
Payload URL: jenkinsURL + /github-webhook/
Content Type: application/json
Just the push event.
```

### Iniciar sesión en Heroku en la CLI

heroku login

```

<details>
<summary style="font-size:30px">DEPLOY WITHOUT MANIFEST</summary>
<blockquote>
### Inicia sesión en el aspecto contenedor de Heroku.

```

heroku container:login

```

### Crea aplicacion en heroku

```

heroku create -a HEROKU_APP_NAME

```

### Add heroku git remote

```

heroku git:remote -a HEROKU_APP_NAME

```

### Establezca la pila de su aplicación en container

```

heroku stack:set container

```

### Comprometerse heroku.yml con git:

```

git add heroku.yml
git commit -m "Added heroku.yml"

```

### Empuje su aplicación a Heroku

```

git push heroku <BRANCH>

```

</blockquote>
</details>

<details>
<summary style="font-size:30px">DEPLOY WITH MANIFEST</summary>
<blockquote>

### Inicia sesión en el aspecto contenedor de Heroku.

```

heroku container:login

```

### Para crear una aplicación desde la setup sección definida en su heroku.yml manifiesto, instale el heroku-manifest complemento desde el betacanal de actualización:

```

heroku update beta
heroku plugins:install @heroku-cli/plugin-manifest

```

### Puede volver al flujo de actualización estable y eliminar el complemento en cualquier momento:

```

heroku update stable
heroku plugins:remove manifest

```

### Luego crea tu aplicación usando la --manifest bandera. La pila de la aplicación se establecerá automáticamente en container:

```

heroku create --manifest

Creating ⬢ HEROKU_APP_NAME... done, stack is container
Adding heroku-postgresql... done
Setting config vars... done

```

### Comprometerse heroku.yml con git:

```

git add heroku.yml
git commit -m "Added heroku.yml"

```

### Empuje el código:

```

git push heroku <BRANCH>

```

</blockquote>
</details>
```
