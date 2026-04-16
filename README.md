<div align="center">

<img src="https://marketingperu.beglobal.biz/wp-content/uploads/2025/01/logo-upc-png-transparente-1.png" width="120" alt="Logo UPC"/>

<br>

# UNIVERSIDAD PERUANA DE CIENCIAS APLICADAS

### 17949 - Fundamentos de Arquitectura de Software

<br>

**Docente:**
**Jorge Luis Delgado**

<br>

**Integrantes:**

Juan Carlos Angulo Abud - u202317692
<br>
Renzo Paul Retuerto Zapata - u202320328
<br>
Renzo Sebastián Uribe Livia - u202311745
<br>
Oscar Leonardo Espinoza Quijandria - u202311842
<br>

**2026 - 01**

</div>

---


# Capítulo I: Introducción


## 1.1 Startup Profile

### 1.1.1 Descripción de la Startup
Somos una startup dedicada a revolucionar la conectividad en zonas críticas mediante el desarrollo de sistemas de comunicación alternativa. Nuestra propuesta combina la potencia de la tecnología **IoT** y redes de largo alcance (**LoRa**) con aplicaciones móviles de última generación, permitiendo crear redes descentralizadas e independientes de la infraestructura de internet convencional. 

### 1.1.2 Perfiles de integrantes del equipo
El equipo está conformado por estudiantes de Ingeniería de Software con competencias complementarias en el ciclo de vida de desarrollo:

| Integrante | Descripción |
| :---: | :--- |
| <img src="./images/juan.png" width="100"><br>**Juan Carlos Angulo Abud** | Especialista en análisis de requerimientos y lógica de negocio. |
| <img src="./images/renzo1.jpg" width="100"><br>**Renzo Paul Retuerto Zapata** | Enfocado en arquitectura de sistemas, integración de hardware IoT y desarrollo backend. |
| <img src="./images/renzo uribe.png" width="100"><br>**Renzo Sebastián Uribe Livia** | Responsable del diseño de interfaces de usuario y aseguramiento de la calidad del software. |
| <img src="./images/oscar.png" width="100"><br>**Oscar Leonardo Espinoza Quijandria** | Encargado de la arquitectura del sistema y desarrollo del backend e integración Bluetooth–LoRa. |
| <img src="./images/foto5.png" width="100"><br>**Nombre Integrante 5** | Descripción de las habilidades y rol del quinto integrante. |


---


# 1.2 Solution Profile


### 1.2.1 Nombre del producto
El producto desarrollado llevará el nombre de **OffGrid Messenger**, una solución de mensajería descentralizada basada en tecnología **LoRa** ya que representa una plataforma de mensajería capaz de operar sin conexión a redes tradicionales, enfocada en comunicación descentralizada y de largo alcance.

### 1.2.2 Antecedentes y problemática
Hoy en día, quedarse sin señal en una zona remota o durante una emergencia no debería ser una limitación. Hemos diseñado una solución de comunicación independiente que rompe la dependencia del internet tradicional mediante el uso de tecnología **IoT (ESP32 y LoRa)**. 

> Nuestra plataforma permite que cualquier celular se mantenga conectado a largas distancias, utilizando dispositivos de bajo consumo que actúan como puentes de comunicación segura. Es una red privada y cifrada, pensada para proteger y conectar a las personas donde las redes convencionales simplemente no llegan.

---
## 1.2.3 Lean UX Process

### 1.2.3.1 Lean UX Problem Statement

| Sección | Detalle del Problem Statement |
| :--- | :--- |
| **El problema** | Los usuarios en zonas rurales, remotas y durante emergencias enfrentan la imposibilidad de comunicarse cuando no tienen acceso a redes móviles tradicionales o internet, lo que genera aislamiento, riesgos de seguridad y limitaciones en la coordinación de actividades críticas. |
| **¿Para quién?** | • Personas en zonas de baja cobertura celular<br>• Equipos de respuesta ante emergencias<br>• Usuarios de actividades outdoor (senderismo, camping, expediciones)<br>• Comunidades rurales desconectadas |
| **El impacto** | • Incapacidad de pedir ayuda en situaciones de emergencia<br>• Pérdida de coordinación en equipos de trabajo remoto<br>• Aislamiento de comunidades durante desastres naturales<br>• Inseguridad personal en zonas sin conectividad |
| **Solución** | **OffGrid Messenger** es una plataforma de mensajería descentralizada que utiliza tecnología LoRa e IoT (ESP32) para crear redes privadas de comunicación independientes. |

---

### 1.2.3.2 Lean UX Assumptions

