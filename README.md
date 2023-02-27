[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=10267424&assignment_repo_type=AssignmentRepo)
# Tiro parabólico: TDD+Java+Maven+JUnit 4
### Ejemplo de TDD para la asignatura Desarrollo Ágil.
Ejemplo que servirá de base para un ejercicio de TDD en el que se use Java, Maven JUNit4 y VS Code.

Este ejemplo muestra cómo podemos calcular las fórmulas involucradas en un tiro parabólico en el que solo afecta la gravedad, dado que no introducimos ni coeficiente de rozamiento ni ninguna otra fuerza que afecte a la trayectoria.

Las fórmulas están calculas siguiendo las indicaciones encontradas en: https://www.areaciencias.com/fisica/tiro-parabolico-formulas/ 

### Creación del proyecto desde el código descargado de GitHub
Para poder usar la plantilla del proyecto y hacer los ejercicios, es impresincidible que tengas instalado algún JDK en tu ordenador. Además, tendrás que instalar en VS Code la extensión denominada: **Extension Pack for Java**, la cual nos instalará las siguientes 6 extensiones:
    * Language Support for Java™ by Red Hat
    * Debugger for Java
    * Test Runner for Java (Run & Debug JUnit/TestNG Test Cases)
    * Maven for Java
    * Project Manager for Java
    * Visual Studio IntelliCode

Una vez instalado todo el software necesario, clona el repositorio donde está la plantilla para los ejercicios y modifica los ficheros: *src/main/java/es/ujaen/dagil/App.java* y *src/test/java/es/ujaen/dagil/AppTest.java* para ir realizando los ejercicios indicados en los comentarios.

### Magdalena Bueno Pedrera
Estudiante de Ingeniería Informática en la Universidad de Jaén.
* **Correo**: mmbp0003@red.ujaen.es


###Comenzare enseñando los expect desde la función de calcular_T_dado_X
--------------------------------------------------

assertEquals(0, App.calcular_T_dado_X(-10, 26, Math.toRadians(40), -10), 0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:59703' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 0.0

---------------------------------------------------


assertEquals(3.41, App.calcular_T_dado_X(0, 26, Math.toRadians(40), 67.86), 0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:59773' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 3.4071130251572472

----------------------------------------

assertEquals(3.41, App.calcular_T_dado_X(-13, 26, Math.toRadians(40), 67.86 - 13), 0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:59931' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 3.4071130251572472

----------------------------

assertEquals(3.41, App.calcular_T_dado_X(22, 26, Math.toRadians(40), 67.86 + 22), 0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:59982' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 3.4071130251572472


--------------------------

assertEquals(10, App.calcular_Y_dado_T(10, 29, 0, -9.81, 0), 0);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60063' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 10.0

-------------------------

assertEquals(4, App.calcular_Y_dado_T(4, 12, 0, -9.81, 0), 0);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60127' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 4.0

-----------------------

assertEquals(14.23, App.calcular_Y_dado_T(0, 26, Math.toRadians(40), -9.81, 3.41/2), 0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60187' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 14.235817112404288

----------------------

assertEquals(14.23+10, App.calcular_Y_dado_T(0+10, 26, Math.toRadians(40), -9.81, 3.41/2), 0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60240' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 24.235817112404284

---------------------

assertEquals(14.23-10, App.calcular_Y_dado_T(0-10, 26, Math.toRadians(40), -9.81, 3.41/2), 0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60287' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
Deberia valer : 4.235817112404288

-------------------

assertEquals(10, App.calcular_Y_dado_X(5, 10, 2, 0, 0, 5),0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60348' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 10.0

------------------

assertEquals(14.23, App.calcular_Y_dado_X(0, 0, 26, Math.toRadians(40), -9.8, 67.73/2),0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60398' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 14.250227303215516

------------------

assertEquals(14.23, App.calcular_Y_dado_X(0, 0, 26, Math.toRadians(40), -9.8, 67.73),0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60443' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 0.16869119322488046

-----------------

assertEquals(14.23, App.calcular_Y_dado_X(0, 10, 26, Math.toRadians(40), -9.8, 67.73),0.1);

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60497' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
###Deberia valer : 10.16869119322488

-----------------

assertTrue(App.impacta_en_muro(0,0,26,Math.toRadians(40),-9.8,67.73/2,15));

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60624' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App' 
Este programa calcula si un tiro parabólico impacta en un muro o no
Introduce velocidad del disparo:
26
Introduce ángulo de disparo (entre 0 y 90):
40
Introduce distancia a la que está el muro:
33.865
Introduce altura del muro:
15
###Sí impacta en el muro

---------------------

assertFalse(App.impacta_en_muro(0,0,26,Math.toRadians(40),-9.8,67.73/2,13));

PS C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003>  c:; cd 'c:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003'; & 'C:\Program Files\Java\jdk-11.0.13\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:60695' '-cp' 'C:\Users\user\Desktop\Practica_2b\dagil-2022-2023-practica-2b-Mmbp0003\target\classes' 'es.ujaen.dagil.App'
Este programa calcula si un tiro parabólico impacta en un muro o no
Introduce velocidad del disparo:
26
Introduce ángulo de disparo (entre 0 y 90):
40
Introduce distancia a la que está el muro:
33.865
Introduce altura del muro:
13
###No impacta en el muro




















































