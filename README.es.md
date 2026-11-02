[English](README.md) · **Español** · [Français](README.fr.md) · [Deutsch](README.de.md) · [日本語](README.ja.md) · [中文](README.zh.md) · [हिन्दी](README.hi.md)

# U-MA Hanon

Los 60 ejercicios de *El pianista virtuoso* de Charles-Louis Hanon, en el navegador: los ves en el pentagrama, ves **las dos manos sobre el teclado** con cada dedo numerado, los escuchás al tempo que elijas y, con un teclado MIDI, la app te escucha y analiza tu toma.

**▶ Abrir la app:** https://buenosairesfront.github.io/hanon/

No hay que instalar nada. La interfaz está en castellano.

## Cómo funciona

1. **Elegí un ejercicio.** Los 60 están agrupados en las tres partes del libro: **I · 1–20** preparatorios (magenta), **II · 21–43** avanzados (cian) y **III · 44–60** virtuosismo (amarillo). Tocá un número debajo del teclado, o tocá el número grande de arriba para abrir la grilla completa 1–60.
2. **Elegí una variante** cuando el ejercicio la tiene: las escalas (39) y los arpegios (41) vienen en las 24 tonalidades en el orden del libro (cada mayor seguida de su relativa menor; las menores en forma armónica y melódica), las cromáticas (40) en 8 intervalos y direcciones, las notas repetidas (45) en 6 digitaciones, las terceras o sextas picadas (48)…
3. **Leé la partitura.** Dos pentagramas muestran el ejercicio: **↑ ida** (cian) y **↓ vuelta** (magenta). En el celular se cambia entre uno y otro con pestañas.
4. **Mirá las manos.** El teclado es el centro de la app. Las dos manos están dibujadas sobre las teclas con sus palmas, cada dedo muestra su número (1 = pulgar … 5 = meñique, cada uno con su color) y un contorno punteado marca **la próxima posición de la mano**. Debajo del teclado, una fila por mano muestra el orden de dedos del grupo actual y enciende la nota que está sonando.
5. **Hacelo sonar.**
   - **▶ 2 pasadas**: una demo corta con los dos primeros y los dos últimos grupos, para escuchar la forma rápido.
   - **↑ subida** / **↓ bajada**: una sola dirección.
   - **↑↓×2**: el ejercicio completo, dos veces.
   - **loop** repite hasta que aprietes **stop**.
6. **Ajustá el tempo** de 40 a 160 BPM con el deslizador o con – / +. La franja amarilla de abajo marca el rango que pide Hanon (60 → 108): empezá lento y subí de a poco. El metrónomo **MET** parpadea y suena en el compás del ejercicio (2/4, 3/4, 4/4 o 6/8), con el acento en magenta.

## Practicar con un teclado MIDI

Apretá **MIDI** y dale permiso. A partir de ahí:

- las teclas que tocás se encienden en cian en el teclado de la pantalla;
- **REC** hace sonar el ejercicio como guía y graba lo que tocás encima;
- al terminar aparece el **análisis de tu toma**: precisión (%), desvío promedio (ms), qué tan parejo (%) y errores; un gráfico de tiempo (antes ↓ / después ↑ en cada nota), retraso y fuerza por dedo, y la dinámica de cada mano (derecha arriba, izquierda abajo).

Sin MIDI podés apretar **nueva toma de ejemplo** para ver cómo es el análisis.

## Claro y oscuro

El botón **claro / oscuro** cambia el tema; la elección queda guardada en ese navegador.

## Por dentro

Un solo `index.html` sin dependencias: los ejercicios no están guardados nota por nota sino que se **generan**. Cada uno es una célula melódica (en grados de la escala) más su digitación para cada mano; el motor la sube un grado por compás y la vuelve a bajar, y escribe cada nota con la alteración correcta (sostenidos al subir y bemoles al bajar en las cromáticas). Escalas, arpegios y ejercicios en octavas se arman para cada una de las 24 tonalidades con las digitaciones tradicionales. La partitura se dibuja en SVG, el teclado y el análisis en `<canvas>`, el sonido y el metrónomo con Web Audio, y la entrada del teclado con Web MIDI.

## Correr en local

Bajá `index.html` y abrilo, o serví la carpeta:

```
python3 -m http.server 8000
```

<!-- u-ma:more -->
**Más de U-MA:** todos los instrumentos y herramientas en un solo lugar → [muestrario U-MA](https://github.com/buenosairesfront/U-ma/blob/main/README.es.md)
<!-- /u-ma:more -->

## Créditos

Ejercicios de *Le Pianiste virtuose en 60 exercices* de Charles-Louis Hanon (1873, dominio público). App de U-MA サウンド · [Buenos Aires Front](https://www.instagram.com/buenos.aires.front/).
