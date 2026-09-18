---
title: Política de privacidad de Renshu
permalink: /privacy
---

# Política de privacidad de Renshu

**Última actualización:** 18 de septiembre de 2026

Renshu se llamó **Forge** hasta septiembre de 2026. Es la misma app, el
mismo responsable y el mismo tratamiento de datos: solo cambió el nombre
público.

Este texto describe lo que Renshu hace de verdad con tus datos. Cada afirmación
sobre el comportamiento de la app está respaldada por el
mapa de datos interno de la app, que cita el código fuente.
No es asesoría legal.

## 1. Quién trata tus datos

**Victor Manrique**, desarrollador independiente con domicilio en Valencia,
Venezuela, es el responsable del tratamiento de los datos descritos aquí. Puedes
escribir a **victorjmanrique@gmail.com** para cualquier cuestión de privacidad o
para ejercer tus derechos.

Renshu se distribuye a través del App Store en todos los territorios donde el App
Store está disponible.

## 2. El principio: Renshu es local-first

Entrenar con Renshu **no requiere cuenta ni conexión**. Mientras no inicies
sesión, tus rutinas, tu historial y tus notas viven únicamente en la base de
datos local de tu iPhone y no se envía nada a nuestros servidores.

Cuando inicias sesión, sincronizamos un subconjunto concreto de esos datos para
que puedas usarlos en otro dispositivo. Este documento dice exactamente cuál.

## 3. Cómo inicias sesión

El **único** método de acceso es **Iniciar sesión con Apple**. No usamos
contraseñas, ni enlaces mágicos, ni ningún otro proveedor de identidad. Al
autenticarte, Apple nos entrega un identificador de usuario y, según lo que tú
autorices, tu nombre y una dirección de correo (que puede ser una dirección
enmascarada de Apple si eliges ocultar la tuya).

Ese correo se usa sólo para identificar la cuenta y mostrártela en Ajustes. No
lo almacenamos en ninguna tabla propia de Renshu: vive en el sistema de
autenticación de nuestro proveedor de backend.

La sesión (tokens de acceso y refresco) se guarda en el **Llavero de iOS**, no en
nuestros servidores.

## 4. Qué datos tratamos y para qué

### 4.1 Datos que sólo existen en tu dispositivo

- **Notas de técnica (Form Notes)**, con su texto y su foto o vídeo. **No se
  suben a ningún servidor.** La app te lo dice antes de guardarlas. El medio se
  copia dentro del contenedor de Renshu, la foto se reencoda a JPEG y el vídeo se
  vuelve a empaquetar **eliminando sus metadatos**, incluida la geolocalización.
  La copia original en tu app Fotos no se toca, y borrar la nota en Renshu no la
  borra de Fotos.
- **El entreno en curso**, hasta que lo terminas o lo descartas.
- **El historial de cambios que aceptas al Coach.** No existe una tabla remota
  para ello; es una decisión de diseño.
- **Tu preferencia de idioma y de apariencia.**

Estos datos **sí pueden aparecer en las copias de seguridad de tu dispositivo**
(iCloud o local), porque forman parte del contenedor de la app. Esa copia la
gestionas tú y Apple, no nosotros.

### 4.2 Datos que se sincronizan con nuestro backend cuando inicias sesión

| Dato | Para qué |
| --- | --- |
| Identificador de usuario | Separar tus datos de los de cualquier otra persona |
| Nombre para mostrar | Mostrarte en la app y en una rutina que compartas |
| Objetivo semanal, objetivo principal, nivel de experiencia, minutos por sesión, lugar de entrenamiento, equipamiento disponible, énfasis muscular, unidades | Personalizar el plan y las estadísticas |
| **Fecha de nacimiento, sexo, peso corporal y altura** | Calcular volumen relativo y ajustar las propuestas del Coach |
| **Áreas de cuidado** (hombro, codo, muñeca, lumbar, cadera, rodilla, tobillo) | Evitar proponerte ejercicios que agraven una molestia |
| **Nota libre para el Coach** (hasta 280 caracteres) | Contexto que tú escribes para el Coach |
| Rutinas: nombre, día, ejercicios, series y repeticiones objetivo, descanso, política de progresión | Sincronizar tu plan entre dispositivos |
| Historial: sesiones con su nombre de rutina, fechas, series con repeticiones y peso, tipo de actividad, distancia y notas de actividad | Conservar tu historial y calcular estadísticas |

