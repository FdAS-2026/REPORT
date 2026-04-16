# Capítulo III: Requirements Specification

## 3.1 To-Be Scenario Mapping

### To-Be Scenario Mapping – Usuario Rural (OffGrid Messenger)

<img width="1561" height="502" alt="image" src="https://github.com/user-attachments/assets/ae4c5b19-29cd-478a-9f9a-e5ad557ec1ef" />

### To-Be Scenario Mapping – Equipo de Emergencia

<img width="1536" height="493" alt="image" src="https://github.com/user-attachments/assets/fb6e2e25-e445-4a88-901a-5626a9167d71" />

LINK MIROBOARD: https://miro.com/app/board/uXjVGh3DVhg=/?share_link_id=353512440400

## 3.2 User Stories

### Segmentos objetivo
- Usuarios en zonas rurales o con baja conectividad
- Usuarios en actividades outdoor (senderismo, camping, expediciones)
- Equipos de emergencia y contingencia

### Epics

| Epic ID | Título | Descripción |
|--------|--------|-------------|
| EP-01 | Comunicación LoRa | Como usuario en zonas sin cobertura móvil, quiero enviar y recibir mensajes mediante tecnología LoRa, para comunicarme a largas distancias sin usar internet. |
| EP-02 | Comunicación Bluetooth | Como usuario, quiero conectar mi celular por Bluetooth a un dispositivo LoRa, para poder transmitir mensajes desde la aplicación móvil. |
| EP-03 | Mensajería encriptada | Como usuario, quiero que mis mensajes estén cifrados, para asegurar la privacidad y seguridad de la información transmitida. |
| EP-04 | Gestión local de usuario | Como usuario, quiero tener una identidad local en la aplicación sin necesidad de servidor, para poder comunicarme sin depender de servicios externos. |
| EP-05 | Almacenamiento local encriptado | Como developer, quiero implementar una base de datos local en SQLite encriptada, para almacenar mensajes, usuarios y configuraciones de forma segura sin depender de la nube. |
| EP-06 | Landing Page informativa | Como visitante, quiero acceder a una landing page informativa, para conocer la propuesta de valor, funcionamiento y beneficios del sistema. |

