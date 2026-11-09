# Política de privacidad de Flit

Fecha de entrada en vigor: 6 de noviembre de 2026
Última actualización: 6 de noviembre de 2026

Flit (en adelante «la App») es una aplicación de notas que funciona únicamente en su dispositivo. Usted anota una idea en el momento en que se le ocurre y más tarde le añade ampliaciones, de modo que cada entrada va formando su propia línea temporal. Esta política describe qué información trata realmente la App y cómo se guarda. Le rogamos que la lea antes de empezar a utilizar la App.

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

Las funciones principales de la App funcionan completamente sin conexión, y sus entradas guardadas nunca se transmiten por la red. Para determinar si la red está disponible (por ejemplo, para mostrar un aviso cuando no hay conexión y actualizar la lista al recuperarla), la App:

- lee, mediante el framework Network de Apple, el tipo de conexión actual (Wi-Fi o datos móviles) y si esa conexión se factura por volumen o está en modo de bajo consumo de datos. Esta información se usa solo en su dispositivo y no se carga a ningún servidor.
- envía una única solicitud HTTPS GET a `https://captive.apple.com/hotspot-detect.html`, una dirección operada por Apple, y considera el éxito o el fallo como señal de accesibilidad. La solicitud utiliza una sesión efímera, no lleva cookies, no escribe caché y no contiene ninguna de sus entradas ni el texto que haya introducido en la App. Como ocurre con cualquier solicitud HTTPS, Apple, en calidad de operador de esa dirección, puede ver la dirección IP de origen y la información de red habitual necesaria para establecer la conexión; nosotros no recibimos ni almacenamos esa información.

Aparte de esta comprobación de conectividad, la App no envía datos al exterior por iniciativa propia.

La versión actual no ofrece ninguna función de exportación o uso compartido de entradas y tampoco entrega contenido a otras aplicaciones mediante el panel de compartir de iOS. Si una versión futura incorpora esa función, la explicaremos antes de su uso y actualizaremos esta política.

Que una copia de seguridad del dispositivo iOS (copia de iCloud o del ordenador) incluya los archivos de entradas del espacio de almacenamiento de la App depende de su configuración de copia de seguridad del sistema. Esa copia la realiza una función del sistema de Apple y es ajena a la App.

## 4. Permisos del sistema y acceso al dispositivo

La entrada de voz es la única función que necesita un permiso. La primera vez que pulse el botón de entrada de voz, iOS le preguntará si la App puede usar el micrófono; según la API del sistema que utilice la App, es posible que iOS muestre también una solicitud de autorización para el reconocimiento de voz. La App no solicita permisos de notificaciones, fototeca, cámara, ubicación, contactos ni datos de salud, ni accede a ellos.

### Micrófono y entrada de voz

- Para qué se usa: la App convierte lo que usted dice en el texto de una entrada, que puede editar antes de guardarla. El texto reconocido se escribe únicamente en el archivo de datos local de la App (cards.json); no se crea nada más.
- Cuándo se solicita: solo la primera vez que utiliza la entrada de voz. La App no activa el micrófono al iniciarse ni en segundo plano, y la grabación se detiene en cuanto termina el dictado, sale del editor o cierra la App.
- El audio no se guarda ni se envía: la App no crea ningún archivo de audio ni conserva grabaciones. La entrada de voz utiliza el reconocimiento de voz del propio dispositivo, por lo que el audio se procesa solo en su dispositivo: no se envía a servidores de Apple ni a nosotros, y el texto reconocido permanece en el archivo de datos local de su dispositivo. Si su dispositivo o su idioma no admiten el reconocimiento en el dispositivo, la App le indicará que la entrada de voz no está disponible o pasará a la entrada por teclado; nunca recurre a un servicio en la nube.
- Si no concede el permiso: el resto de funciones sigue disponible y podrá seguir añadiendo y editando entradas con el teclado. Puede conceder el permiso más adelante en los Ajustes de iOS o revocarlo en cualquier momento; en tal caso la entrada de voz dejará de funcionar.

Es posible que vea en los Ajustes de iOS un interruptor de «Datos móviles» para la App; se trata de un control general del sistema para las aplicaciones que usan la red, no de una solicitud de autorización de la App. Si lo desactiva, la App seguirá funcionando, pero puede que su comprobación del estado de la red deje de funcionar.

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

- Desarrollador: <开发者主体名称 / Developer Name>
- Correo electrónico de contacto: yufei.cjn@outlook.com
- Dirección postal: <通信地址 / Mailing Address> (elimine esta línea si no es obligatoria en su jurisdicción)