Las cuatro filas en negrita son **datos de salud**. Los tratamos únicamente para
prestarte la funcionalidad de la app. **No los usamos para publicidad, no los
vendemos y no los compartimos con anunciantes ni intermediarios de datos.**

### 4.3 Datos de la app Salud de Apple

Si concedes el permiso, Renshu:

- **Lee** de Salud: energía activa, frecuencia cardiaca y distancia (caminar o
  correr, bicicleta, natación). La frecuencia cardiaca se consulta sólo en una
  ventana de los últimos diez minutos, durante el entreno.
- **Escribe** en Salud tu entreno terminado, para que aparezca en Fitness y
  cuente en tus anillos. En el Apple Watch, la sesión grabada incluye además las
  muestras de frecuencia cardiaca y energía que el reloj recoge.

**Nada de lo que leemos de Salud se envía a nuestros servidores.** Lo único que
se sincroniza es una referencia interna al entreno que escribimos, no las
muestras. Puedes revocar el permiso en cualquier momento desde Ajustes de iOS →
Salud; revocarlo no elimina lo ya escrito en Salud, que gestionas desde esa app.

### 4.4 Apple Watch y widgets

El Apple Watch recibe del iPhone lo necesario para dirigir el entreno: nombre de
la rutina, nombres de los ejercicios, series con repeticiones, peso y estado, y
los tiempos de descanso. Devuelve frecuencia cardiaca, energía activa y los
comandos que pulsas en la muñeca. **El reloj no se conecta a nuestro backend**, y
el único otro dato que cruza entre ambos es tu preferencia de idioma.

El widget lee una copia reducida del estado —rutina de hoy, rutina siguiente,
sesiones de la semana, objetivo, racha y qué días del mes entrenaste— desde un
contenedor compartido en tu dispositivo. Ese contenedor no sale del teléfono.

### 4.5 El Coach y Google Gemini

El Coach es una función opcional que **requiere tu permiso explícito**. La app te
muestra antes qué se envía y no lo envía hasta que aceptas.

Cuando pides una propuesta o escribes en el chat del Coach, tu dispositivo envía
a nuestro backend un contexto de entrenamiento y nuestro backend lo reenvía a
**Google Gemini** para generar la respuesta. Ese contexto incluye: tu edad
(calculada, no tu fecha de nacimiento), sexo, peso, altura, áreas de cuidado,
músculos restringidos, **tu nota libre tal cual la escribiste**, tu historial
agregado (sesiones de la semana, racha, volumen, récords recientes), tus rutinas
con sus identificadores internos y sus series, el catálogo de ejercicios
permitido, el idioma de respuesta y los mensajes del chat.

**No enviamos a Google tu identificador de cuenta, tu correo ni tu nombre.** La
petición al proveedor no lleva ningún identificador de usuario. Sí viajan los
identificadores internos de tus rutinas, que son seudónimos estables.

Por eso la app te advierte de que el texto que escribas puede identificarte y de
que evites incluir detalles personales que no quieras compartir. Retirar el
permiso detiene las peticiones futuras pero **no borra lo ya enviado**.

En este dispositivo conservamos los mensajes de tu conversación para que puedas
retomarla al cerrar y abrir el Coach. Se guardan separados por cuenta, sin
sincronizarlos con otros dispositivos, y se incluyen en la exportación JSON de
tus datos. Puedes borrarlos desde el chat; también se borran al retirar el
permiso del Coach. La eliminación de la cuenta aplica el proceso de eliminación
del almacenamiento local de esa cuenta. Los borradores pendientes y el contexto
de entrenamiento enviado no se conservan como parte de esta conversación local.

Nuestro servidor **no guarda ni el contexto ni la respuesta**. Guarda dos cosas:

- Una marca de tiempo por llamada, asociada a tu cuenta, para aplicar un límite
  de 20 peticiones por hora.
- Si tú reportas una respuesta como problemática, el **texto de esa respuesta**
  (hasta 4000 caracteres) y el motivo, asociados a tu cuenta. La pregunta no se
  guarda.

Google puede conservar temporalmente el contenido enviado a su API conforme a
los términos de la API de Gemini. No hemos contratado ningún plan que autorice
a Google a usar ese contenido para entrenar sus modelos.

### 4.6 Catálogo de ejercicios

Los nombres, músculos, equipamiento, instrucciones y medios de los ejercicios
proceden de **ExerciseDB**, a través de su API pública y de su distribución en
RapidAPI. Al buscar un ejercicio, tu dispositivo envía el término de búsqueda o
el identificador del ejercicio a esos servicios. **No enviamos ningún
identificador tuyo** en esas peticiones.

