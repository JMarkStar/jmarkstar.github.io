---
layout: default
title: Instalando Android Studio 3.1.2
description: Este artículo es el primero del curso de android básico. Aquí instalaremos y configuraremos de manera rápida android studio 3.1.2 para poder comenzar a codear.
cover: cover.jpg
date: 2018-05-04 15:07:00
categories: AndroidBasico
tags: [Android_basico]
---

## Instalando Android Studio 3.1.2

Si eres completamente nuevo en android y  quieres dar tu primer paso, este será un buen artículo para ti, ya que te ayudará a instalar y configurar android studio y crear un proyecto android para luego ejecutarlo en un emulador. Los pasos a seguir son:
* Instalar Java 10
* Configurar Java 10
* Instalar Android Studio 3.1.2
* Crear un proyecto Android
* Crear un emulador
* Ejecutar el proyecto en un emulador

Sin mas preámbulos, comencemos.

### Instalar Java 10

**Nota: Si ya tienes instalado el JDK 7, 8 o 9, puedes evitar este paso.**

El primer paso es descargar e instalar Java 10. **¿Por qué?**, Java es el lenguaje de programación escogido por Google para poder crear aplicaciones móviles para Android. Vamos a descargar el JDK de Java. **¿Qué es el JDK?**, es un conjunto de herramientas que nos permitirán programar con Java, entre ellos tenemos a la **JVM**(La máquina virtual de Java), **Librerías estándar** que serán usados con el lenguaje Java y más.

Nos dirigimos a la [página de Oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk10-downloads-4416644.html) para descargar el JDK(Java Development Kit).

Nos interesa esta sección de la página

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_java_1.png" width="400" title="Sección para descargar el JDK" alt="Sección para descargar el JDK"></p>

En primer lugar, tenemos que aceptar la licencia. Para ello, hacemos click en el RadioButton **Accept License Agreement**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_java_2.png" width="350" title="Aceptar la licencia" alt="Aceptar la licencia"></p>

Ahora ya podemos descargar el JDK :). Selecciona el JDK de acuerdo al sistema operativo que estás usando. En caso de este artículo seleccionaremos el de **Windows x64**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_java_3.png" width="400" title="Descargar el JDK de acuerdo a tu Sistema operativo" alt="Descargar el JDK de acuerdo a tu Sistema operativo"></p>

Una vez que hayas descargado el *\*.exe*. Solo debes de ejecutarlo y hacer click en los botones **next** hasta llegar a esta pantalla.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_java_4.png" width="350" title="Java fue Instalado" alt="Java fue Instalado"></p>

### Configurar Java 10

En este paso, vamos a añadir una nueva variable de entorno llamada **JAVA_HOME** en nuestro sistema operativo. Como valor, la variable tendrá ruta de la carpeta raíz donde esta instalado nuestro Java.

##### ¿Por qué debemos configurar la variable de entorno JAVA_HOME?
Si no configuramos el JAVA_HOME, no vamos a poder usar las herramientas que Java nos proporciona, desde cualquier ruta. Java tiene una serie de herramientas(**comandos**) que usaremos en un futuro al estar programando en Android como por ejemplo el **keytool**. Esta herramienta está en la ruta C:\Program Files\Java\jdk-10.0.1**\bin**. Por esta razón, es importante tener esta variable siempre disponible.

Si aún no lo hemos configurado y ejecutamos el comando para ver la versión de Java que tenemos instalado: **java -version**, nuestro Windows no lo reconocerá. Probemos.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_1.png" width="400" title="Windows no reconoce el comando Java" alt="Windows no reconoce el comando Java"></p>

Para configurar una variable de entorno, tenemos que seguir los siguientes pasos:

Hacer click derecho en **Este equipo**, para luego hacer clic en **Propiedades**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_2.png" width="200" title="" alt=""></p>

Hacemos clic izquierdo en **Configuración avanzada del sistema**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_3.png" width="500" title="" alt=""></p>

Veremos la ventana de **Propiedades del sistema** y hacemos click en el botón **variables de entorno**:

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_4.png" width="350" title="" alt=""></p>

Una vez estando en la ventana de **Variables de entorno**, hacemos clic en **Nueva**, en la sección de Variables del sistema:

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_5.png" width="350" title="" alt=""></p>

Veremos una pantalla pequeña donde ingresaremos los datos de JAVA_HOME:
En Nombre de la variable ingresaremos **JAVA_HOME** y en Valor de la variable **La ruta de la carpeta donde instalamos Java**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_10.png" width="350" title="" alt=""></p>

Para ir a la ruta de instalación, nos dirigimos a **C:** -> **Archivos de programa** y **Java**. Si estamos en la carpeta Java veremos 2 carpetas, **Copiar la ruta de jdk-10.0.1**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_6.png" width="350" title="" alt=""></p>

Este es el resultado y **aceptamos**.
<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_7.png" width="350" title="" alt=""></p>

