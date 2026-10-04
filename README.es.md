<p align="center">
  <img src="assets/logo.png" width="96" alt="Logo de Printheon">
</p>

<h1 align="center">Printheon</h1>

<p align="center">
  <b>Una sola app para tu impresora 3D: control, laminado, calibración y reparaciones en el mismo sitio.</b>
</p>

<p align="center">
  <a href="README.md">Read in English</a> ·
  <a href="#funciones">Funciones</a> ·
  <a href="#impresoras-compatibles">Impresoras compatibles</a> ·
  <a href="#estado">Estado</a>
</p>

<p align="center">
  <img src="screenshots/dashboard.png" alt="Panel de Printheon" width="900">
</p>

---

Tener una impresora FDM suele significar ir saltando entre cinco programas: el laminador, el panel web de la impresora, una app del móvil para la cámara, una hoja de cálculo para el filamento y un montón de hilos de foro cada vez que algo falla.

Printheon junta todo eso en una app de escritorio. Conectas la impresora una vez y desde ahí preparas el modelo, lo mandas, lo vigilas y lo arreglas cuando da guerra. Lee todo lo que la impresora sabe de sí misma, así que no tienes que meter a mano los datos de tu máquina.

Está pensada para dos tipos de personas. El **modo sencillo** enseña solo lo necesario para imprimir y salir de un apuro. El **modo avanzado** abre todos los parámetros, las calibraciones, la sección de firmware y lo necesario para una granja de impresoras.

## Funciones

### Control de la impresora
- Temperaturas, ejes, ventiladores, luces, velocidad y flujo en directo, y parada de emergencia.
- Cámara en directo, fotos y timelapses.
- Archivos de la impresora y cola de impresión, incluida una cola que reparte trabajos entre varias impresoras.
- Un panel con todas tus impresoras.

<img src="screenshots/control.png" alt="Control de la impresora" width="800">

### Lee tu impresora por ti
Nada más conectarse, Printheon lee la máquina: volumen de impresión, boquilla, temperaturas máximas, versiones de firmware, offsets del sensor, malla de la cama y mucho más. Luego lo compara con la ficha oficial del fabricante y te avisa si algo no cuadra.

<img src="screenshots/printer-info.png" alt="Ficha de la impresora" width="800">

### Cuando algo va mal
Es la parte por la que nació Printheon. Cuando una impresora da un error, lo normal es acabar desenchufando cables y probando ventiladores a mano para ir descartando. Printheon lo automatiza:

- **Probar la impresora pieza a pieza:** conexión, termistores, cada ventilador por separado, calentadores de boquilla y cama, finales de carrera, sensor de nivelación, homing, movimiento, extrusor, sensor de filamento, luces y cámara. Cada prueba enciende, mide, te pregunta qué has visto y al terminar lo apaga todo.
- **Buscador de códigos de error:** códigos HMS de Bambu, números de error de Prusa y mensajes de Klipper y Marlin. Te explica el error y te propone las pruebas relacionadas.
- **Soluciones guiadas:** para primera capa que no pega, esquinas levantadas, hilos, falta de extrusión, capas desplazadas, espagueti, errores de temperatura y desconexiones.

<img src="screenshots/troubleshooting.png" alt="Diagnóstico y pruebas de la impresora" width="800">

### Desatascar y cambiar filamento
Desatasco automático o paso a paso según el síntoma: purgado en caliente, extrusión por pulsos, cold pull, atasco en el disipador o engranajes del extrusor. Las temperaturas siempre son las del material cargado. El cambio de filamento también es guiado, para cambiar de color sin atascos.

<img src="screenshots/unclog.png" alt="Asistente de desatasco" width="800">

### Calibración
- PID automático de boquilla y cama: la app lo lanza, aplica los valores y los guarda.
- Compensación de vibraciones (input shaper) con el acelerómetro de la impresora.
- Altura de la primera capa con un folio, y babystep que se puede guardar para siempre.
- Malla de la cama: medirla, verla y guardarla.
- Guías de pasos del extrusor, pressure advance y tensión de correas.