| User Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
|---------------------|--------|-------------|--------------------------|---------------------------|
| US-01 | Enviar mensaje por LoRa | Como usuario, quiero enviar mensajes mediante tecnología LoRa, para comunicarme sin usar internet. | Escenario 1: Dado que el usuario está conectado a un dispositivo LoRa vía Bluetooth, Cuando redacta un mensaje y presiona enviar, Entonces el sistema transmite el mensaje mediante la red LoRa. Escenario 2: Dado que no existe conexión con el dispositivo LoRa, Cuando el usuario intenta enviar un mensaje, Entonces el sistema muestra un error indicando que no hay conexión disponible. | EP-01 |
| US-02 | Recepción de mensajes LoRa | Como usuario, quiero recibir mensajes desde la red LoRa, para mantener comunicación con otros usuarios. | Escenario 1: Dado que el dispositivo LoRa recibe un mensaje, Cuando el sistema procesa la señal, Entonces el mensaje se muestra en la aplicación. Escenario 2: Dado que el mensaje llega mientras la app está en segundo plano, Cuando el sistema lo recibe, Entonces se genera una notificación para el usuario. | EP-01 |
| US-03 | Comunicación a larga distancia | Como usuario, quiero comunicarme a larga distancia mediante LoRa, para usar el sistema en zonas remotas. | Escenario 1: Dado que existen nodos LoRa intermedios, Cuando el usuario envía un mensaje, Entonces el mensaje es retransmitido hasta llegar al destinatario. Escenario 2: Dado que no hay nodos disponibles, Cuando se envía el mensaje, Entonces el sistema indica que no se pudo completar la entrega. | EP-01 |
| US-04 | Confirmación de envío | Como usuario, quiero saber si mi mensaje fue enviado correctamente, para asegurar la comunicación. | Escenario 1: Dado que el mensaje se transmite correctamente, Cuando finaliza el envío, Entonces el sistema muestra el estado “enviado”. Escenario 2: Dado que ocurre un fallo en la transmisión, Cuando el sistema detecta el error, Entonces muestra el estado “fallido”. | EP-01 |
| US-05 | Recepción en segundo plano | Como usuario, quiero recibir mensajes aunque no esté en la pantalla principal, para no perder información. | Escenario 1: Dado que la app está en segundo plano, Cuando llega un mensaje LoRa, Entonces el sistema lo procesa y lo guarda. Escenario 2: Dado que el usuario no tiene la app abierta, Cuando llega el mensaje, Entonces recibe una notificación. | EP-01 |
| US-06 | Conexión Bluetooth | Como usuario, quiero conectar mi celular al dispositivo LoRa mediante Bluetooth, para poder enviar mensajes. | Escenario 1: Dado que el Bluetooth está activado, Cuando el usuario selecciona un dispositivo, Entonces el sistema establece la conexión. Escenario 2: Dado que el dispositivo no está disponible, Cuando el usuario intenta conectarse, Entonces se muestra un error. | EP-02 |
| US-07 | Visualizar dispositivos | Como usuario, quiero ver dispositivos Bluetooth disponibles, para seleccionar el correcto. | Escenario 1: Dado que el Bluetooth está activo, Cuando el usuario accede a la lista, Entonces se muestran los dispositivos cercanos. Escenario 2: Dado que no hay dispositivos, Cuando se accede, Entonces se muestra un mensaje de “sin dispositivos”. | EP-02 |
| US-08 | Estado de conexión | Como usuario, quiero ver el estado de conexión, para saber si puedo enviar mensajes. | Escenario 1: Dado que existe conexión, Cuando se visualiza el estado, Entonces muestra “conectado”. Escenario 2: Dado que se pierde la conexión, Cuando ocurre el evento, Entonces cambia a “desconectado”. | EP-02 |
| US-09 | Reconexión automática | Como usuario, quiero reconexión automática, para no reconectar manualmente. | Escenario 1: Dado que la conexión se pierde, Cuando el dispositivo vuelve a estar disponible, Entonces el sistema intenta reconectar automáticamente. Escenario 2: Dado que falla la reconexión, Cuando se intenta varias veces, Entonces se notifica al usuario. | EP-02 |
| US-10 | Desconexión manual | Como usuario, quiero desconectarme manualmente, para gestionar mis dispositivos. | Escenario 1: Dado que el usuario presiona desconectar, Cuando se ejecuta la acción, Entonces la conexión se termina. Escenario 2: Dado que se desconecta, Cuando se actualiza el estado, Entonces se muestra “desconectado”. | EP-02 |
| US-11 | Encriptar mensajes | Como usuario, quiero que mis mensajes se encripten antes de ser enviados, para proteger mi información. | Escenario 1: Dado que el usuario envía un mensaje, Cuando el sistema procesa el envío, Entonces el mensaje se encripta antes de transmitirse. Escenario 2: Dado que ocurre un error en el cifrado, Cuando se intenta enviar el mensaje, Entonces el sistema bloquea el envío y notifica el error. | EP-03 |
| US-12 | Desencriptar mensajes | Como usuario, quiero que los mensajes recibidos se desencripten automáticamente, para poder leerlos. | Escenario 1: Dado que se recibe un mensaje cifrado, Cuando el sistema lo procesa, Entonces se desencripta correctamente. Escenario 2: Dado que la clave es inválida, Cuando se intenta desencriptar, Entonces se muestra un error. | EP-03 |
| US-13 | Protección en transmisión | Como usuario, quiero que los mensajes no puedan ser leídos por terceros, para mantener privacidad. | Escenario 1: Dado que el mensaje viaja por LoRa, Cuando es interceptado, Entonces no es legible. Escenario 2: Dado que un usuario no autorizado accede, Entonces no puede descifrar el mensaje. | EP-03 |
| US-14 | Integridad del mensaje | Como usuario, quiero asegurar que el mensaje no sea alterado, para confiar en la información. | Escenario 1: Dado que el mensaje llega, Cuando se valida, Entonces se confirma su integridad. Escenario 2: Dado que el mensaje fue alterado, Cuando se valida, Entonces se descarta. | EP-03 |
| US-15 | Seguridad de claves | Como usuario, quiero que las claves de cifrado sean seguras, para proteger mis datos. | Escenario 1: Dado que se genera una clave, Cuando se almacena, Entonces se guarda de forma segura. Escenario 2: Dado acceso no autorizado, Entonces no puede acceder a las claves. | EP-03 |
| US-16 | Crear usuario local | Como usuario, quiero crear un perfil local, para usar la app sin servidor. | Escenario 1: Dado que es la primera vez, Cuando ingresa datos, Entonces se crea usuario. Escenario 2: Dado error, Entonces se notifica. | EP-04 |
| US-17 | Editar perfil | Como usuario, quiero modificar mis datos, para mantenerlos actualizados. | Escenario 1: Dado edición, Cuando guarda, Entonces se actualiza. Escenario 2: Dado error, Entonces no se guarda. | EP-04 |
| US-18 | Identidad en mensajes | Como usuario, quiero que mis mensajes incluyan mi nombre, para identificarme. | Escenario 1: Dado envío, Cuando se procesa, Entonces incluye nombre. Escenario 2: Dado falta de datos, Entonces usa ID local. | EP-04 |
| US-19 | Persistencia del usuario | Como usuario, quiero que mi perfil se mantenga, para no configurarlo nuevamente. | Escenario 1: Dado reinicio, Entonces mantiene datos. Escenario 2: Dado borrado, Entonces solicita creación. | EP-04 |
| US-20 | Uso sin cuenta externa | Como usuario, quiero usar la app sin login online, para no depender de internet. | Escenario 1: Dado acceso, Entonces no solicita login. Escenario 2: Dado uso completo, Entonces funciona offline. | EP-04 |
| US-21 | Guardar mensajes | Como usuario, quiero almacenar mensajes localmente, para revisarlos luego. | Escenario 1: Dado mensaje, Cuando se envía/recibe, Entonces se guarda en DB. Escenario 2: Dado error, Entonces se notifica. | EP-05 |
| US-22 | Ver historial | Como usuario, quiero ver historial de mensajes, para consultar conversaciones. | Escenario 1: Dado acceso, Entonces muestra historial. Escenario 2: Dado vacío, Entonces muestra mensaje. | EP-05 |
| US-23 | Datos encriptados | Como usuario, quiero que los datos estén cifrados, para seguridad. | Escenario 1: Dado almacenamiento, Entonces se cifra. Escenario 2: Dado acceso externo, Entonces no es legible. | EP-05 |
| US-24 | Persistencia de datos | Como usuario, quiero que los datos no se pierdan, para continuidad. | Escenario 1: Dado reinicio, Entonces mantiene datos. Escenario 2: Dado fallo, Entonces intenta recuperar. | EP-05 |
| US-25 | Guardar configuración | Como usuario, quiero guardar configuraciones, para personalizar la app. | Escenario 1: Dado cambio, Entonces se guarda. Escenario 2: Dado error, Entonces no se aplica. | EP-05 |
| US-26 | Acceder a landing | Como visitante, quiero acceder a la landing page, para conocer el producto. | Escenario 1: Dado acceso web, Entonces carga correctamente. Escenario 2: Dado error, Entonces muestra fallback. | EP-06 |
| US-27 | Ver propuesta de valor | Como visitante, quiero entender el beneficio del sistema, para evaluarlo. | Escenario 1: Dado navegación, Entonces muestra propuesta clara. Escenario 2: Dado lectura, Entonces es comprensible. | EP-06 |
| US-28 | Ver funcionamiento | Como visitante, quiero entender cómo funciona el sistema, para conocer su tecnología. | Escenario 1: Dado sección info, Entonces explica LoRa + Bluetooth. Escenario 2: Dado interacción, Entonces es claro. | EP-06 |
| US-29 | Diseño responsive | Como visitante, quiero ver la web en cualquier dispositivo, para acceder fácilmente. | Escenario 1: Dado móvil, Entonces se adapta. Escenario 2: Dado desktop, Entonces mantiene diseño. | EP-06 |
| US-30 | Contacto | Como visitante, quiero contactar o mostrar interés, para saber más. | Escenario 1: Dado acción, Entonces registra contacto. Escenario 2: Dado error, Entonces notifica. | EP-06 |
| TS-01 | Implementación de comunicación LoRa | Como developer del sistema, quiero implementar la transmisión de datos mediante LoRa, para permitir comunicación entre dispositivos. | Escenario 1: Dado que el dispositivo LoRa está correctamente inicializado, Cuando el sistema envía un paquete de datos, Entonces el mensaje es transmitido correctamente a través de la red LoRa. <br><br> Escenario 2: Dado que ocurre interferencia o pérdida de señal, Cuando el sistema intenta enviar el mensaje, Entonces reintenta la transmisión y registra el fallo si no se logra enviar. | EP-01 |
| TS-02 | Recepción de datos LoRa | Como developer del sistema, quiero implementar la recepción de datos LoRa, para procesar mensajes entrantes. | Escenario 1: Dado que llega un paquete LoRa válido, Cuando el sistema lo recibe, Entonces lo decodifica y lo entrega a la aplicación. <br><br> Escenario 2: Dado que el paquete recibido está corrupto o incompleto, Cuando el sistema intenta procesarlo, Entonces descarta el paquete y registra el error. | EP-01 |
| TS-03 | Implementación Bluetooth BLE | Como developer del sistema, quiero implementar conexión Bluetooth Low Energy (BLE), para conectar la app con el dispositivo LoRa de forma eficiente. | Escenario 1: Dado que el Bluetooth está habilitado en el dispositivo móvil, Cuando el sistema inicia el proceso de conexión, Entonces se establece una conexión BLE estable con el dispositivo LoRa. <br><br> Escenario 2: Dado que el dispositivo no responde o está fuera de alcance, Cuando se intenta la conexión, Entonces el sistema muestra un error y permite reintentar. | EP-02 |
| TS-04 | Manejo de estado de conexión Bluetooth | Como developer del sistema, quiero gestionar los estados de conexión Bluetooth, para reflejar correctamente el estado en la interfaz. | Escenario 1: Dado que la conexión Bluetooth cambia de estado (conectado/desconectado), Cuando ocurre el evento, Entonces el sistema actualiza inmediatamente la interfaz del usuario. <br><br> Escenario 2: Dado que la conexión se pierde inesperadamente, Cuando el sistema detecta la desconexión, Entonces notifica al usuario e intenta reconectar automáticamente. | EP-02 |
| TS-05 | Implementación de cifrado de mensajes | Como developer del sistema, quiero implementar cifrado de extremo a extremo, para proteger los mensajes durante la transmisión. | Escenario 1: Dado que el usuario envía un mensaje, Cuando el sistema procesa el envío, Entonces el mensaje se cifra antes de ser transmitido. <br><br> Escenario 2: Dado que ocurre un error en el proceso de cifrado, Cuando el sistema intenta enviar el mensaje, Entonces se bloquea el envío y se registra el error. | EP-03 |
| TS-06 | Gestión de usuario local | Como developer del sistema, quiero implementar la gestión de usuarios locales, para evitar dependencia de un servidor externo. | Escenario 1: Dado que el usuario crea o edita su perfil, Cuando el sistema procesa la información, Entonces los datos se almacenan correctamente en el dispositivo. <br><br> Escenario 2: Dado que ocurre un error al guardar los datos, Cuando el sistema intenta persistir la información, Entonces se muestra un mensaje de error y no se aplican los cambios. | EP-04 |
| TS-07 | Implementación de base de datos SQLite | Como developer del sistema, quiero integrar SQLite, para almacenar mensajes y configuraciones de forma local. | Escenario 1: Dado que se realiza una operación de almacenamiento, Cuando el sistema guarda los datos, Entonces la información se persiste correctamente en la base de datos SQLite. <br><br> Escenario 2: Dado que ocurre un error en la operación de la base de datos, Cuando el sistema intenta guardar la información, Entonces registra el error y muestra un mensaje indicando que no se pudo completar la operación. | EP-05 |
| TS-08 | Encriptación de base de datos | Como developer del sistema, quiero cifrar la base de datos SQLite, para proteger los datos almacenados localmente. | Escenario 1: Dado que los datos se almacenan en la base de datos, Cuando el sistema los guarda, Entonces se cifran automáticamente antes de persistirse. <br><br> Escenario 2: Dado que un acceso no autorizado intenta leer la base de datos, Cuando se intenta acceder sin credenciales válidas, Entonces los datos no son legibles y el acceso es denegado. | EP-05 |

