# Conceptos claves 

- JSX:              extension que hace referencia a Javascript y XML, un sistema de plantillas. Por medio de esto, podemos utilizar una serie de elementos que conforman nuestro proyecto en HTML y CSS para llevarlo a JavaScript.

- Virtual DOM:      es una representacion del DOM real donde se aplicaran los cambios de nuestro desarrollo sin que afecte la funcionalidad de las URLs que manipulamos.

- Ciclo de Vida:    es el periodo de tiempo del proyecto en el que se cumple la funcionalidad de los elementos, componentes que usaremos.

- Estado:   

- Eventos:          es la funcion que necesitaremos que se ejecute en nuestro proyecto.

- Hooks:            es un recurso para optimizar el desarrollo con el uso de las herramientas anteriormente mencionadas.

# ##### FIN     VIDEO 2

# ##### INICIO  VIDEO 3

# Instalacion

- Creamos la carpeta en la que se ubicara nuestro proyecto.
- Inicializamos con git nuestro repositorio local.
- Inicializamos nuestro proyecto con

#   $ npm init

- Instalaremos un par de dependencias con los siguientes nombres y comandos

    react
    react-dom
#   $ npm install react react-dom

- Realizamos configuraciones en el sistema de directorios del proyecto creando las siguientes rutas:

/public
    /index.html
/src
    /index.js
    /components/
        App.jsx

# ##### FIN     VIDEO 3

# ##### INICIO  VIDEO 4

- Instalamos algunas dependencias de Babel en el proyecto con el siguiente comando:

#   $ npm install @babel/core @babel/preset-env @babel/preset-react

#   $ npm install webpack webpack-cli webpack-dev-server

#   $ npm install babel-loader html-loader html-webpack-plugin

- Se crearon los archivos en la carpeta raiz del proyecto

#   /.babelrc
```json
{
    "presets": [
        "@babel/preset-env",
        "@babel/preset-react"
    ]
}
```
#   /.gitignore
```txt
    node_modules
```
#   /webpack.config.js
```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
    entry: './src/index.js',
    output: {
        path: path.resolve(__dirname, 'dist'),
        filename: 'bundle.js'
    },
    resolve: {
        extensions: ['.js', '.jsx'],
    },
    module: {
        rules: [
            {
                text: /\.(js|jsx)$/,
                exclude: /node_modules/,
                use: {
                    loader: 'babel-loader'
                }
            },
            {
                test: /\.html$/,
                use: [
                    {
                        loader: 'html-loader'
                    }
                ]
            }
        ]
    },
    plugins: [
        new HtmlWebpackPlugin({
            template: './public/index.html',
            filename: './index.html'
        })
    ]
}
```

# ##### FIN     VIDEO 4

# ##### INICIO  VIDEO 5

- Agregamos un par de variables en la configuracion del webpack como:
```json
{
   "mode": "develop"
}
```

- Armamos nuestra plantilla html llamando en un div con el id="app" lo que renderizamos desde index.js

# ##### FIN     VIDEO 5

# ##### INICIO  VIDEO 6

- Instalamos herramientas para el manejo del css

#   $ npm install mini-css-extract-plugin css-loader style-loader sass -D

- Tambien, instalaremos:

#   $ npm install sass-loader

# ##### FIN     VIDEO 6

# ##### INICIO  VIDEO 7

- Para este video, implementamos plantillas preparadas para dicha practica en nuestro proyecto. Como lo hacemos?

- Creamos archivos scss y containers (jsx) para cada elemento de nuestra pagina que necesitemos.

# ##### FIN     VIDEO 7

# ##### INICIO  VIDEO 8

# ##### FIN     VIDEO 8

# ##### INICIO  VIDEO 9

- Para esta seccion, necesitaremos una herramienta para definir el sistema de rutas de nuestro proyecto. Para esto, instalaremos:

#   $ npm install react-router-dom

- Ya con esto, en nuestro archivo principal "App.jsx" usaremos la etiqueta <Route/> para definir las pantallas o las rutas que querremos visualizar y utilizar.

# #### FIN      VIDEO 9

# #### INCIO    VIDEO 10

-   

# #### FIN      VIDEO 10

# #### INCIO    VIDEO 11

# #### FIN      VIDEO 11

# #### INCIO    VIDEO 12

