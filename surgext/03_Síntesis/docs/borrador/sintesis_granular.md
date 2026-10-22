# Síntesis Granular en Acústica

La **síntesis granular** es una técnica de síntesis acústica y digital que consiste en **descomponer un sonido en fragmentos microscópicos llamados "granos"** para luego modificarlos, multiplicarlos y reorganizarlos en el tiempo, creando texturas sonoras completamente nuevas. 

A diferencia de la síntesis tradicional que utiliza osciladores básicos (como ondas senoidales o cuadradas), la síntesis granular trata el audio bajo el concepto de **"cuantos o partículas de sonido"**, una idea introducida originalmente por el físico Dennis Gabor.

---

## Características Clave de un Grano

Para entender cómo funciona, cada grano individual posee las siguientes propiedades:

- **Duración extremadamente corta:** Generalmente oscila entre **1 y 100 milisegundos**. Si fueran más largos, el oído humano los percibiría como un fragmento musical (un *sample* común) y no como una partícula acústica.

- **Ventana o Envolvente:** Cada grano cuenta con una rampa de volumen al inicio y al final (ataque y decaimiento). Esto evita los clics o chasquidos digitales que ocurrirían si el audio se cortara abruptamente.

- **Parámetros modificables:** Cada partícula se puede alterar individualmente en su **tono (*pitch*)**, **dirección** (reproducción al derecho o al revés), **paneo estéreo** y **volumen**.

Cuando miles de estos granos se reproducen de forma simultánea y superpuesta, se genera lo que acústicamente se conoce como una **nube sonora**.

---

## Diagrama Conceptual del Proceso

El flujo de señal de un sintetizador granular se estructura de la siguiente manera:

```text
[ AUDIO DE ENTRADA ]  (Un archivo de sonido, muestra o señal en vivo)
         │
         ▼
 ┌───────────────┐
 │ Fragmentador  │ ──► Divide el audio en miles de partes (1 a 100 ms)
 └───────────────┘
         │
         ▼
  [ GRANOS INDIVIDUALES ]  (Múltiples partículas acústicas aisladas)
         │
         ├───► [Modificador de Ventana/Envolvente] (Suaviza los bordes del grano)
         ├───► [Modificador de Pitch / Dirección] (Cambia velocidad, tono o reversa)
         └───► [Control de Densidad] (Define cuántos granos se disparan por segundo)
         │
         ▼
 ┌──────────────────────┐
 │ Motor de Distribución│ ──► Distribuye los granos en el tiempo de forma:
 └──────────────────────┘     ├─► Sincrónica (Frecuencias regulares y rítmicas)
                              └─► Asincrónica (Espaciado aleatorio / Nube de sonido)
         │
         ▼
 ┌──────────────────────┐
 │  Mezclador / Salida  │ ──► Superpone los granos (Polifonía granular)
 └──────────────────────┘
         │
         ▼
   [ NUEVA TEXTURA SONORA ]  (Paisajes sonoros, nubes, drones o efectos glitch)
```

---

## Métodos de Organización Temporal

Una vez que el motor tiene los granos listos, los organiza principalmente mediante dos métodos:

* **Método Sincrónico:** Los granos se disparan en intervalos de tiempo fijos y regulares. Esto suele generar flujos sonoros estables y con una percepción de tono o ritmo definido.
* **Método Asincrónico:** Las partículas se esparcen de manera estadística o aleatoria en el tiempo. Es el método ideal para diseñar efectos ambientales, *soundscapes* (paisajes sonoros) y densas nubes de sonido abstractas.
