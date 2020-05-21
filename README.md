<h1 align="center">Conceptos Front End</h1>
Conceptos usados en el track de Front End.

---

## Compilar
Compilar es el proceso de transformar un programa informático escrito en un lenguaje en un programa equivalente en otro formato. Al programa que se encarga de compilar se le llama `compilador`. A veces, a esta tarea se le llama "ensamblar" o "construir", lo que suele implicar otros procesos adicionales, e.j. empaquetarlo en formato binario.

## Transpilador
Programas que traducen un lenguaje a otro del mismo nivel. Ejemplo: Al compilar de TypeScript a JavaScript. 

---

## ¿Qué licencia elegir para tu software?
A grandes rasgos existen dos tipos de licencias: las de Copyright y las Open Source(Copyleft). No elegir una licencia para nuestro proyecto no es una buena práctica.

Si no hubiera licencia alguna en tu proyecto, significaría que automáticamente se aplicarían las leyes de derechos de autor. Es decir, conservarías todos los derechos sobre el código fuente y nadie más podrá reproducir, distribuir o crear trabajos derivados de tu proyecto.

Pudiera parecer que el Copyright por defecto es la opción más cómoda y directa; sin embargo, no es así exactamente. De hecho, la ausencia de licencia es perjudicial para el ecosistema comercial del software, por la falta de control. Así, las empresas no quieren saber nada de software sin licenciar, y se pierde mucho, mucho dinero por el camino.

Sea como fuere, infórmate y licencia tu software. Y si no te importan estos temas ni lo que puedan hacer otros con tu software, para ello existe la Licencia MIT.

### Conceptos:

- Copyright: 
En español `Derechos de autor`. Esto le proporciona al responsable de un contenido artístico o de una obra intelectual un derecho de autor cada vez que sea reproducido o utilizado, participando por ley en los posibles beneficios que genere su trabajo.

- Copyleft:
Práctica legal que consiste en el ejercicio del derecho de autor con el objetivo de propiciar el libre uso y distribución de una obra, exigiendo que los concesionarios preserven las mismas libertades al distribuir sus copias y derivados.


### Recursos:
- Para poder elegir la licencia adecuada, Github nos ofrece la siguiente guía: https://choosealicense.com/.
- [Agregar una licencia a tu repositorio](https://help.github.com/es/github/building-a-strong-community/adding-a-license-to-a-repository)
- [Cómo elegir la licencia correcta para tu proyecto Open Source](https://hipertextual.com/archivo/2014/05/como-elegir-licencias-open-source/)
- [¿Sabes bien qué licencia elegir para tu software?](https://www.muylinux.com/2013/07/18/eleccion-licencia-software/)

---

## Añadiendo insignias a nuestro README

Las insignias en nuestro README podrían indicar datos como el número de descargas, el estado de la build, la cobertura de los tests, etc.

#### Ejemplos de insignias:
<p align="center">
  <img src="https://img.shields.io/badge/build-passing-brightgreen">
  <img src="https://img.shields.io/badge/npm-v15.5.6-9cf">
</p>

`build`: Indica el estado de la compilación.

En nuestro ejemplo, indica que la compilación está "pasando" (comúnmente significa que las pruebas pasan y nada explotó durante la compilación más reciente).

### Recursos

- Página para crear insignias: https://shields.io/
- [Enriqueciendo el README con Shields.io](https://www.ikeinyyo.com/shields-io-enriqueciendo-nuestro-readme-md/)

---

## Testing en el desarrollo de software

 Es el proceso de comprobar que tu aplicación funciona correctamente, con el fin de obtener información acerca de su calidad.
 
 ### Tipos de pruebas
 
 #### Según la ejecución o no del código:
 
 - Estáticas: Se realizan sin necesidad de ejecutar el código. Un ejemplo de este tipo de pruebas puede ser la revisión estática de código, es decir, analizar el código fuente de una aplicación en busca de defectos, de algún tipo de patrones incorrectos y demás.
 
 - Dinámicas: Se realizan ejecutando el software para poder probarlo. Por ejemplo, pruebas funcionales.
 
 #### Según el uso de herramientas:
 
 - Manuales: Se prueba una navegación normal. Por ejemplo, acceder a la aplicación y pulsar los botones para comprobar si funciona o no.
 
- Automáticas: Se utiliza una o varias herramientas para realizar estas pruebas.

 #### Según lo que verifican:
 
 - **Pruebas funcionales:** Revisan el comportamiento del sistema, subsistema o componente software. Entre las más importantes tenemos:
 
      - Pruebas unitarias: Prueba trozos de código concretos para ver que funciona y que no tiene errores.
      - Pruebas de integración: Prueba a todos los componentes juntos, para ver cómo interactúan entre ellos y comprobar que todo vaya bien.
      - Pruebas de aceptación: Las realiza el usuario. Puede que un software no contenga errores, que funcione bien, pero tal vez no hace lo que debería hacer, no está haciendo lo que el usuario quería que hiciese.
      - Pruebas de regresión: Verifican un conjunto de escenarios que funcionaron correctamente en el pasado, para asegurar que continúen así. Una falla en una prueba de regresión significa que una nueva funcionalidad ha afectado otra funcionalidad que era correcta en el pasado, causando una "regresión".
    
- **Pruebas no funcionales:** Consideran el comportamiento externo del sistema. Hay varios tipos:

     - Pruebas de seguridad: Buscan vulnerabilidades de seguridad (hacking ético).
     - Pruebas de rendimiento: Permiten conocer el comportamiento del software ante una carga determinada, cómo responde y cómo se recupera ante fallos.
     - Pruebas de usabilidad: Permiten saber el nivel de usabilidad de la aplicación, pero sin entrar en aspectos funcionales. Por ejemplo, si tiene un menú que hace que la navegación sea intuitiva, si tiene un contenido de ayuda que explica el funcionamiento de la aplicación, etc.
     - Pruebas de accesibilidad: Tienen por fin determinar la facilidad con la que se puede utilizar un sitio web. Por ejemplo, correcta visualización de los elementos, proveer alternativas de uso para personas con alguna discapacidad visual o auditiva, etc.
      
Tal vez hayas oído de las pruebas de caja blanca y de caja negra, pero lo que ocurre con las mismas es que no son tipos de pruebas, sino técnicas de pruebas de software.

### Cuando NO testear

Existe la posibilidad de que desarrollar pruebas automáticas haga más lenta tu experiencia de desarrollo. Recordemos que el propósito de las pruebas automáticas es ahorrar tiempo.

### En resumen

   - No siempre hace falta tener pruebas automáticas 🤔
   - No necesitas tests si pasas más tiempo re-escribiendo tests que desarrollando funcionalidades.
   - Tu objetivo no es obtener el 💯% de cobertura en tus tests 🚫. 
   - No eres mejor tester por tener todo al 💯%.
   - TDD es bueno. TDD estricto y a rajatabla puede ser un dolor de cabeza.

 ### Recursos

 - [Tipos de testing en el desarrollo de software](https://programacionymas.com/blog/tipos-de-testing-en-desarrollo-de-software)
 
 ---
 
 
