<!-- Encabezado -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B3D2E,50:1B7F4B,100:3DDC84&height=190&section=header&text=Jonathan%20Javier%20Ramirez&fontSize=42&fontColor=ffffff&fontAlignY=36&desc=Desarrollador%20de%20apps%20m%C3%B3viles%20%C2%B7%20Scarab%20Solutions&descAlignY=58&descSize=18" alt="Jonathan Javier Ramirez"/>
</p>

<p align="center">
  <a href="https://github.com/Scarab-Solutions-LTD">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&duration=3500&pause=900&color=3DDC84&center=true&vCenter=true&width=720&lines=Android+nativo+con+Kotlin+y+Jetpack+Compose;Kotlin+Multiplatform+%2B+Compose+Multiplatform;Apps+offline-first+para+el+campo+agr%C3%ADcola;BLE%2C+GPS%2C+c%C3%A1mara+y+ML+Kit+en+producci%C3%B3n" alt="Typing SVG"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Scarab_Solutions-Mobile_Team-1B7F4B?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/Apps-8-3DDC84?style=for-the-badge&logo=googleplay&logoColor=white" />
  <img src="https://img.shields.io/badge/Commits-880%2B-7F52FF?style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Kotlin-100k%2B_l%C3%ADneas-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" />
</p>

---

## 👨‍💻 Sobre mí