#### 🟦 Suposiciones sobre el Usuario
* **Suposición 1: Necesidad de Comunicación Alternativa**
    * Los usuarios en zonas rurales y remotas necesitan realmente una alternativa de comunicación cuando no tienen acceso a redes móviles tradicionales.
    * Los usuarios enfrentan situaciones donde la falta de comunicación representa un riesgo real (emergencias, coordinación de actividades).
    * **A validar mediante:** Entrevistas con usuarios objetivo, análisis de incidentes de emergencia en zonas remotas.

* **Suposición 2: Disposición a Usar Dispositivos Adicionales**
    * Los usuarios están dispuestos a adoptar dispositivos LoRa adicionales si mejora significativamente su conectividad.
    * Los usuarios entienden el valor de una red descentralizada y están motivados a participar en ella.
    * **A validar mediante:** Encuestas de aceptación de tecnología, pruebas con usuarios beta.

* **Suposición 3: Priorización de Privacidad y Seguridad**
    * Los usuarios en emergencias y zonas remotas priorizan la privacidad de sus comunicaciones.
    * Los usuarios confían en soluciones con cifrado de extremo a extremo para proteger información sensible.
    * Los usuarios entienden y valoran la diferencia entre redes privadas descentralizadas y redes públicas.
    * **A validar mediante:** Estudios de preferencia de usuarios, análisis de preocupaciones de seguridad.

* **Suposición 4: Capacidad de Uso sin Conocimientos Técnicos Avanzados**
    * Los usuarios de zonas rurales pueden operar la aplicación móvil sin requerir entrenamiento técnico extenso.
    * Los usuarios pueden realizar setup de dispositivos LoRa con instrucciones simples.
    * La interfaz móvil intuitiva es suficiente para usuarios con baja alfabetización digital.
    * **A validar mediante:** Pruebas de usabilidad con usuarios objetivo, medición de tiempo de aprendizaje.

* **Suposición 5: Accesibilidad Económica**
    * Los usuarios target pueden permitirse el costo de nodos LoRa y suscripción al servicio.
    * El precio es competitivo comparado con soluciones alternativas (satélites, radios profesionales).
    * **A validar mediante:** Análisis de viabilidad económica, encuestas de disposición a pagar.

#### 🟩 Suposiciones sobre el Producto
* **Suposición 6: Viabilidad Técnica de Cobertura LoRa**
    * La tecnología LoRa puede alcanzar distancias de 5-10 km en línea de vista en terreno rural de Perú.
    * La cobertura real en terreno montañoso/Amazonía alcanza al menos 3-5 km con retransmisión multi-hop.
    * Los nodos LoRa funcionan confiablemente en condiciones ambientales de Perú (lluvia, temperatura, altitud).
    * **A validar mediante:** Pruebas de campo en zonas piloto, medición de cobertura real vs. simulada.

* **Suposición 7: Rendimiento de Mensajería Aceptable**
    * El tiempo de entrega de mensajes es menor a 2 segundos en condiciones normales.
    * La tasa de entrega exitosa es ≥80% incluso con red congestionada.
    * El throughput de mensajes es suficiente para comunicación en tiempo real.
    * **A validar mediante:** Pruebas de rendimiento en laboratorio y campo, monitoreo de SLA.

* **Suposición 8: Eficiencia Energética de Dispositivos**
    * Los dispositivos móviles consumen <10% de batería por hora en modo de comunicación activa.
    * Los nodos LoRa pueden funcionar 48+ horas con batería estándar.
    * El consumo de energía es aceptable incluso en uso intensivo durante emergencias.
    * **A validar mediante:** Pruebas de autonomía de batería, medición de consumo en diferentes escenarios.

* **Suposición 9: Escalabilidad de la Red Descentralizada**
    * La arquitectura descentralizada puede soportar 100+ nodos simultáneamente sin degradación crítica.
    * El protocolo multi-hop permite cobertura expandida sin servidor central.
    * La red puede auto-organizarse y recuperarse de fallos de nodos individuales.
    * **A validar mediante:** Pruebas de carga, simulaciones de redes grandes, resiliencia ante fallos.

* **Suposición 10: Seguridad del Cifrado Implementado**
    * El cifrado de extremo a extremo es resistente a ataques comunes (sin auditoría profesional).
    * La implementación en ESP32 es criptográficamente segura sin comprometer rendimiento.
    * Las claves se pueden gestionar sin compromiso de seguridad en dispositivos de bajo poder.
    * **A validar mediante:** Auditoría de seguridad profesional, testing de penetración.

