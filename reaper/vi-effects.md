# :sound: Cómo Aplicar Efectos a Pistas con Instrumentos Virtuales (VSTi) en REAPER


## Paso 1: Asegúrate de tener tu pista con el Instrumento Virtual

Antes de añadir efectos, ya debes tener una pista con tu instrumento virtual cargado y tus notas MIDI grabadas o dibujadas.

1. Si aún no lo has hecho, haz doble clic en el área vacía de la izquierda (TCP - *Track Control Panel*) para crear una pista.

2. Haz clic en el botón **FX** de esa pista, busca tu instrumento virtual (en la categoría *VSTi* o *AUi*) y cárgalo.

> En caso de no contar con alguna pista, se pueden descargar de forma gratuita de los siguientes vínculos:
> - [https://artlist.io](https://artlist.io/royalty-free-music/search?includedIds=552&utm_source=google&utm_medium=cpc&utm_campaign=23273290445&utm_content=191548708729&utm_term=sound%20effects%20for%20music%20production&keyword=sound%20effects%20for%20music%20production&ad=784546234283&matchtype=p&device=c&gad_source=1&gad_campaignid=23273290445&gbraid=0AAAAACumMRn0aqBTa2chyxyVcWxtpTjvY&gclid=Cj0KCQiAtvXXBhC2ARIsAJc8SUT2N8AcLOClU4ihQcg-EWIuZesRkgtuXJ4KPG6sEloRtMCeLkZT8aIaAmIbEALw_wcB)
> - [https://www.epidemicsound.com](https://www.epidemicsound.com/music/genres/cinematic/?utm_source=google&utm_medium=paidsearch&utm_campaign=23377461518&utm_term=&gad_source=1&gad_campaignid=23377461518&gbraid=0AAAAADk_3KnEuCzahwD4C_Ze4AexKq44s&gclid=Cj0KCQiAtvXXBhC2ARIsAJc8SUQRv6WzXiivXfT8WIqhGNArL8l17CrNJCdW6ScdxMzAJxaUoL3hYd0aAujgEALw_wcB)


## Paso 2: Abrir la cadena de efectos (FX Chain)

Para procesar el sonido que genera tu instrumento virtual:

1. Ve a la pista donde está tu instrumento virtual.

2. Haz clic nuevamente en el botón **FX** (que ahora estará iluminado en verde porque ya tiene el instrumento cargado).

3. Se abrirá la ventana **FX Chain** (Cadena de Efectos). En la lista de la izquierda verás el nombre de tu instrumento virtual.


## Paso 3: Añadir un efecto a la cadena

1. En la ventana *FX Chain*, haz clic en el botón **Add** (Añadir) ubicado en la parte inferior izquierda (o haz doble clic en el espacio vacío debajo del nombre de tu instrumento).

2. Se abrirá el navegador de plugins (*Add FX to Track*).

3. En el cuadro de búsqueda (**Filter**) en la parte inferior, escribe el nombre o tipo de efecto que deseas usar (por ejemplo: *ReaEQ* para ecualizar, *ReaComp* para comprimir, *ReaVerbate* para reverberación, etc.).

4. Haz doble clic sobre el efecto elegido (o selecciónalo y pulsa **OK**).


## Paso 4: Verificar el orden de la cadena (Muy Importante)

En REAPER, el audio fluye **de arriba hacia abajo** dentro de la lista de efectos. 
* **El instrumento virtual (VSTi) SIEMPRE debe estar en la parte superior (posición 1).** Este plugin es el que convierte las notas MIDI en sonido.

* **Los efectos (FX) deben ir DEBAJO del instrumento virtual.** 

* *Nota:* Si por error colocas un efecto de audio *encima* del instrumento virtual, no funcionará, ya que por encima del instrumento solo pasan datos MIDI, no audio. Si necesitas reordenarlos, simplemente haz clic y arrastra el efecto hacia abajo.


## Paso 5: Configurar los parámetros del efecto

1. Haz clic sobre el nombre del efecto recién añadido en la lista de la izquierda para ver su interfaz gráfica en el panel derecho.

2. Ajusta las perillas o deslizadores según lo que necesites (por ejemplo, cortar frecuencias graves en un ecualizador o añadir tiempo de cola en una reverb).

3. También puedes explorar los ajustes preestablecidos haciendo clic en el menú desplegable de **Presets** en la parte superior del plugin.


## Paso 6: Controlar la mezcla (Wet/Dry) en REAPER

REAPER incluye una herramienta nativa muy útil en la esquina superior derecha de cada ventana de plugin: la perilla **Wet** (Mezcla).

* Si un efecto (como una distorsión o reverberación) suena demasiado fuerte y el plugin no tiene su propio control de mezcla, gira la perilla **Wet** de REAPER hacia la izquierda para mezclar la señal original (seca) con la señal procesada (mojada).

---

## Método Alternativo (Avanzado): Usar Pistas de Envío (Sends)

Si quieres aplicar un mismo efecto (como una reverberación) a varios instrumentos virtuales a la vez para ahorrar recursos de CPU y dar cohesión a tu mezcla:

1. **Crea una pista auxiliar:** Haz doble clic en el área vacía de pistas y nómbrala (ej. *"Reverb General"*).

2. **Carga el efecto:** Haz clic en el botón **FX** de esta nueva pista y añade tu reverberación o delay. Asegúrate de configurar el efecto al **100% Wet** (solo sonido del efecto, sin señal seca).

3. **Envía el audio desde tu instrumento virtual:**
   * Haz clic y mantén presionado el botón **ROUTE** (o *I/O*) de la pista de tu instrumento virtual.
   * Arrastra y suelta ese botón directamente encima de la pista *"Reverb General"*.
   * Se abrirá una pequeña ventana de control de envío donde podrás ajustar el volumen (cantidad de efecto) que envías hacia esa pista.

---

## Consejos Adicionales

* **Activar/Desactivar efectos rápidamente:** En la ventana *FX Chain*, puedes desmarcar la casilla junto al nombre de cada efecto para escuchar el antes y el después (*Bypass*), o hacer `Shift + Clic` sobre el efecto en la lista.

* **Congelar pistas (Freeze):** Si usas muchos instrumentos virtuales y efectos pesados y tu computadora empieza a tener cortes de audio, haz clic derecho sobre la pista > **Render/freeze tracks** > **Freeze tracks to stereo**. Esto convertirá temporalmente el instrumento y sus efectos en un archivo de audio ligero, liberando memoria RAM y CPU.