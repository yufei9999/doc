# Política de privacidad de Floatage

Fecha de entrada en vigor: 6 de noviembre de 2026
Última actualización: 6 de noviembre de 2026

Floatage (en adelante «la App») es una aplicación de notas que funciona únicamente en su dispositivo. Usted anota una idea en el momento en que se le ocurre y más tarde le añade ampliaciones, de modo que cada entrada va formando su propia línea temporal. Esta política describe qué información trata realmente la App y cómo se guarda. Le rogamos que la lea antes de empezar a utilizar la App.

## 1. Qué información almacena la App

Todo lo que usted escribe o dicta en la App se guarda en su dispositivo, en concreto:

- el título y el cuerpo de cada entrada (el cuerpo también se usa para generar el resumen de la lista);
- las ampliaciones que añada a una entrada, junto con su fecha y hora;
- la marca de estado de cada entrada y si está fijada;
- las fechas de creación y modificación de las entradas y de sus ampliaciones.

La App también conserva localmente una copia de seguridad de los datos anteriores, utilizada para recuperarlos si el archivo de datos principal se corrompe (véase la sección 2).

La App no recopila el modelo del dispositivo, la versión del sistema operativo, identificadores del dispositivo (IDFV o IDFA), datos de ubicación, contactos, fotografías, cámara, datos de salud ni información de pago. La entrada de voz no crea archivos de audio ni conserva grabaciones: solo se guarda el texto reconocido como contenido de la entrada, y tampoco registra su comportamiento de uso ni las rutas de navegación.

## 2. Dónde se almacena su información

Las entradas se guardan como un archivo JSON dentro del espacio de almacenamiento propio de la App (Application Support/Flit), junto con una copia de seguridad `.bak`. Al guardar, la App escribe primero un archivo temporal y luego sustituye el archivo principal de forma atómica, para reducir el riesgo de corrupción si se interrumpe la escritura; si no puede leer el archivo principal, intenta restaurarlo desde la copia de seguridad.

La App no dispone de servidor: no carga, transmite ni sincroniza estos contenidos con ningún servicio en la nube ni con terceros. No podemos ver, leer ni recuperar sus entradas.

## 3. Acceso a la red, exportación y uso compartido

La App no realiza ninguna solicitud de red ni utiliza ningún servidor. No contiene código de red y la app compilada tampoco se enlaza con los frameworks de red de Apple, por lo que sus entradas nunca se suben, transmiten ni sincronizan en ningún sitio.

Todas las funciones se pueden usar sin conexión a la red, incluida la entrada de voz: el habla se reconoce en su dispositivo y el texto reconocido se escribe únicamente en el archivo de datos local. La disponibilidad de la entrada de voz depende de que el sistema tenga recursos de dictado para su idioma y de que el dictado del sistema esté activado; si falta cualquiera de las dos cosas, la entrada de voz se desactiva y la App muestra un aviso de que el reconocimiento de voz en el dispositivo no está disponible en ese momento y le sugiere revisar los ajustes de dictado del sistema o usar el teclado. Puede seguir escribiendo con el teclado, y la App nunca cambia a un método de reconocimiento que necesite conexión a la red.

La versión actual no ofrece funciones de exportación ni de uso compartido, y no entrega contenido a otras apps mediante la hoja de compartir de iOS. Si una versión futura las añade, lo explicaremos antes de usarlas y actualizaremos esta política.

Que una copia de seguridad del dispositivo iOS (copia de iCloud o del ordenador) incluya los archivos de registro del sandbox de la App depende de los ajustes de copia de seguridad de su sistema. Esa copia la realiza una función del sistema de Apple y no está relacionada con la App.

## 4. Permisos del sistema y acceso al dispositivo

La entrada de voz es la única función que necesita un permiso. La primera vez que pulse el botón de entrada de voz, iOS le preguntará si la App puede usar el micrófono; según la API del sistema que utilice la App, es posible que iOS muestre también una solicitud de autorización para el reconocimiento de voz. La App no solicita permisos de notificaciones, fototeca, cámara, ubicación, contactos ni datos de salud, ni accede a ellos.

