
---



# Guía de Síntesis Granular en Surge XT y Referencias Bibliográficas

Este documento resume los métodos para realizar síntesis granular en el sintetizador de código abierto **Surge XT**, seguido de sus respectivas referencias en formato APA (7.ª edición).

---

## 1. Métodos de Síntesis Granular en Surge XT

### Método 1: Síntesis Granular mediante el Efecto "Nimbus" (Recomendado)
Este método procesa cualquier señal fuente a través del módulo integrado Nimbus, basado en el famoso procesador granular de hardware *Mutable Instruments Clouds*.

1. **Inicializar el parche:** Seleccione **Init -> Clean** en el navegador de presets para comenzar desde cero.
2. **Crear el sonido fuente:** Configure el *Oscilador 1* con una onda geométrica simple o un pad suave. Ajuste el envolvente de amplitud (*Amp Envelope*) con tiempos de ataque y liberación moderados para evitar clics.
3. **Cargar Nimbus:** En la sección **FX** (derecha de la interfaz), haga clic en un slot libre (ej. *FX A1*) y seleccione **Nimbus**.
4. **Configurar parámetros clave:**
   - **Mode:** Asegúrese de que se encuentre en el modo tradicional de granulador (*Granulizer*).
   - **Size (Tamaño):** Define la duración individual de cada grano.
   - **Density (Densidad):** Controla la frecuencia de generación de los granos. Valores altos crean una nube densa; valores bajos crean gotas aisladas.
   - **Position (Posición):** Escanea el búfer de audio guardado. Mapear un LFO lento a este parámetro genera texturas en constante evolución.
   - **Mix:** Sature el control hacia 50% o 100% *Wet* para aislar el resultado granular.

### Método 2: Estilo Granular vía Oscilador ("Window" o "Wavetable")
Para generar un comportamiento granular nativo desde la fuente sin depender de la sección de efectos:

- **Motor Window:** Cambie el tipo de oscilador a **Window**. Este motor fragmenta el ciclo de onda utilizando ventanas matemáticas (gaussianas, senoidales, etc.), actuando como un micro-granulador armónico. Modifique los controles **Form** y **Pitch/Ratio** para reestructurar los fragmentos.
- **Motor Wavetable (Escaneo de Tablas de Ondas):** Cargue una tabla de ondas compleja. Asigne un **LFO** lento o aleatorio al slider de **Morph** para escanear los índices de la tabla de forma caótica. Esto emula la aleatoriedad y el posicionamiento de un sampler granular tradicional.

---

## :book: Referencias Bibliográficas

- **Surge Synth Team**. (2026). *Surge XT User Manual*. GitHub Pages. [https://surge-synthesizer.github.io/manual-xt/](https://surge-synthesizer.github.io/manual-xt/)

- **Surge Synth Team**. (2021). *Nimbus - Mutable Instruments Clouds inspired granular effect* (Issue #3756). GitHub. [https://github.com/surge-synthesizer/surge/issues/3756](https://github.com/surge-synthesizer/surge/issues/3756)

- **Synth Anatomy**. (2021, 22 de abril). *Surge 1.9 Free Synth Plugin, 4 New OSC Types, New Effects (MI Clouds) & More*. [https://synthanatomy.com/2021/04/surge-1-9-free-synth-plugin-4-new-osc-types-new-effects-mi-clouds-more.html](https://synthanatomy.com/2021/04/surge-1-9-free-synth-plugin-4-new-osc-types-new-effects-mi-clouds-more.html)

- **VCV Library**. (2025). *Surge XT Window VCO*. [https://library.vcvrack.com/SurgeXTRack/SurgeXTOSCWindow](https://library.vcvrack.com/SurgeXTRack/SurgeXTOSCWindow)