## 3.3. Impact Mapping

El Impact Mapping es una metodología visual que permite establecer una conexión clara entre los objetivos estratégicos del negocio, los actores involucrados y las funcionalidades del producto digital. A través de una estructura jerárquica, esta herramienta facilita comprender cómo las metas del proyecto se traducen en cambios de comportamiento en los usuarios y, posteriormente, en entregables concretos que generan valor.

En el presente proyecto, el Impact Mapping se utilizó para estructurar la relación entre los objetivos estratégicos de comunicación en entornos sin conectividad, los User Personas definidos previamente (**Carlos Mamani**, agricultor en zona rural, y **María García**, jefa de brigada de emergencia), y las funcionalidades clave del sistema *OffGrid Messenger*. Este enfoque permitió asegurar que cada elemento desarrollado responda a necesidades reales y tenga un impacto directo en la solución del problema identificado.

El trabajo realizado incluyó:

- **Business Goals orientados a conectividad real y seguridad:** metas específicas y medibles enfocadas en mejorar la comunicación en zonas rurales y escenarios de emergencia, como reducir los tiempos de respuesta ante incidentes, aumentar la cobertura de comunicación sin internet y garantizar la privacidad de los mensajes mediante encriptación.

- **Actores principales (User Personas):** Carlos Mamani, quien representa a usuarios en zonas rurales con acceso limitado a tecnología y conectividad, y María García, quien representa a equipos de emergencia que requieren comunicación confiable en situaciones críticas. Ambos actores fueron definidos considerando sus necesidades, comportamientos y limitaciones tecnológicas.

