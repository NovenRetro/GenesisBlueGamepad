# Convierte tu mando original de Sega Genesis / Mega Drive en un gamepad Bluetooth para Nintendo Switch y BlueRetro

Este proyecto transforma un mando original de **Sega Genesis / Mega Drive de 6 botones** en un gamepad Bluetooth usando un **ESP32**, sin necesidad de agregar botones extra y conservando la estética original del control.

El firmware permite usar el mismo mando en **dos modos**:

- **Modo Nintendo Switch**, donde es reconocido como un **Pro Controller**
- **Modo BlueGamepad**, ideal para **BlueRetro, PC, Android y otros dispositivos Bluetooth compatibles**

Todo esto se logra reutilizando el mando original y manteniendo un esquema simple, compacto y funcional.

## ✨ Características

- Compatible con **Nintendo Switch**
- Compatible con **BlueRetro**
- Compatible con **PC y Android** en modo Bluetooth gamepad
- No requiere agregar botones adicionales
- Puede hacerse a partir de un mando original de **Sega Genesis / Mega Drive de 6 botones**
- Cambio de modo integrado por combinación de botones
- Atajos especiales para ampliar funciones en Switch
- Indicador visual mediante **LED RGB** usando:
  - **Rojo** para modo **Pro Controller**
  - **Azul** para modo **Bluetooth**
- Firmware instalable desde navegador mediante **ESP Web Tools**
- Basado en una adaptación y mejora del proyecto **BlueGamepad** de **@eolvera**

## 🎮 Modos de funcionamiento

Este firmware incluye dos modos:

### 1. Modo Nintendo Switch
En este modo, la consola lo reconoce como un **Pro Controller**.

Esto permite una compatibilidad mucho más amplia con el sistema, menús y juegos de Nintendo Switch.

### 2. Modo BlueGamepad
En este modo, el mando funciona como un **gamepad Bluetooth genérico**, útil para:

- BlueRetro
- PC
- Android
- otros dispositivos compatibles con Bluetooth HID

## 🔁 Cómo cambiar de modo

Para alternar entre los dos modos, mantén presionados:

**START + MODE durante 5 segundos**

El mando reiniciará automáticamente y arrancará en el otro modo.

## ⌨️ Atajos y combinaciones

### Atajos generales

| Acción | Combinación |
|---|---|
| Cambiar entre modo Switch y modo BlueGamepad | **START + MODE** durante **5 segundos** |

### Atajos en modo Nintendo Switch

| Función | Combinación |
|---|---|
| Capture | **MODE + LEFT** |
| Home | **START + MODE** pulsación corta |

## 🧩 Importante

Este mod fue pensado para mantener la esencia del mando original, por lo que:

- **no se agregan botones extra**
- se reutilizan únicamente los botones ya presentes en el control original
- ciertas funciones avanzadas se resuelven mediante **combinaciones de botones**

## 🎨 Indicador LED

El proyecto utiliza un **LED RGB de ánodo común**, usando solo dos colores:

- **Rojo** = modo **Pro Controller**
- **Azul** = modo **Bluetooth**

### Comportamiento del LED

- **Parpadeo lento** = buscando conexión
- **Encendido fijo** = conectado

## 🗺️ Mapeo de botones

### Modo Bluetooth / BlueRetro

| Botón físico Sega Genesis | Salida Bluetooth |
|---|---|
| Cruceta | D-Pad |
| A | **X** |
| B | **CIRCLE** |
| C | **L1** |
| X | **SQUARE** |
| Y | **TRIANGLE** |
| Z | **R1** |
| Start | **OPTIONS** |
| Mode | **SHARE** |

### Modo Nintendo Switch

| Botón físico Sega Genesis | Función en Switch |
|---|---|
| Cruceta | D-Pad |
| A | **A** |
| B | **B** |
| C | **L** |
| X | **X** |
| Y | **Y** |
| Z | **R** |
| Start | **+** |
| Mode | **-** |

## 🚀 Instalación rápida

Puedes flashear el ESP32 directamente desde el navegador usando **ESP Web Tools**.

➡️ **[Ir al instalador web](https://novenretro.github.io/famicom-gamepad-bluetooth-mod/)**

### Pasos

1. Conectá el ESP32 por USB
2. Hacé clic en **CONNECT**
3. Elegí el puerto correcto
4. Instalá el firmware
5. ¡Listo!

## 🛠️ Hardware utilizado

- ESP32
- mando original de **Sega Genesis / Mega Drive de 6 botones**
- batería de 3.7V
- módulo de carga **TP4056**
- LED RGB de **ánodo común**

## 📌 Compatibilidad

### Modo Switch
- Nintendo Switch
- Juegos compatibles con Pro Controller

### Modo BlueGamepad
- BlueRetro
- PC
- Android
- dispositivos compatibles con Bluetooth gamepad

## 🔌 Pinout del ESP32

| Función | GPIO ESP32 |
|---|---:|
| LED rojo | **2** |
| LED azul | **32** |
| Arriba | **13** |
| Abajo | **14** |
| Izquierda | **16** |
| Derecha | **17** |
| A | **18** |
| B | **19** |
| C | **21** |
| X | **22** |
| Y | **23** |
| Z | **25** |
| Start | **26** |
| Mode | **27** |

### LED RGB

Como el LED es **ánodo común**:

- **pata común** → **3.3V**
- **rojo** → **GPIO 2**
- **azul** → **GPIO 32**
- **verde** → sin conectar

### Botones

Todos los botones deben cablearse igual que en el proyecto anterior:

- un lado del botón al **GPIO correspondiente**
- el otro lado a **GND**

## 💡 Sobre este proyecto

Este firmware es una **adaptación personalizada** para mando original de Sega Genesis / Mega Drive, tomando como base el proyecto **BlueGamepad** de **@eolvera**, y ajustándolo para:

- trabajar con el cableado del mando original
- no requerir botones adicionales
- soportar cambio de modo integrado
- funcionar tanto en **Switch** como en **BlueRetro / PC / Android**
- presentar el mando como **Pro Controller** en Nintendo Switch
- incluir indicación visual por LED para identificar rápidamente el modo activo

## 📺 Video del proyecto

Puedes ver el proceso completo y el armado paso a paso en el canal:

**YouTube:** [NovenRetro](https://youtube.com/@novenretro)

## 👨‍💻 Autor

Proyecto adaptado y desarrollado por **@NovenRetro**  
Basado en el proyecto **BlueGamepad** de **@eolvera**