Ahora que ya hemos agregado la variable JAVA_HOME, buscamos la variable **Path**, lo seleccionamos y damos click en **Editar**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_8.png" width="350" title="" alt=""></p>

Ahora nos dirigimos al final del **valor de la variable** y añadimos **;%JAVA_HOME%\bin**.
<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_9.png" width="350" title="" alt=""></p>

**¿Por qué añadimos la carpeta bin?**, es porque las herramientas del JDK se encuentran en **bin**. Por ejemplo, allí se encuentra la herramienta **Java** que sirve para ejecutar programas en Java, la herramienta **keytool** que usaremos en un futuro para crear nuestro almacén de claves.
<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_11.png" width="450" title="" alt=""></p>

Por último, vamos a probar el comando **java -version** que en un principio Windows no reconoció:

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/config_java_12.png" width="350" title="" alt=""></p>

Ahora Windows reconoció el comando y nos dice que tenemos la versión **10.0.1**.

### Instalar Android Studio 3.1.2

Ahora que ya tenemos el JDK instalado en nuestra computadora, ya podemos instalar Android Studio sin problemas. Para ello, nos dirigimos a la [página oficial](https://developer.android.com/studio/) y veremos un botón **Descargar Android Studio**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_1.png" width="500" title="" alt=""></p>

Hacemos clic para descargar el ejecutable *\*.exe* y veremos que Google nos muestra la licencia, **aceptamos** y **descargamos**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_2.png" width="500" title="" alt=""></p>

Ahora que ya tenemos el *\*.exe* en nuestra computadora, lo ejecutamos y hacemos clic en **next** y **next** hasta llegar a la pantalla final de instalación:

Primera pantalla del ayudante de instalación:
<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_3.png" width="400"></p>

 Click para iniciar la instalación:
<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_4.png" width="400" title="Inicio de la instalación" alt="Inicio de la instalación"></p>

Fin de la instalación:

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_5.png" width="400" title="Fin de la instalación" alt="Fin de la instalación"></p>

Si es una instalación nueva, selecciona la última opción y acepta, ya que no tienes la necesidad de importar las configuraciones de algún antiguo android studio que tenías instalado.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_6.png" width="400"></p>

Ahora nos aparecerá un wizard para configurar el **Android SDK**  en android Studio.

**Nota: Android Studio en palabras sencillas es un editor pero para poder compilar, ejecutar, debuggear, probar nuestro app necesitamos en Android SDK, este contiene todas las herramientas para el desarrollo de apps.**

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_7.png" width="400"></p>

Seleccionamos el tipo de configuración que deseamos hacer. Recomiendo dejarlo en una instalación de tipo **Standard**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_8.png" width="400"></p>

Ahora, seleccionamos el Tema del IDE, podemos seleccionar el que mas nos guste. En mi caso el **Darcula**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_9.png" width="400"></p>

En esta ventana configuraremos el  **Android SDK**, si ya tenemos alguno instalado, en wizard lo detectará automáticamente pero si no, tenemos que indicarle la ruta donde queremos instalar nuestro SDK.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_13.png" width="400"></p>

Finalizamos para descargar, instalar y configurar las opciones seleccionadas anteriormente.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_10.png" width="400"></p>

Ya hemos instalado los componentes necesarios para que android studio funcione correctamente, ahora solo finaliza.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_11.png" width="400"></p>

Ya tenemos nuestro Android Studio listo para crear nuestro primer proyecto.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/install_android_12.png" width="400"></p>

### Crear un proyecto Android

Después de haber instalado correctamente Android Studio, haremos click en el botón **Start a new Android Studio Project** para comenzar a crear nuestro primer Android App.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_1.png" width="500"></p>

El siguiente paso es darle un nombre a nuestro proyecto en el campo **Application Name**. Después agregaremos nuestro **Company Domain**(nombre de dominio) o de la empresa para la cual trabajamos, en mi caso usaré mi dominio **jmarkstar.com**. Como podemos ver un campo más abajo se autogenera un valor de acuerdo lo que ingresos en los dos primeros campos, este vendría a ser el **nombre de paquete**. En caso de que el nombre autogenerado no te guste, puedes editarlo haciendo click en _**Edit**_. Luego, hacemos clic en el botón **Next**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_2.png" width="500"></p>

Este paso es para seleccionar los dispositivos donde queremos que se ejecute nuestro App. Por defecto ya está para **Smartphones y Tabletas**.  Ahora tenemos que seleccionar para que versión de Android queremos que corra nuestro App, para eso hacemos clic en **Help me choose**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_3.png" width="500"></p>

Nos abrirá otra ventana donde veremos una lista de versiones de android. Por el momento, seleccionaremos la versión **4.4 Kitkat** y hacemos clic en **OK**. Para luego con  **Next** ir al siguiente paso.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_4.png" width="500"></p>

Cuando creamos un proyecto Android, este ya viene con una pantalla por defecto. Por ahora solo escogeremos que la pantalla esté vacía; Clicamos en **Empty Activity** y vamos a siguiente paso clicando en el botón **Next**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_5.png" width="500"></p>

Aquí le daremos nombre a esa pantalla por defecto. Para entender un poco sobre los datos que estamos ingresando, explicaré un poco de las pantallas en Android.

Básicamente a una pantalla en Android esta representada por un **Activity**, este activity gestiona todo el comportamiento de una pantalla y comúnmente esta dividido en dos partes: en un archivo **\*.java** y un **\*.xml**. El archivo **\*.xml** tiene el diseño de la pantalla (las cajitas de texto, los botones, etc.) y el archivo **\*.java** llama a estos componentes de vista y les da comportamiento, aquí es donde usamos Java para programar.

Regresando a la imagen. Existen dos campos importantes, el **Activity Name** es para darle nombre al archivo **\*.java** y el campo **Layout Name** es para darle nombre al archivo **\*.xml**. Podemos dejarlo con los nombres por defecto si deseamos y hacemos click en  **Next** o **Finish** dependiendo del caso.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_6.png" width="500"></p>

En caso de que sea la primera vez que se crea un proyecto, posiblemente se muestre esta pantalla. Lo que hace es descargar las librerías necesarias para el proyecto.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_7.png" width="500"></p>

En caso de que sea la primera vez se descargará  [Gradle](https://gradle.org/), que es la herramienta para hacer **Build** nuestro proyecto.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_8.png" width="500"></p>

Ya tenemos nuestro primer proyecto creado.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_project_9.png" width="600"></p>

### Crear un emulador

Ahora que ya hemos creado nuestro primer proyecto, supongo que querras probarlo. Para ello vamos a crear un emulador android. **¿Qué es un emulador Android?**, este simula un dispositivo real en nuestra computadora, le podemos instalar y desinstalar los Apps que querramos.

La idea es correr nuestro proyecto en este emulador.

Primero, hacemos click en el botón **AVD Manager**; que es el botón donde la flecha esta señalando.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_1.png" width="500"></p>

**AVD** significa Dispositivo Virtual de Android, para saber más de ello entra a la [página oficial](https://developer.android.com/studio/run/managing-avds.html).

Continuando con los pasos, hacemos click en el botón **Create Virtual Device**.
<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_2.png" width="400"></p>

Seleccionamos un modelo de Smartphone y hacemos clic en **Next**. En mi caso seleccioné al **Galaxy Nexus**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_3.png" width="400"></p>

Ahora vamos a seleccionar la versión de Android que queremos para nuestro emulador. Si la instalación es nueva, tenemos que descargar uno de los emuladores, puedes escoger el que te guste, en mi caso, el **Nougat - V7.1.1**. Hacemos clic en **Download**

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_4.png" width="400"></p>

Aceptamos la licencia y hacemos clic en **Next**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_5.png" width="400"></p>

Esperamos que descarge, esto puede tarde un buen tiempo y le damos clic en **Finish**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_6.png" width="400"></p>

En este último paso, podemos agregar y quitar características al emulador, pero por el momento no haremos ningún cambio y hacemos clic en **Finish**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_7.png" width="400"></p>

Ahora, podemos ver nuestro primer emulador creado en una lista de emuladores. Nos dirigimos a ella y hacemos clic en el botón **Play**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_8.png" width="400"></p>

Esperamos un momento y veremos a nuestro primero emulador corriendo en nuestra computadora :).

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/creating_emulator_9.png" width="400"></p>

### Ejecutar el proyecto en un emulador

Ahora que ya tenemos nuestro proyecto creado y nuestro emulador funcionando, vamos a correr nuestro proyecto en el emulador haciendo clic en el botón **Run**.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/running_app_1.png" width="400"></p>

Como ya tenemos un emulador funcionando, este aparecerá en la lista de dispositivos conectados, lo seleccionamos y hacemos clic en **OK**:

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/running_app_2.png" width="400"></p>

Si es tu primera instalación probablemente te salga esta ventana.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/running_app_3.png" width="400"></p>

Es la ventana para instalar el [Instant Run](https://medium.com/google-developers/instant-run-how-does-it-work-294a1633367f).

**Nota: El Instant Run es una característica de Android Studio que reduce el tiempo de construcción y despliegue del APK en nuestro emulador.**

Esperamos que descargue las herramientas y hacemos clic en **Finish**

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/running_app_4.png" width="400"></p>

Esperamos un momento y nuestro primero proyecto se estará visualizando en el emulador.

<p style="text-align:center;"><img src="{{ site.baseurl_root }}/assets/img/android-basic-1/running_app_5.png" width="400"></p>

Espero que este artículo te haya sido de ayuda.

Gracias por la visita.

{% include comments.html %}