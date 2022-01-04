JSX
Es la extensión de archivos que se usa en react donde podemos hacer html dentro de js facilitando el uso sacando lo mejor de html css y js.

Virual DOM
Es una copia del DOM real y lo que hace es compararlo, asi cuando existe algun cambio no se tiene que renderizar toda la pantalla si no solo lo que se cambio mejorando el desempeño de nuestra app, como lo comente antes esto es por que se compara el Virtual DOM con el DOM Real encontrando los cambios

Ciclo de vida
Este concepto es ampliamente conocido en la programación, en este curso vamos a conocer cual es el ciclo de vida de los elementos que vamos a crear en react desde que nace, se combina hasta que muere

Estado
Esto es fundamental, ya que podemos ver los estados y ver como es el flujo de la información entre componentes a travez de un imputs, botones, interacciones entre otros elementos

¿Qué es router en React?
Debido a que React es de tipo SPA(single page application), no recarga la página cuando cambiamos de url. Sin embargo, router nos ayuda a crear otra página para poder navegar en nuestra aplicación. Imagina twitter web, cuando das click en un tweet, se abre otra sección donde puedes ver el tweet. Sería un problema que al momento de darle click, no cambie la url, por lo que ese tweet no tiene dirección propia, no se guardaría en tu historial y sería un problema el SEO. Para ello, usamos router, que se encargará de administrar esta situación, donde en el momento que abras el tweet, cambie la URL, pero todavía mantenga ese dinamismo y rapidez de una SPA.

¿Entonces qué es ReactRouterDOM?
* Para instalar 

#   $ npm install react-router-dom

```typescript
//import en App.jsx
import { BrowserRouter, Switch, Route } from 'react-router-dom';
// usaremos esas 3 herramientas
```

ReactRouterDOM te permite implementar enrutado dinámico en la aplicación. Nos facilita pues podemos enrutar nuestra app basada en componentes de la app (como login o recoverypassword).

```typescript
const App = () => {
    return (
        <BrowserRouter>
            <Switch>
                <Layout>
                    <Route exact path="/" component={Home} />
                    <Route exact path="/login" component={Login} />
                    <Route exact path="recovery-password" component={Recoverypassword} />
                    <Route component={NotFound} />
                </Layout>
            </Switch>
        </BrowserRouter>
    );
}
```

¿Qué estamos haciendo?
BrowserRoute sirve para implementar router en el navegador

Switch regresa la primera ruta que coincida. En pocas palabras, si estamos en www.platzi.com/contacto , regresará el componente que coincida a este (es decir, el componente que contenga la lógica de contacto). En esta caso, estamos poniendo varios routes dentro de switch, ¿para qué? para que solamente traiga esa misma ruta, y no tenga que buscar más. Como si fuese un condicional switch de javascript efectivamente. Y por ello tenemos un route sin path, que será el valor por defecto.

Layout solamente renderizará el route que coincida efectivamente con la URL especificada.

