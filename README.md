# Estadificación de melanoma cutáneo

Herramienta web de apoyo a la decisión clínica para estadificar el melanoma cutáneo
según la **8.ª edición de la AJCC** y obtener las recomendaciones de manejo de las
guías **EADO 2024** (partes 1 y 2), **ESMO 2024** y **SEOM-GEM 2023**. Cada
recomendación indica la guía de la que procede y su nivel de evidencia.

**Abrir la aplicación:** https://luciamc80.github.io/app-Melanoma/

## Qué hace

A partir de los datos del caso (edad, Breslow, ulceración, estado ganglionar,
metástasis, LDH y estado *BRAF*) la aplicación devuelve:

- **TNM y estadio**, clínico y patológico.
- **Veredicto de biopsia selectiva del ganglio centinela**: indicada, a discutir o no indicada.
- **Veredicto de linfadenectomía**: si procede o no el vaciamiento ganglionar, con el
  motivo y la guía que lo respalda.
- Recomendaciones de **cirugía del primario, manejo ganglionar y locorregional,
  estudio de extensión, tratamiento adyuvante o sistémico y seguimiento**.
- **Resumen imprimible** del caso.

## Uso en el móvil

Se abre desde el navegador con el enlace de arriba. Para dejarla como una app:

- **Android (Chrome):** menú ⋮ → *Añadir a pantalla de inicio*.
- **iPhone (Safari):** botón de compartir → *Añadir a pantalla de inicio*.

Instalada de este modo funciona **sin conexión**: el contenido completo se guarda en
el dispositivo la primera vez que se abre.

## Compartir un caso

El botón **Compartir caso** genera un enlace que lleva los datos del caso en la
propia dirección (después de `#`). Al abrirlo, la aplicación reproduce el caso tal
cual. En el móvil se abre directamente el menú de compartir del sistema.

Los datos del caso **no salen del dispositivo**: viajan dentro del enlace y solo
llegan a quien se lo envíe. La aplicación no tiene servidor, no guarda nada y no
registra ninguna información.

## Aviso

Herramienta de apoyo a la decisión. **No sustituye el juicio clínico ni la
valoración del comité multidisciplinar de tumores.** No es un producto sanitario
certificado y no debe usarse como única base de una decisión asistencial.

## Fuentes

- Garbe C, et al. EADO/EDF/EORTC 2024, partes 1 y 2. *Eur J Cancer* 2025;215:115152 y 115153.
- Amaral T, et al. ESMO Clinical Practice Guideline: cutaneous melanoma. *Ann Oncol* 2025;36:10-30.
- Márquez-Rodas I, et al. SEOM-GEM 2023. *Clin Transl Oncol* 2024;26:2841-2855.
- AJCC Cancer Staging Manual, 8.ª edición.

## Contenido del repositorio

| Archivo | Descripción |
| --- | --- |
| `index.html` | La aplicación completa (interfaz, lógica y recursos en un único archivo). |
| `manifest.webmanifest` | Datos de instalación como app (nombre, iconos, colores). |
| `sw.js` | *Service worker*: permite el uso sin conexión. |
| `icons/` | Iconos de la app. |