- **Impactos esperados:** definidos como cambios en el comportamiento de los usuarios que contribuyen al logro de los objetivos del negocio. Por ejemplo, que Carlos utilice la aplicación para coordinar actividades sin necesidad de desplazarse físicamente, o que María pueda gestionar equipos de rescate en tiempo real sin depender de redes móviles tradicionales.

- **Deliverables funcionales:** características del sistema diseñadas para generar dichos impactos, como la comunicación mediante LoRa, la conexión vía Bluetooth con dispositivos físicos, la mensajería encriptada, el almacenamiento local en SQLite y la interfaz simple e intuitiva.

El Impact Mapping fue desarrollado bajo un enfoque centrado en el usuario, priorizando accesibilidad, confiabilidad y simplicidad. Se buscó que cada funcionalidad no solo sea técnicamente viable, sino que también responda directamente a los problemas identificados en los mapas de empatía y escenarios previos, garantizando coherencia entre el diseño del sistema y la realidad del usuario final.

---

## Business Goal 1

**Permitir una comunicación confiable, segura y sin dependencia de internet en zonas rurales y escenarios de emergencia, mediante el uso de tecnología LoRa y conexión Bluetooth, mejorando la coordinación, reduciendo tiempos de respuesta y aumentando la seguridad de los usuarios en un periodo inicial de adopción de 6 meses.**