Las imágenes animadas de los ejercicios se cargan directamente desde el servidor
de ExerciseDB, por lo que **tu dirección IP llega a ese proveedor** al mostrarlas,
como ocurre con cualquier imagen alojada fuera de la app.

### 4.7 Compartir y exportar

- **Compartir una rutina** genera un código. Quien tenga ese código y una cuenta
  puede ver el nombre de la rutina, su día, sus ejercicios y series, **y tu
  nombre para mostrar**. No ve tu historial, tu perfil ni tus notas. Puedes dejar
  de compartirla desde la app, lo que anula el código; las copias que ya se
  importaron siguen existiendo en esas cuentas.
- **La tarjeta de compartir** de un entreno es una imagen que genera tu propio
  dispositivo y que envías con la hoja de compartir del sistema. Contiene el
  nombre de la rutina, la fecha, la duración, series, volumen y músculos, y, si
  tú la eliges, una foto tuya. **No lleva tu nombre, tu correo ni tu
  identificador**, y no pasa por ningún servidor nuestro.
- **La exportación de datos** produce un JSON y dos CSV con tu perfil completo
  —incluidos fecha de nacimiento, sexo, peso, altura, áreas de cuidado y tu nota
  del Coach— y todo tu historial. El fichero se guarda donde tú decides, sin
  pasar por la red. Las notas de técnica y sus adjuntos quedan fuera de esta
  exportación.

## 5. Qué NO hacemos

Verificado revisando todo el código de la app:

- **No hay publicidad ni rastreo.** No usamos IDFA, ni pedimos permiso de
  seguimiento, ni existe ningún SDK publicitario.
- **No hay analítica ni telemetría de producto**, ni herramienta de reporte de
  fallos de terceros.
- **No recogemos tu ubicación.** La app no usa servicios de localización.
- **No accedemos a tu cámara ni a tu fototeca.** El selector de fotos de iOS te
  deja entregar un elemento concreto sin darnos acceso a la biblioteca.
- **No enviamos notificaciones push desde un servidor.** El único aviso es local,
  para el final del descanso, y no requiere ningún identificador de dispositivo.
- **No vendemos datos personales** ni los compartimos con intermediarios.
- **No usamos CloudKit** para replicar el almacén local.

## 6. Encargados del tratamiento y dónde están tus datos

| Proveedor | Papel | Qué recibe |
| --- | --- | --- |
| **Apple** | Autenticación (Sign in with Apple), plataforma, app Salud, copias de seguridad del dispositivo | Identidad de acceso; los entrenos que escribimos en Salud quedan en tu dispositivo y bajo tu cuenta de Apple |
| **Supabase** | Base de datos, autenticación y funciones del backend | Todo lo descrito en 4.2, más el registro de uso del Coach y las respuestas que reportes |
| **Google** (API de Gemini) | Generación de las respuestas del Coach | Lo descrito en 4.5, sin identificador de cuenta |
| **ExerciseDB / RapidAPI** | Catálogo y medios de ejercicios | Términos de búsqueda e identificadores de ejercicio; tu IP al cargar medios |

Nuestro proyecto de Supabase está alojado en **Estados Unidos** (región
us-east-2). Google procesa las peticiones del Coach en su infraestructura global.
Si vives fuera de Estados Unidos, tus datos sincronizados se transfieren allí.
Usamos estos proveedores bajo sus términos de servicio estándar; no hemos
firmado acuerdos de tratamiento adicionales.

## 7. Base para tratar tus datos

Para quien esté cubierto por el RGPD u otra normativa equivalente:

- **Ejecución del contrato**: cuenta, sincronización de rutinas e historial.
- **Consentimiento explícito**: datos de salud del perfil, datos leídos de la app
  Salud y envío de contexto al Coach. Puedes retirarlo desde Ajustes de iOS
  (permisos de Salud) o desde Ajustes de Renshu (permiso del Coach).
- **Interés legítimo**: seguridad del servicio y control de abuso, que es lo que
  justifica el límite de peticiones del Coach.

## 8. Conservación y borrado

Puedes borrar tu cuenta desde Ajustes de la app. El borrado elimina el usuario en
nuestro backend y, con él, en cascada, tu perfil, rutinas, historial, registro de
uso del Coach y respuestas reportadas. En el mismo flujo la app elimina el
almacén local de esa cuenta y los medios de sus notas de técnica. Si la
respuesta del servidor se pierde a mitad del proceso, la app la recupera al
volver a abrirse y completa la limpieza sin repetir el borrado.

