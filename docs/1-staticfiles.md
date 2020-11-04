# Leccion 1

El objetivo de esta leccion es comenzar un proyecto en NEST y poder proveer archivos estaticos

Instalar Nest CLI Tool en el sistema:

`npm i -g @nestjs/cli`

Crear el proyecto:

`nest new nest-demo`

Entrar a la carpeta del proyecto:

`cd cfp-demo`

Commit del proyecto inicial:

```
git add .
git commit -m "Initial Project commit"
```

Ahora intentar levantarlo:

`npm run start:dev`

y entrar a [http://localhost:3000](http://localhost:3000)

`npm install --save @nestjs/serve-static`

En `app.controller.ts` Cambiar la ruta del controlador: `@Controller('api')`.

En `app.module.ts` agregar 
```js
 [
    ServeStaticModule.forRoot({
      rootPath: join(__dirname, '..', 'client'),
    }),
  ],
```

Crear la carpeta para archivos estaticos: `client`.