Este objetivo representa el núcleo estratégico del proyecto, ya que aborda directamente el problema principal identificado: la falta de comunicación en entornos donde no existe cobertura de red. La solución propuesta no busca reemplazar los sistemas tradicionales, sino ofrecer una alternativa funcional en contextos donde estos fallan, como zonas rurales, áreas montañosas o situaciones de desastre.

Desde una perspectiva operativa, este objetivo es medible a través de indicadores como el tiempo promedio de envío y recepción de mensajes, la tasa de éxito en la comunicación entre dispositivos, y la reducción en los tiempos de respuesta en situaciones de emergencia. Asimismo, se puede evaluar mediante la adopción del sistema por parte de usuarios en comunidades rurales o equipos de rescate.

Este Business Goal se encuentra alineado con los comportamientos esperados de los actores definidos. Carlos Mamani podrá comunicarse con su familia o coordinar actividades agrícolas sin necesidad de desplazarse, lo que reduce costos y tiempo. Por otro lado, María García podrá gestionar operaciones de emergencia con mayor eficiencia, manteniendo comunicación constante incluso en ausencia de infraestructura de red.

En este sentido, el objetivo no solo responde a una necesidad tecnológica, sino también social, ya que busca mejorar la calidad de vida de los usuarios y fortalecer la capacidad de respuesta ante situaciones críticas. La solución propuesta promueve un cambio en la forma en que las personas entienden la comunicación: pasando de depender completamente del internet, a utilizar redes descentralizadas adaptadas a su entorno.