Límites que declaramos de forma explícita:

1. Conservamos un **recibo de borrado** que contiene únicamente un identificador
   interno de usuario y una huella criptográfica. Existe para poder completar un
   borrado cuya respuesta se perdió; no es legible por ningún cliente y no
   permite reconstruir ningún dato tuyo. Hoy no tiene un plazo de caducidad
   automático.
2. Al borrar la cuenta **no revocamos todavía la autorización de Iniciar sesión
   con Apple**. Puedes revocarla tú desde Ajustes de iOS → tu nombre → Iniciar
   sesión con Apple → Renshu.
3. El registro de uso del Coach y las respuestas reportadas se conservan
   mientras exista la cuenta y se eliminan al borrarla; no aplicamos hoy un
   plazo más corto.
4. Cerrar sesión no borra los datos locales de esa cuenta. Para eliminarlos sin
   borrar la cuenta, desinstala la app.
5. Las copias de seguridad de tu dispositivo y las de nuestro proveedor pueden
   conservar datos durante su propio ciclo de retención después de un borrado.

## 9. Tus derechos

Puedes acceder a tus datos, rectificarlos, borrarlos, limitar u oponerte a su
tratamiento y solicitar su portabilidad. La exportación descrita en 4.7 cubre por
sí sola el acceso y la portabilidad en formato legible por máquina; para lo
demás, escribe a victorjmanrique@gmail.com. También puedes reclamar ante la
autoridad de protección de datos de tu país de residencia.

## 10. Menores

Renshu está dirigida a **mayores de 16 años**. No recogemos a sabiendas datos de
personas por debajo de esa edad, y la app no comprueba la edad: si detectamos
una cuenta de un menor, la eliminaremos. Si eres padre, madre o tutor y crees
que un menor nos ha entregado datos, escríbenos.

## 11. Seguridad

- Toda la comunicación con el backend usa HTTPS.
- Cada usuario sólo puede leer y escribir sus propias filas, mediante políticas de
  seguridad a nivel de fila en la base de datos. El historial es de escritura
  restringida: sólo puede escribirse por la función de sincronización.
- El catálogo de ejercicios sólo es legible por usuarios autenticados.
- Los tokens de sesión y la prueba de borrado se guardan en el Llavero de iOS; la
  prueba de borrado está marcada para no sincronizarse con el Llavero de iCloud.
- Los medios de las notas de técnica y el diario de borrado se escriben con
  protección de datos de iOS. El almacén local principal usa la protección que
  iOS aplica por defecto.
- Los registros de nuestras funciones de servidor están escritos para **no**
  incluir el contenido de tus peticiones ni tu identidad.

Ninguna medida descrita constituye una certificación ni una auditoría de
seguridad.

## 12. Licencias y atribuciones

El registro completo de trabajos de terceros vive en
[NOTICE](NOTICE) y se muestra en Ajustes › Créditos:

- **MuscleMap**, de Melih Colpan (MIT), para la geometría del diagrama corporal.
- **Human Base Meshes v1.0.0** — *Body Male – Realistic*, de Julien Kaspar /
  Blender Studio (CC0), para la malla 3D del mapa muscular.
- **ExerciseDB**, para los datos y medios de ejercicios. Su licencia permite usar
  el conjunto dentro del producto pero no republicarlo como API abierta; por eso
  el catálogo sólo es legible por usuarios autenticados y los medios se enlazan
  en lugar de copiarse.
- Paquetes de Swift enlazados: **SVGPath** (MIT), **SDWebImageSwiftUI** y
  **SDWebImage** (MIT), **supabase-swift** (MIT) y sus dependencias
  **swift-crypto** (Apache-2.0), **swift-asn1**, **swift-http-types**,
  **swift-clocks**, **swift-concurrency-extras** y **xctest-dynamic-overlay**.
- La iconografía es de **SF Symbols**, de Apple, sujeta a sus condiciones de uso.

## 13. Cambios en esta política

La versión vigente está publicada en
<https://victjam.github.io/forge-legal/privacy> con su fecha. Los cambios
materiales se avisarán en la app antes de que surtan efecto.

## 14. Contacto

victorjmanrique@gmail.com — Victor Manrique, Valencia, Venezuela.