#### 🟧 Suposiciones sobre el Negocio
* **Suposición 11: Demanda Real en el Mercado**
    * Existe una demanda genuina en zonas rurales y equipos de emergencia de Perú.
    * El mercado objetivo está dispuesto a cambiar de solución actual o adoptar nueva tecnología.
    * El tamaño del mercado es lo suficientemente grande para viabilidad comercial.
    * **A validar mediante:** Estudios de mercado, encuestas, entrevistas con potenciales clientes.

* **Suposición 12: Modelo de Negocio Viable**
    * Los usuarios pagarían suscripción mensual por servicio premium (backup en cloud, análisis, etc.).
    * La venta de nodos LoRa genera margen de ganancia suficiente para sostenibilidad.
    * Los costos operativos son menores que los ingresos proyectados.
    * **A validar mediante:** Modelo financiero, análisis de rentabilidad, forecasting de adopción.

* **Suposición 13: Oportunidad de Alianzas Institucionales**
    * Instituciones públicas (INDECI, bomberos, municipalidades) buscan soluciones como OffGrid Messenger.
    * Las alianzas públicas son viables y escalables como canal de distribución.
    * El gobierno puede financiar o subsidiar soluciones de conectividad para zonas rurales.
    * **A validar mediante:** Contacto con instituciones, análisis de procurement público, pilotos institucionales.

* **Suposición 14: Factibilidad de Fabricación y Distribución**
    * Los costos de manufactura de nodos LoRa son económicamente competitivos en volumen.
    * Existe cadena de suministro viable para componentes LoRa en Perú/Latinoamérica.
    * La distribución a zonas rurales es logísticamente factible sin costos prohibitivos.
    * **A validar mediante:** Cotizaciones de manufactura, análisis de supply chain, logística piloto.

#### 🟨 Suposiciones sobre Regulación y Cumplimiento
* **Suposición 15: Regulación de Espectro LoRa Favorable**
    * El espectro LoRa (ISM 915 MHz o similar) es de uso libre en Perú sin licencia requerida.
    * No existen restricciones legales para operación de redes LoRa privadas descentralizadas.
    * La regulación MITC/MTC permite el despliegue sin interferencias legales.
    * **A validar mediante:** Investigación regulatoria, consulta con abogados especializados, MITC.

* **Suposición 16: Privacidad de Datos Conforme a Normativa**
    * La solución cumple con LPDP (Ley de Protección de Datos Personales) de Perú.
    * El almacenamiento local de mensajes es legal bajo normativa de privacidad.
    * No hay obligación de retención de datos en servidores centrales.
    * **A validar mediante:** Asesoría legal, compliance audit, AEPD.

---

### 1.2.3.3 Lean UX Hypothesis


 **Hipótesis 1: Mensajería Cifrada de Extremo a Extremo**
> * **Si** [usuarios en zonas remotas y durante emergencias]
> * **Logran** [comunicación privada y segura sin exposición de datos]
> * **Con** [cifrado de extremo a extremo en todos los mensajes]
> * **Creemos que** los usuarios adoptarán OffGrid Messenger porque garantiza que sus comunicaciones críticas en emergencias no serán interceptadas, lo cual es esencial para equipos de respuesta y comunidades vulnerables.


 **Hipótesis 2: Cobertura de Largo Alcance con LoRa**
> * **Si** [usuarios en zonas rurales sin cobertura celular]
> * **Logran** [capacidad de comunicarse a distancias de 5-10 km sin infraestructura tradicional]
> * **Con** [red descentralizada de nodos LoRa que funcionan como retransmisores (multi-hop)]
> * **Creemos que** al distribuir nodos LoRa en puntos estratégicos, los usuarios podrán mantener conectividad continua en áreas donde actualmente no existe cobertura, resolviendo el aislamiento en zonas remotas.


 **Hipótesis 3: Interfaz Móvil Intuitiva y Accesible**
> * **Si** [usuarios con diferentes niveles de habilidad técnica]
> * **Logran** [capacidad de usar la app sin necesidad de configuración técnica compleja]
> * **Con** [interfaz móvil simple, con setup automático de nodos y visualización clara del estado de la red]
> * **Creemos que** una app fácil de usar sin requerir conocimientos técnicos avanzados aumentará la adopción incluso en comunidades rurales con baja alfabetización digital.


 **Hipótesis 4: Bajo Consumo de Energía en Dispositivos Móviles**
> * **Si** [usuarios que dependen de baterías en zonas sin electricidad]
> * **Logran** [duración extendida de la batería del dispositivo móvil durante comunicación]
> * **Con** [optimización del consumo de energía en la conexión LoRa y procesamiento local de mensajes]
> * **Creemos que** minimizar el consumo de batería permitirá que los usuarios mantengan comunicación durante períodos extendidos sin acceso a energía, crítico en emergencias.


 **Hipótesis 5: Sincronización Automática en Modo Offline**