Finalmente, este objetivo impulsa la adopción de una tecnología accesible, confiable y segura, incentivando a los usuarios a confiar en el sistema y convertirlo en parte de su vida diaria o de sus operaciones críticas. De esta manera, el proyecto no solo entrega una herramienta, sino que propone una nueva forma de comunicación adaptada a realidades donde la conectividad tradicional no es suficiente.

<img width="1715" height="589" alt="image" src="https://github.com/user-attachments/assets/d7992742-eef3-478f-8bb7-6dcb60144f89" />

Link MiroBoard:https://miro.com/app/board/uXjVGh28bbM=/?share_link_id=225209259008

## 3.4 Product Backlog 

| # Orden | User Story Id | Título | Descripción | Story Points |
|--------|---------------|--------|-------------|--------------|
| 1 | US-06 | Conexión Bluetooth | Como usuario, deseo conectar mi celular al dispositivo LoRa mediante Bluetooth, para poder iniciar la comunicación. | 8 |
| 2 | TS-03 | Implementación Bluetooth BLE | Como developer del sistema, deseo implementar conexión Bluetooth Low Energy, para permitir la comunicación entre la app y el dispositivo LoRa. | 8 |
| 3 | US-01 | Enviar mensaje por LoRa | Como usuario, deseo enviar mensajes mediante tecnología LoRa, para comunicarme sin usar internet. | 8 |
| 4 | TS-01 | Implementación comunicación LoRa | Como developer del sistema, deseo implementar la transmisión de datos mediante LoRa, para permitir comunicación entre dispositivos. | 8 |
| 5 | US-02 | Recepción de mensajes LoRa | Como usuario, deseo recibir mensajes desde la red LoRa, para mantener comunicación con otros usuarios. | 5 |
| 6 | TS-02 | Recepción de datos LoRa | Como developer del sistema, deseo implementar la recepción de datos LoRa, para procesar mensajes entrantes. | 5 |
| 7 | US-08 | Estado de conexión | Como usuario, deseo ver el estado de conexión Bluetooth y LoRa, para saber si puedo enviar mensajes. | 3 |
| 8 | TS-04 | Manejo de estado Bluetooth | Como developer del sistema, deseo gestionar los estados de conexión, para reflejar correctamente la información en la interfaz. | 3 |
| 9 | US-11 | Encriptar mensajes | Como usuario, deseo que mis mensajes se encripten antes de ser enviados, para proteger mi información. | 5 |
| 10 | TS-05 | Implementación de cifrado | Como developer del sistema, deseo implementar cifrado de extremo a extremo, para proteger los mensajes. | 5 |
| 11 | US-12 | Desencriptar mensajes | Como usuario, deseo que los mensajes recibidos se desencripten automáticamente, para poder leerlos. | 5 |
| 12 | US-16 | Crear usuario local | Como usuario, deseo crear un perfil local, para usar la aplicación sin necesidad de servidor. | 3 |
| 13 | TS-06 | Gestión de usuario local | Como developer del sistema, deseo implementar la gestión de usuarios locales, para evitar dependencia de un servidor. | 3 |
| 14 | US-21 | Guardar mensajes | Como usuario, deseo almacenar mensajes localmente, para revisarlos posteriormente. | 5 |
| 15 | TS-07 | Implementación SQLite | Como developer del sistema, deseo integrar SQLite, para almacenamiento local de datos. | 5 |
| 16 | TS-08 | Encriptación de base de datos | Como developer del sistema, deseo cifrar la base de datos, para proteger la información almacenada. | 5 |
| 17 | US-22 | Ver historial | Como usuario, deseo visualizar el historial de mensajes, para consultar conversaciones anteriores. | 3 |
| 18 | US-09 | Reconexión automática | Como usuario, deseo que el sistema se reconecte automáticamente, para evitar reconexión manual. | 5 |
| 19 | US-07 | Visualizar dispositivos | Como usuario, deseo ver dispositivos Bluetooth disponibles, para seleccionar el correcto. | 3 |
| 20 | US-04 | Confirmación de envío | Como usuario, deseo saber si mi mensaje fue enviado correctamente, para asegurar la comunicación. | 2 |
| 21 | US-10 | Desconexión manual | Como usuario, deseo desconectarme manualmente, para gestionar mis dispositivos. | 2 |
| 22 | US-03 | Comunicación a larga distancia | Como usuario, deseo comunicarme a larga distancia mediante LoRa, para usar el sistema en zonas remotas. | 5 |
| 23 | US-05 | Recepción en segundo plano | Como usuario, deseo recibir mensajes en segundo plano, para no perder información. | 3 |
| 24 | US-17 | Editar perfil | Como usuario, deseo modificar mis datos, para mantenerlos actualizados. | 2 |
| 25 | US-18 | Identidad en mensajes | Como usuario, deseo que mis mensajes incluyan mi nombre, para identificarme. | 2 |
| 26 | US-19 | Persistencia del usuario | Como usuario, deseo que mi perfil se mantenga guardado, para no configurarlo nuevamente. | 2 |
| 27 | US-20 | Uso sin cuenta externa | Como usuario, deseo utilizar la app sin iniciar sesión en internet, para no depender de servicios externos. | 3 |
| 28 | US-23 | Datos encriptados | Como usuario, deseo que los datos almacenados estén cifrados, para proteger mi información local. | 5 |
| 29 | US-24 | Persistencia de datos | Como usuario, deseo que los datos no se pierdan al cerrar la aplicación, para mantener continuidad. | 3 |
| 30 | US-25 | Guardar configuración | Como usuario, deseo guardar configuraciones personalizadas, para adaptar la aplicación a mis necesidades. | 2 |
| 31 | US-26 | Acceder a landing | Como visitante, deseo acceder a la landing page, para conocer el producto. | 2 |
| 32 | TS-09 | Desarrollo landing web | Como developer del sistema, deseo implementar la landing page, para presentar el producto. | 3 |
| 33 | US-27 | Ver propuesta de valor | Como visitante, deseo entender el beneficio del sistema, para evaluarlo. | 2 |
| 34 | US-28 | Ver funcionamiento | Como visitante, deseo entender cómo funciona el sistema, para conocer su tecnología. | 3 |
| 35 | US-29 | Diseño responsive | Como visitante, deseo visualizar la página en cualquier dispositivo, para acceder fácilmente. | 2 |
| 36 | US-30 | Contacto | Como visitante, deseo contactar o mostrar interés, para obtener más información. | 2 |

Trello Link: https://trello.com/invite/b/69e039aa6ed1e43060410917/ATTIb801d16fcecd920a4b1b714c5b7dd64b45A2AB05/offgridmessenger

<img width="1919" height="799" alt="image" src="https://github.com/user-attachments/assets/e67ab4d6-46f5-409e-abf8-eab600011350" />