Soy **desarrollador de aplicaciones móviles en [Scarab Solutions](https://github.com/Scarab-Solutions-LTD)**, empresa de tecnología para la **agricultura de precisión**. Construyo y mantengo el ecosistema de apps que usan a diario los equipos de campo: monitores, agrónomos, técnicos y supervisores que trabajan en fincas e invernaderos, muchas veces **sin conexión a internet**.

Mi trabajo va desde crear apps nuevas con **Kotlin Multiplatform y Compose Multiplatform** hasta modernizar bases de código con años en producción. Por ejemplo, migré a Kotlin y Clean Architecture apps que venían de Java.

- 🌱 **Offline-first de verdad:** Room y SQLDelight como fuente de verdad local, con sincronización en segundo plano, reintentos y recuperación automática.
- 📡 **Hardware en campo:** sensores Bluetooth LE, actualización de firmware por el aire (DFU), GPS con control de precisión y cámara con ML Kit.
- 🏗️ **Arquitectura limpia:** MVVM y Clean Architecture, casos de uso, inyección de dependencias con Hilt y Koin, y código testeable.
- 🔭 **Calidad y observabilidad:** tests unitarios y BDD, CI con GitHub Actions y SonarQube, y monitoreo con Crashlytics, Sentry y LogRocket.

---

## 🚜 Apps que desarrollo en Scarab Solutions

### 🟢 Scarab Control
> **Controles e inspecciones de campo con formularios dinámicos.**

App Android con la que los operarios capturan controles de calidad y de labores siguiendo la jerarquía agrícola **finca → casa → bloque → cultivo → variedad → producto**. Los formularios los define el servidor y la app los genera en tiempo de ejecución. Cada captura queda **georreferenciada** y se sincroniza cuando vuelve la conexión.

- Vinculación del dispositivo por **QR** con un escáner híbrido (Google Code Scanner, con respaldo en CameraX + ML Kit).
- **Login offline** con verificación local segura y **renovación automática de tokens**.
- **Motor de formularios** con campos de texto, número, fecha, rango, booleano y selección, más dependencias jerárquicas.
- **Sincronización** manual y en segundo plano con WorkManager, errores claros en cada fase y recuperación automática del acceso a las fincas.
- Recordatorios diarios programables, notificaciones y **actualizaciones dentro de la app**.
- **CI con GitHub Actions**: tests unitarios, cobertura con JaCoCo y análisis en SonarQube en cada PR.

`Kotlin` `Jetpack Compose` `Material 3` `Hilt` `Room` `WorkManager` `Retrofit` `CameraX` `ML Kit` `Fused Location` `Firebase` `LogRocket` `JUnit 5` `Turbine` `SonarQube`

---

### 🟢 Scarab Precision · Scarab Crop Husbandry · Scarab White Rust
> **Tres apps publicadas desde un solo código base.**

Apps de **monitoreo (scouting) de cultivos en invernadero**. El monitor recorre la finca, la casa y la cama, y registra observaciones de **presencia, conteo y puntuación** según plantillas, en paradas **georreferenciadas**. Las tres apps comparten el código y se generan con **product flavors**: cada una tiene su propia identidad visual y su firma de publicación, y la app comprueba en el alta que el cliente pertenezca a ese producto.

- **GPS pensado para el campo:** descarta posiciones antiguas o simuladas, exige una precisión mínima, cuenta los satélites y sugiere la cama más cercana (Haversine).
- **Offline-first** con Room, migraciones versionadas y **tests de migración**.
- Alta por **QR**, órdenes de trabajo, resumen por cama y casa, y reenvío de datos por fecha.
- Exportación de diagnóstico en **ZIP cifrado con AES-256**.
- Firma de release por app, preparada para CI y válida en Windows, Linux y macOS.

`Kotlin` `Product Flavors` `Room` `Coroutines` `OkHttp` `LocationManager / GNSS` `ZXing` `Sentry` `zip4j`

---

### 🟢 Scarab Planting
> **Registro de siembra, cosecha y erradicación en finca.**

App de campo de la suite de precisión, con la que el personal registra las **labores de siembra, cosecha y erradicación** por finca, invernadero, sector, variedad y trabajador. Guarda cada operación como una acción pendiente y la procesa con una **cadena de sincronización en WorkManager** que sube, notifica y descarga, con restricciones de red y reintentos.

- Emparejamiento por **QR** con escáner híbrido y **login offline**.
- **Calculadora de tallos** por malla, sobrantes y totales, con borrador persistente.
- **Sincronización bidireccional** de datos maestros, con análisis de la causa raíz de cada fallo y re-emparejamiento silencioso.
- **Modo QA** oculto con exportación cifrada de evidencias.
- **Observabilidad avanzada:** detección de bloqueos del hilo principal, análisis de ANR y grabación de sesiones con LogRocket.
- Tests unitarios de los workers y **tests BDD con Cucumber** sobre Android.

`Kotlin` `Jetpack Compose` `Hilt` `Room` `DataStore` `WorkManager` `Retrofit` `kotlinx.serialization` `Arrow` `CameraX` `ML Kit` `Firebase` `LogRocket` `MockK` `Cucumber`

---

### 🟢 Scarab Audit
> **Auditoría de campo multiplataforma con Kotlin Multiplatform.**

App **KMP + Compose Multiplatform** con **un solo código para Android, iOS, escritorio y web (Wasm)**. El auditor elige una finca y unas fechas, y la app genera un **tablero de auditoría** organizado por monitor, bloque y cama. Sobre él valida o corrige las mediciones **píxel a píxel**, con marcas, comentarios, dibujo a mano alzada y fotos.

- **Tablero dibujado con Canvas** y gestos precisos, que convierten las coordenadas de pantalla a píxeles del dato.
- **Comentarios a mano alzada** que se exportan como imagen, y fotos por celda.
- **UI adaptativa:** panel en árbol en tablet y escritorio, y selectores en el móvil.
- Remoto primero, con **caché local en SQLDelight** y un driver distinto por plataforma.
- Código específico de cada plataforma con `expect/actual`: cámara, orientación y módulos de DI.

`Kotlin Multiplatform` `Compose Multiplatform` `Android` `iOS` `Desktop` `Wasm` `Ktor` `SQLDelight` `Koin` `kotlinx.serialization` `Coroutines` `Napier`

---

### 🟢 Scarab Tracker
> **Puente Bluetooth LE entre los sensores de campo y la nube.**

Es la app **gateway** entre los **sensores portátiles Bluetooth LE** instalados en las fincas y la plataforma web de Scarab Solutions. Busca los sensores cercanos, descarga los datos que tienen guardados, los almacena en el teléfono y los sube a la nube. También mantiene los sensores operativos: configuración, calibración y **actualización de firmware por el aire**.

- **Hasta 8 sesiones BLE en paralelo**, con un mutex por sensor y subidas concurrentes limitadas por semáforo.
- **Protocolo BLE propio:** comandos de configuración, reensamblado de los datos, CRC16 y control de integridad (MD5).
- **Actualización de firmware con Nordic DFU** integrada en el mismo ciclo de trabajo.
- **Migración completa de Java a Kotlin** y Clean Architecture: clases de más de 5.000 líneas divididas en módulos pequeños.
- Modo diagnóstico con cronómetros por fase y un catálogo de errores traducidos a mensajes para el usuario.

`Kotlin` `Nordic BLE Library` `Nordic DFU` `Hilt` `Room` `Coroutines` `StateFlow` `Retrofit` `Material 3` `Firebase Crashlytics` `MockK`

---

### 🟢 spot.ag scout
> **Scouting de plagas y enfermedades con mapas y GPS.**

App de campo de la plataforma **spot.ag** para **inspeccionar cultivos y detectar plagas y enfermedades**. Los scouts recorren los lotes y registran observaciones **georreferenciadas por punto de parada** según plantillas de evaluación. También capturan **fotos y video** de las muestras y **dibujan los lotes en el mapa caminando con GPS**.

- **Google Maps** con tiles en caché para trabajar sin conexión, y cálculo de área, perímetro y centroide en el dispositivo.
- **Integridad de los datos:** bloqueo de ubicaciones simuladas y hora obtenida por **SNTP**.
- Seis tipos de evaluación: booleano, conteo, rango, puntaje, puntaje con etiqueta y selección.
- **CameraX** para foto y video, y subida de archivos a **Firebase Cloud Storage**.
- **Migraciones de Room** probadas para no perder datos históricos, y soporte para 4 idiomas.

`Java` `Kotlin` `Google Maps SDK` `Fused Location` `CameraX` `Room` `RxJava 3` `WorkManager` `Retrofit` `Firebase Storage` `Crashlytics`

---

## 📊 Mi aporte en números

```mermaid
pie showData
    title Mis commits por app
    "Scarab Control" : 363
    "Scarab Planting" : 270
    "Scarab Precision (3 apps)" : 103
    "Scarab Tracker" : 97
    "Scarab Audit" : 37
    "spot.ag scout" : 18
```

```mermaid
gantt
    title Mi participación en cada proyecto
    dateFormat YYYY-MM-DD
    axisFormat %b %Y
    section Android nativo
    Scarab Control            :active, 2025-03-18, 2026-09-28
    Scarab Precision (3 apps) :active, 2025-04-01, 2026-09-28
    Scarab Planting           :active, 2025-04-30, 2026-09-28
    spot.ag scout             :active, 2025-08-04, 2026-09-28
    Scarab Tracker            :active, 2026-03-02, 2026-09-28
    section Multiplataforma
    Scarab Audit (KMP/CMP)    :done,   2025-11-11, 2026-03-19
```

| | Scarab Control | Scarab Precision ×3 | Scarab Planting | Scarab Audit | Scarab Tracker | spot.ag scout |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| **Jetpack Compose** | ✅ | | ✅ | | | |
| **Compose Multiplatform** | | | | ✅ | | |
| **Offline-first** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Sync en segundo plano** | ✅ | ✅ | ✅ | | ✅ | ✅ |
| **QR** | ✅ | ✅ | ✅ | | ✅ | ✅ |
| **GPS** | ✅ | ✅ | | | | ✅ |
| **Mapas** | | | | | | ✅ |
| **Bluetooth LE / DFU** | | | | | ✅ | |
| **ML Kit / CameraX** | ✅ | | ✅ | ✅ | | ✅ |
| **Firebase** | ✅ | | ✅ | | ✅ | ✅ |
| **Inyección de dependencias** | Hilt | | Hilt | Koin | Hilt | |
| **Clean Architecture** | ✅ | | ✅ | ✅ | ✅ | |

---

## 🛠️ Stack tecnológico

**Lenguajes y plataformas**

<p>
  <img src="https://skillicons.dev/icons?i=kotlin,java,swift,androidstudio,idea,gradle&theme=dark" />
</p>

[![Kotlin Multiplatform](https://img.shields.io/badge/Kotlin_Multiplatform-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white&labelColor=101010)]()
[![Compose Multiplatform](https://img.shields.io/badge/Compose_Multiplatform-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white&labelColor=101010)]()
[![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white&labelColor=101010)]()
[![iOS](https://img.shields.io/badge/iOS-000000?style=for-the-badge&logo=apple&logoColor=white&labelColor=101010)]()
[![Wasm](https://img.shields.io/badge/WebAssembly-654FF0?style=for-the-badge&logo=webassembly&logoColor=white&labelColor=101010)]()

**UI**

[![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white&labelColor=101010)]()
[![Material 3](https://img.shields.io/badge/Material_3-757575?style=for-the-badge&logo=materialdesign&logoColor=white&labelColor=101010)]()
[![XML Views](https://img.shields.io/badge/XML_Views_%26_ViewBinding-3DDC84?style=for-the-badge&logo=android&logoColor=white&labelColor=101010)]()
[![Navigation](https://img.shields.io/badge/Navigation-3DDC84?style=for-the-badge&logo=android&logoColor=white&labelColor=101010)]()

**Arquitectura, datos y concurrencia**

[![Hilt](https://img.shields.io/badge/Hilt-3DDC84?style=for-the-badge&logo=android&logoColor=white&labelColor=101010)]()
[![Koin](https://img.shields.io/badge/Koin-F58220?style=for-the-badge&logo=kotlin&logoColor=white&labelColor=101010)]()
[![Room](https://img.shields.io/badge/Room-3DDC84?style=for-the-badge&logo=sqlite&logoColor=white&labelColor=101010)]()
[![SQLDelight](https://img.shields.io/badge/SQLDelight-003B57?style=for-the-badge&logo=sqlite&logoColor=white&labelColor=101010)]()
[![DataStore](https://img.shields.io/badge/DataStore-3DDC84?style=for-the-badge&logo=android&logoColor=white&labelColor=101010)]()
[![Coroutines](https://img.shields.io/badge/Coroutines_%26_Flow-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white&labelColor=101010)]()
[![WorkManager](https://img.shields.io/badge/WorkManager-3DDC84?style=for-the-badge&logo=android&logoColor=white&labelColor=101010)]()
[![RxJava](https://img.shields.io/badge/RxJava-B7178C?style=for-the-badge&logo=reactivex&logoColor=white&labelColor=101010)]()
[![Arrow](https://img.shields.io/badge/Arrow-2D7BF4?style=for-the-badge&logo=kotlin&logoColor=white&labelColor=101010)]()

**Red**

[![Retrofit](https://img.shields.io/badge/Retrofit_%2F_OkHttp-48B983?style=for-the-badge&logo=square&logoColor=white&labelColor=101010)]()
[![Ktor](https://img.shields.io/badge/Ktor_Client-087CFA?style=for-the-badge&logo=ktor&logoColor=white&labelColor=101010)]()
[![kotlinx.serialization](https://img.shields.io/badge/kotlinx.serialization-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white&labelColor=101010)]()
[![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white&labelColor=101010)]()

**Hardware, sensores y visión**

[![Bluetooth LE](https://img.shields.io/badge/Bluetooth_LE-0082FC?style=for-the-badge&logo=bluetooth&logoColor=white&labelColor=101010)]()
[![Nordic DFU](https://img.shields.io/badge/Nordic_BLE_%2F_DFU-00A9CE?style=for-the-badge&logo=nordicsemiconductor&logoColor=white&labelColor=101010)]()
[![CameraX](https://img.shields.io/badge/CameraX-3DDC84?style=for-the-badge&logo=android&logoColor=white&labelColor=101010)]()
[![ML Kit](https://img.shields.io/badge/ML_Kit-4285F4?style=for-the-badge&logo=google&logoColor=white&labelColor=101010)]()
[![Google Maps](https://img.shields.io/badge/Google_Maps-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white&labelColor=101010)]()
[![GPS](https://img.shields.io/badge/GPS_%2F_GNSS-34A853?style=for-the-badge&logo=googlemaps&logoColor=white&labelColor=101010)]()

**Firebase y observabilidad**

[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black&labelColor=101010)]()
[![Crashlytics](https://img.shields.io/badge/Crashlytics-FFCA28?style=for-the-badge&logo=firebase&logoColor=black&labelColor=101010)]()
[![Sentry](https://img.shields.io/badge/Sentry-362D59?style=for-the-badge&logo=sentry&logoColor=white&labelColor=101010)]()
[![LogRocket](https://img.shields.io/badge/LogRocket-764ABC?style=for-the-badge&logoColor=white&labelColor=101010)]()

**Testing, CI y herramientas**

<p>
  <img src="https://skillicons.dev/icons?i=git,github,githubactions,postman,vscode&theme=dark" />
</p>

[![JUnit 5](https://img.shields.io/badge/JUnit_5-25A162?style=for-the-badge&logo=junit5&logoColor=white&labelColor=101010)]()
[![MockK](https://img.shields.io/badge/MockK_%2F_Mockito-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white&labelColor=101010)]()
[![Cucumber](https://img.shields.io/badge/Cucumber_BDD-23D96C?style=for-the-badge&logo=cucumber&logoColor=white&labelColor=101010)]()
[![Espresso](https://img.shields.io/badge/Espresso_%2F_Compose_UI_Test-3DDC84?style=for-the-badge&logo=android&logoColor=white&labelColor=101010)]()
[![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white&labelColor=101010)]()
[![JaCoCo](https://img.shields.io/badge/JaCoCo-C21325?style=for-the-badge&logoColor=white&labelColor=101010)]()

---

## 📈 Actividad en GitHub

<p align="center">
  <img src="https://streak-stats.demolab.com?user=JonathanJR10&theme=dark&hide_border=true&background=0D1117&ring=3DDC84&fire=3DDC84&currStreakLabel=3DDC84&sideLabels=FFFFFF&dates=9E9E9E&locale=es" alt="Rachas de contribución" />
</p>

<p align="center">
  <img src="https://ghchart.rshah.org/1B7F4B/JonathanJR10" alt="Calendario de contribuciones" width="100%" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/JonathanJR10/JonathanJR10/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/JonathanJR10/JonathanJR10/output/github-snake.svg" />
    <img alt="Serpiente de contribuciones" src="https://raw.githubusercontent.com/JonathanJR10/JonathanJR10/output/github-snake-dark.svg" width="100%" />
  </picture>
</p>

---

## 📫 Contacto

<p>
  <a href="mailto:jonathan.ramirez@scarab-solutions.com"><img src="https://img.shields.io/badge/jonathan.ramirez@scarab--solutions.com-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=101010" /></a>
  <a href="https://www.linkedin.com/in/jonathan-ramirez-b01286202/"><img src="https://img.shields.io/badge/LinkedIn-Jonathan_Ramirez-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=101010" /></a>
  <a href="https://github.com/Scarab-Solutions-LTD"><img src="https://img.shields.io/badge/GitHub-Scarab--Solutions--LTD-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=101010" /></a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:3DDC84,50:1B7F4B,100:0B3D2E&height=110&section=footer" />
</p>