> * **Si** [usuarios en zonas con conectividad intermitente]
> * **Logran** [entrega confiable de mensajes incluso cuando hay desconexiones temporales]
> * **Con** [almacenamiento local de mensajes y sincronización automática cuando la red se recupera]
> * **Creemos que** permitir el trabajo offline sin perder mensajes eliminará la frustración de usuarios en zonas de cobertura inconsistente y mejorará la experiencia general.


 **Hipótesis 6: Cumplimiento Regulatorio y Legalidad**
> * **Si** [usuarios en Perú y zonas Latinoamericanas]
> * **Logran** [operación legal y sin interferencias de frecuencias reguladas]
> * **Con** [uso de espectro LoRa libre (banda ISM 915 MHz o similar según regulación local)]
> * **Creemos que** operar dentro del marco regulatorio correcto garantizará que la solución sea escalable sin riesgos legales y generará confianza en usuarios institucionales como equipos de emergencia.

---

### 📊 Métricas de Validación Sugeridas

| Hipótesis | Métrica de Validación | Objetivo / Criterio de Éxito |
| :--- | :--- | :--- |
| **H1: Seguridad** | Auditoría de seguridad y reporte de confianza | Encriptación verificada; 90%+ de usuarios confían en la privacidad. |
| **H2: Cobertura** | Pruebas de campo en terreno real | Alcance de 5-10 km; 80%+ de mensajes entregados con éxito. |
| **H3: Usabilidad** | Pruebas de usuario (User Testing) | Tiempo de setup < 2 min; 85%+ de éxito sin soporte técnico. |
| **H4: Energía** | Monitoreo de consumo de batería | Consumo < 10% por hora (activo); duración de 24+ horas. |
| **H5: Offline** | Pruebas de estrés y reconexión | 95%+ de entrega tras reconexión; pérdida de datos < 1%. |
| **H6: Legal** | Certificación regulatoria y escaneo de espectro | Certificación obtenida; 0 incidentes de interferencia. |

---
### 1.2.3.4 Lean UX Canvas

---


# 1.3 Segmentos Objetivo


El producto está dirigido a usuarios que requieren comunicación en entornos donde la conectividad a internet o redes móviles es limitada o inexistente. A continuación, se detallan los segmentos objetivo identificados:

### 1. Usuarios en zonas rurales o con baja conectividad
Este segmento abarca a pobladores y trabajadores en áreas geográficas donde las operadoras de red tradicionales no tienen cobertura debido a la dificultad del terreno (sierra y selva).
* **Perfil:** Agricultores, ganaderos y comunidades rurales aisladas.
* **Necesidad:** Mantener contacto con familiares y coordinar actividades comerciales o de salud básicas.
* **Caso de Uso:** Envío de alertas ante emergencias médicas o coordinación de logística para el transporte de productos sin depender de una señal de celular costosa o inexistente.

### 2. Usuarios en actividades al aire libre (Outdoor)
Dirigido a entusiastas del deporte y la aventura que exploran rutas fuera del alcance de las torres de comunicación.
* **Perfil:** Senderistas (trekkers), montañistas, ciclistas de montaña y grupos de expedición.
* **Necesidad:** Mantener la comunicación entre los miembros del grupo y contar con un mecanismo de auxilio en zonas remotas.
* **Caso de Uso:** Localización de miembros del grupo en rutas de trekking y envío de señales de "S.O.S" con coordenadas exactas en caso de accidentes o extravío.

### 3. Equipos de emergencia y contingencia
Organizaciones que operan en escenarios de desastres naturales o situaciones críticas donde la infraestructura de red convencional ha colapsado.
* **Perfil:** Brigadistas, bomberos, equipos de rescate y personal de organizaciones como **INDECI**.
* **Necesidad:** Una red de comunicación resiliente, privada y fácil de desplegar para coordinar operaciones de rescate.
* **Caso de Uso:** Establecimiento de una red de mensajería instantánea para la coordinación de brigadas durante inundaciones o sismos, donde las antenas de telefonía suelen quedar inoperativas.

### 4. Empresas de Logística y Operaciones en Campo (Segmento Adicional)
Empresas que poseen activos o personal en movimiento en zonas industriales o mineras remotas.
* **Perfil:** Supervisores de obra, transportistas en rutas críticas y personal de mantenimiento técnico.
* **Necesidad:** Monitoreo y comunicación de bajo costo energético y alta disponibilidad.
* **Caso de Uso:** Reporte de estado de maquinaria o confirmación de llegada a puntos de control en zonas mineras donde el satélite es demasiado costoso.

---
