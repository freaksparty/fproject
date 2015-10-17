#Cómo trabajar

Se debería de ejecutar un _npm install_ para instalar todas las dependencias (interesante hacerlo cada vez que se hace un pull, por si un compañero añadió alguna dependencia).

Si es la primera vez que se trabaja con él, hay que comprobar que esté grunt instalado, por lo que se debería de hacer como administrador:

    npm install -g grunt

Con todo esto listo, antes de empezar a trabajar deberíamos de ejecutar un _grunt watch_ y dejarlo corriendo en una terminal. Así, cada cambio que se haga en un jade, less o js automáticamente será transformado en html, css o minificado para javascript.

#Estructura de directorios

* **dev**: Aquí se desarrolla todo el código. Está dividido en carpetas según el tipo de elemento frontend, a saber: html, stilos css o javacript. En la parte de javascript está organizado según la estructura de angular.
* **publi**: Esta es la carpeta donde grunt compila los archivos y las rutas finales a las cuales hacer referencia desde el frontend. Será el código final al que accederá el cliente.

#Compilación stand-alone

Si se nos olvidó ejecutar el *watch* o queremos forzar el compilado de algún recurso, podemos hacerlo manualmente con grunt:

* **grunt less**: Compila todos los estilos y los situa en *public/css/styles.css*
* **grunt uglify**: Minifica todos los javascript y los situa en *public/js/scripts.js*
* **grunt jade**: Compila todos los jade según sus reglas tomando como base la carpeta *public*.

**Todas las reglas de grunt pueden ser consultadas o modificadas en Gruntfile.js. Es importante que, debido a que este archivo es muy importante para la generación de los ficheros, si se modifica se documente el cambio**