<img src="screenshots/calibration.png" alt="Calibración" width="800">

### Vigilancia de fallos
- **Detección de espagueti con la cámara.** Funciona en tu propio ordenador, sin internet ni suscripciones, y puede pausar la impresión por ti.
- **Vigilancia de la telemetría.** Te avisa si se pierde temperatura, si no se llega a la temperatura pedida, si un termistor está suelto, si la impresión deja de avanzar o si se cae la conexión.
- **Avisos al móvil** por Telegram, Discord o ntfy.

<img src="screenshots/failure-detection.png" alt="Vigilancia de fallos" width="800">

### Firmware y copias de seguridad
- Ficha de firmware por modelo: el firmware oficial, cómo actualizarlo, los firmwares alternativos con sus riesgos y los problemas conocidos.
- Aviso de actualizaciones para Klipper, Bambu Lab y OctoPrint.
- Copias automáticas de tu configuración (printer.cfg y macros, config de RRF, EEPROM de Marlin) para restaurarla cuando haga falta.

<img src="screenshots/firmware.png" alt="Firmware y copias de seguridad" width="800">

### Imprimir
- **Laminador integrado** con el motor de OrcaSlicer y perfiles adaptados a tu impresora y material.
- Comparador A/B de perfiles y coste estimado de cada pieza.
- **Buscador de modelos 3D:** Printables y Thingiverse por categorías dentro de la app, con enlaces a MakerWorld, Thangs, Cults3D y otras webs.
- Inventario de bobinas que descuenta lo que gasta cada impresión.
- Historial de impresiones y estadísticas.
- Mantenimiento con avisos según las horas de uso.
- Presupuestos con el coste real de cada pieza, tu margen y el IVA, y seguimiento de encargos para quien vende impresiones.

## La seguridad primero

Printheon no te deja estropear la impresora. Cada temperatura, velocidad, flujo y comando que envía se comprueba contra los límites oficiales de la impresora. Lo que se pase se bloquea, venga de un botón, de una macro, del terminal o de un archivo G-code.

## Impresoras compatibles

| Conexión | Impresoras |
|---|---|
| Klipper (Moonraker, Mainsail, Fluidd, RatOS) | Voron, RatRig, Sovol SV08, Elegoo Neptune 4, Qidi Plus4 / Q1 Pro y cualquier otra con Klipper |
| Bambu Lab en red local | X1, P1, A1, H2 |
| PrusaLink | MK4, MK3.5, MINI+, XL, CORE One |
| OctoPrint | Cualquier impresora con OctoPrint |
| Duet / RepRapFirmware | Duet 2, Maestro, Duet 3 |
| ESP3D | Placas WiFi de BigTreeTech, MKS y otras |
| Elegoo en red local | Centauri Carbon 2 |
| Cable USB | Impresoras con Marlin: Ender, Prusa MK3S, Anycubic, Artillery y más |

El catálogo integrado tiene la ficha oficial de unos 290 modelos de impresora de 58 marcas, cada uno con su fuente.

## Estado

Printheon está en pleno desarrollo y **todavía no está publicada**. La enseño ya para ver si le sirve a más gente y recoger ideas antes de la primera versión pública.

- Plataforma: Windows (app de escritorio).
- Idioma: español. El inglés viene después.
- Precio: gratis. Para quien quiera apoyar el desarrollo habrá un Patreon, sin funciones de pago.

## Ideas, fallos, impresoras

Abre un [issue](../../issues) si quieres:
- proponer una función,
- pedir que tu impresora sea compatible,
- contarme qué programas usas hoy que Printheon debería sustituir.

---

<sub>Capturas sacadas de la versión en desarrollo con el simulador de impresora integrado. © Printheon. Todos los derechos reservados.</sub>