### Micrófono y entrada de voz

- Para qué se usa: la App convierte lo que usted dice en el texto de una entrada, que puede editar antes de guardarla. El texto reconocido se escribe únicamente en el archivo de datos local de la App (cards.json); no se crea nada más.
- Cuándo se solicita: solo la primera vez que utiliza la entrada de voz. La App no activa el micrófono al iniciarse ni en segundo plano, y la grabación se detiene en cuanto termina el dictado, sale del editor o cierra la App.
- El audio no se guarda ni se envía: la App no crea ningún archivo de audio ni conserva grabaciones. La entrada de voz utiliza el reconocimiento de voz del propio dispositivo, por lo que el audio se procesa solo en su dispositivo: no se envía a servidores de Apple ni a nosotros, y el texto reconocido permanece en el archivo de datos local de su dispositivo. Para ello se necesitan recursos de dictado para su idioma en el sistema y que el dictado del sistema esté activado; si no es así, la entrada de voz se desactiva y la App muestra un aviso de que el reconocimiento de voz en el dispositivo no está disponible en ese momento y le sugiere revisar los ajustes de dictado del sistema o usar el teclado. Nunca recurre a un método de reconocimiento que necesite conexión a la red.
- Si no concede el permiso: el resto de funciones sigue disponible y podrá seguir añadiendo y editando entradas con el teclado. Puede conceder el permiso más adelante en los Ajustes de iOS o revocarlo en cualquier momento; en tal caso la entrada de voz dejará de funcionar.

Si una versión futura incorpora alguna función que necesite otro permiso, mostraremos la solicitud estándar de iOS antes del primer uso, explicaremos para qué sirve y actualizaremos esta política en esta misma página. Puede revocar en cualquier momento los permisos concedidos desde los Ajustes de iOS; en tal caso, la función correspondiente podría dejar de estar disponible.

## 5. Conservación y eliminación

- Las entradas permanecen en su dispositivo hasta que usted las elimine.
- Puede eliminar una entrada completa dentro de la App, así como eliminar por separado cada ampliación de una entrada.
- Si desinstala la App en iOS, también se eliminarán el archivo de datos principal y el archivo de copia de seguridad del espacio de almacenamiento de la App.
- La eliminación no se puede deshacer. Dado que los datos solo existen en su dispositivo y la App no ofrece función de exportación, no podemos recuperarlos por usted; elimine con cuidado.

## 6. SDK de terceros, analítica y publicidad

La App no incluye ningún SDK de terceros: ni de analítica, ni de publicidad, ni de atribución, ni de informes de fallos. No contiene publicidad, no le rastrea entre aplicaciones ni sitios web, no utiliza IDFA y no solicita autorización de App Tracking Transparency. Que los diagnósticos y registros de fallos del sistema se envíen a Apple depende de la opción que usted elija en Ajustes de iOS > Privacidad y seguridad > Análisis y mejoras, y es ajena a la App.

## 7. Privacidad de los menores

La App no está diseñada para menores y no recopila datos personales de nadie. Como todas las entradas se guardan únicamente de forma local en el dispositivo, nunca obtenemos, almacenamos ni compartimos nada de lo que escriba un menor. Si usted es padre, madre o tutor legal y cree que existe algún problema, póngase en contacto con nosotros mediante los datos que figuran más abajo.

## 8. Cambios en esta política

Cuando modifiquemos esta política, actualizaremos la fecha de «Última actualización» que figura al inicio de esta página. Si el cambio afecta a la forma en que se trata su información, lo indicaremos en la App o en las notas de la versión publicadas en el App Store. Si sigue utilizando la App después de que un cambio entre en vigor, se entenderá que acepta la política actualizada.

## 9. Cómo contactarnos

Si tiene preguntas sobre esta política o desea ejercer algún derecho en relación con sus datos, puede contactarnos en:

- Correo electrónico de contacto: yufei.cjn@outlook.com
