#   VIDEO 5

- Al buscar correr el comando 

#   $ npm run start

- Se presenta el siguiente mensaje en consola:

```c#
> react-shop@1.0.0 start /home/andres/personal/curso-practico-reactjs-platzi/react-shop
> webpack serve --open

[webpack-cli] /home/andres/personal/curso-practico-reactjs-platzi/react-shop/node_modules/webpack-dev-server/lib/servers/WebsocketServer.js:10
  static heartbeatInterval = 1000;
                           ^

SyntaxError: Unexpected token =
    at Module._compile (internal/modules/cjs/loader.js:723:23)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:789:10)
    at Module.load (internal/modules/cjs/loader.js:653:32)
    at tryModuleLoad (internal/modules/cjs/loader.js:593:12)
    at Function.Module._load (internal/modules/cjs/loader.js:585:3)
    at Module.require (internal/modules/cjs/loader.js:692:17)
    at require (internal/modules/cjs/helpers.js:25:18)
    at Server.getServerTransport (/home/andres/personal/curso-practico-reactjs-platzi/react-shop/node_modules/webpack-dev-server/lib/Server.js:1670:28)
    at Server.createWebSocketServer (/home/andres/personal/curso-practico-reactjs-platzi/react-shop/node_modules/webpack-dev-server/lib/Server.js:2452:57)
    at Server.start (/home/andres/personal/curso-practico-reactjs-platzi/react-shop/node_modules/webpack-dev-server/lib/Server.js:3238:12)
npm ERR! code ELIFECYCLE
npm ERR! errno 2
npm ERR! react-shop@1.0.0 start: `webpack serve --open`
npm ERR! Exit status 2
npm ERR! 
npm ERR! Failed at the react-shop@1.0.0 start script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     /home/andres/.npm/_logs/2021-12-28T11_45_47_532Z-debug.log
```

# #######################
#       SOLUCION
# #######################

- Actualizar a la version mas reciente de nodeJs.

# ******************************************************************************************************************
# ******************************************************************************************************************
# ******************************************************************************************************************

- Se presenta el siguiente error en consola:

```c#
Compiled with problems:X

ERROR in ./src/styles/global.css 1:0

Module parse failed: Unexpected token (1:0)
You may need an appropriate loader to handle this file type, currently no loaders are configured to process this file. See https://webpack.js.org/concepts#loaders
> :root {
|     --white: #FFFFFF;
|     --black: #000000;
```

# #######################
#       SOLUCION
# #######################

- Mover las variables definidas en el ':Root' del scss de global a un archivo container llamado '_vars' e importar dicho archivo en donde se esten utilizando estas variables definidas.

# ******************************************************************************************************************
# ******************************************************************************************************************
# ******************************************************************************************************************

- Se presenta un error en la pagina sobre una dependencia, pues los paquetes de la clase Switch ya no los traen las versiones recientes de react-routes-dom, se debe instalar una version anterior para utilizar estos paquetes de dicha dependencia.

#   $ npm install react-router-dom@5.2.0

# #######################
#       SOLUCION
# #######################