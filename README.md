# R2-A1-S7-Tarea-Resolucion-de-ejercicios-practicos-con-OpenCV

<div align="center">

# Resolución de ejercicios prácticos con OpenCV

**R2-A1-S7 · Semana 7 · Práctica guiada de procesamiento de imágenes**

CADI Percepción Computacional · Experiencia IMAGEN
Especialización en Inteligencia Artificial · Universidad de Cundinamarca

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-4.14.0-5C3EE8?logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-2.1.3-013243?logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-plots-11557C)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google-Colab-F9AB00?logo=googlecolab&logoColor=white)

[Informe (PDF)](R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Informe/R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV_final.pdf) · [Informe (Word)](R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Informe/R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV_final.docx) · [Notebook Imagen 1](R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Copia_de_Semana_7_OpenCV_Practica_Guiada.ipynb) · [Notebook Imagen 2](R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Semana_7_OpenCV_Practica_Guiada_1.ipynb)

</div>

---

## Tabla de contenido

1. [Descripción](#descripción)
2. [Objetivos](#objetivos)
3. [Estructura del repositorio](#estructura-del-repositorio)
4. [Imágenes de prueba](#imágenes-de-prueba)
5. [Flujo de procesamiento](#flujo-de-procesamiento)
6. [Resultados](#resultados)
7. [Cómo reproducir la práctica](#cómo-reproducir-la-práctica)
8. [Informe](#informe)
9. [Hallazgos y recomendaciones](#hallazgos-y-recomendaciones)
10. [Tecnologías](#tecnologías)
11. [Autores y contexto académico](#autores-y-contexto-académico)
12. [Referencias](#referencias)

---

## Descripción

Este repositorio reúne el trabajo de la **Semana 7** del CADI *Percepción Computacional*: una práctica guiada en la que una imagen digital se trata como un **arreglo numérico** y se transforma paso a paso con **OpenCV** en Python.

El mismo flujo de trabajo se ejecutó sobre **dos fotografías propias** de contenido, resolución e iluminación muy distintos, para comparar cómo se comporta cada operación. El repositorio incluye los dos cuadernos de Google Colab con sus salidas, las imágenes generadas en cada etapa y el informe final redactado en formato **APA 7**.

## Objetivos

- Comprender cómo se representa una imagen como datos: forma `(alto, ancho, canales)`, tipo de dato y valores de píxel.
- Aplicar operaciones básicas de OpenCV: carga, conversión de color, redimensionamiento, recorte, filtrado, umbralización, detección de bordes y contornos.
- Interpretar qué hace cada transformación y **qué información permite observar**, y no solo mostrar capturas.
- Documentar el proceso, los resultados, las dificultades y las recomendaciones en un informe.

## Estructura del repositorio

```text
.
├── README.md
└── R2-A1-S7 Tarea – Resolución de ejercicios prácticos con OpenCV/
    ├── Copia_de_Semana_7_OpenCV_Practica_Guiada.ipynb      # Notebook · Imagen 1 (figuras sobre un parlante)
    ├── Semana_7_OpenCV_Practica_Guiada_1.ipynb             # Notebook · Imagen 2 (escritorio de trabajo)
    ├── Informe/
    │   ├── R2-A1-S7 Tarea – Resolución de ejercicios prácticos con OpenCV_final.docx
    │   └── R2-A1-S7 Tarea – Resolución de ejercicios prácticos con OpenCV_final.pdf
    ├── resultados_opencv/                                  # Evidencias de la Imagen 1
    │   └── resultados_opencv/
    │       ├── 01_original.png … 08_contornos.png
    └── resultados_opencv (1)/                              # Evidencias de la Imagen 2
        └── resultados_opencv/
            └── 002_gris.png … 008_contornos.png
```

| Ruta | Contenido |
|---|---|
| [`Copia_de_Semana_7_OpenCV_Practica_Guiada.ipynb`](R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Copia_de_Semana_7_OpenCV_Practica_Guiada.ipynb) | Práctica completa ejecutada con la **Imagen 1** (3000 × 4000 px). |
| [`Semana_7_OpenCV_Practica_Guiada_1.ipynb`](R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Semana_7_OpenCV_Practica_Guiada_1.ipynb) | La misma práctica ejecutada con la **Imagen 2** (8000 × 6000 px). |
| `resultados_opencv/resultados_opencv/` | Ocho imágenes PNG generadas por el cuaderno de la Imagen 1. |
| `resultados_opencv (1)/resultados_opencv/` | Siete imágenes PNG generadas por el cuaderno de la Imagen 2. |
| `Informe/` | Informe final en Word (`.docx`) y en PDF. |

> **Nota sobre el tamaño.** El repositorio pesa cerca de 150 MB porque las evidencias se guardaron a resolución completa (algunos PNG superan los 20 MB). Para clonarlo más rápido se puede usar `git clone --depth 1`.

## Imágenes de prueba

| | Imagen 1 | Imagen 2 |
|---|---|---|
| **Contenido** | Cinco figuras pequeñas de colores sobre un parlante negro, frente a una cortina clara | Escritorio oscuro con monitor, teclado rojo y tapete, frente a una pared blanca con relieve |
| **Orientación** | Vertical | Horizontal |
| **Forma** `(alto, ancho, canales)` | `(4000, 3000, 3)` | `(6000, 8000, 3)` |
| **Total de píxeles** | 12 000 000 | 48 000 000 |
| **Tipo de dato** | `uint8` | `uint8` |
| **Valor mínimo / máximo** | 0 / 255 | 0 / 255 |
| **Píxel central (B, G, R)** | `[39, 16, 24]` | `[33, 28, 30]` |
| **Notebook** | `Copia_de_Semana_7_…ipynb` | `Semana_7_…_1.ipynb` |
| **Carpeta de resultados** | `resultados_opencv/` | `resultados_opencv (1)/` |

## Flujo de procesamiento

Cada cuaderno sigue las mismas etapas, en este orden:

| # | Etapa | Funciones principales | Qué permite observar |
|---|---|---|---|
| 1 | Carga e inspección | `cv2.imread`, `img.shape`, `img.dtype` | La imagen como matriz de enteros de 8 bits por canal. |
| 2 | Conversión de color | `cv2.cvtColor` (`BGR2RGB`, `BGR2GRAY`) | OpenCV usa orden **BGR**; en gris se conserva el brillo y se pierde el color. |
| 3 | Redimensionamiento y recorte | `cv2.resize`, *slicing* de NumPy | Menos datos y pérdida de detalle al reducir; el recorte aísla una región de interés. |
| 4 | Filtrado | `cv2.blur`, `cv2.GaussianBlur`, `cv2.medianBlur` | Suavizado del vecindario (promedio, gaussiano y mediana) para reducir ruido. |
| 5 | Umbralización | `cv2.threshold` (umbral 127) | Separación binaria por intensidad; depende de la iluminación. |
| 6 | Detección de bordes | `cv2.Canny` (80 y 160) | Cambios fuertes de intensidad: la estructura de la escena. |
| 7 | Contornos | `cv2.findContours`, `cv2.boundingRect` | Regiones candidatas encerradas en cajas delimitadoras (área > 100 px²). |
| 8 | Guardado | `cv2.imwrite` | Evidencias en PNG para el informe. |

Fragmento representativo del cuaderno:

```python
import cv2

img  = cv2.imread(ruta_imagen)                         # carga (BGR)
gris = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)           # escala de grises
suave = cv2.GaussianBlur(gris, (5, 5), 0)              # reduce ruido
_, umbral = cv2.threshold(suave, 127, 255, cv2.THRESH_BINARY)
bordes = cv2.Canny(suave, 80, 160)                     # bordes de Canny

contornos, _ = cv2.findContours(bordes, cv2.RETR_EXTERNAL, cv2.CHAIN_APPROX_SIMPLE)
for c in contornos:
    if cv2.contourArea(c) > 100:                       # descarta contornos pequeños
        x, y, w, h = cv2.boundingRect(c)
        cv2.rectangle(img, (x, y), (x + w, y + h), (0, 255, 0), 2)
```

## Resultados

### Resumen numérico

| Métrica | Imagen 1 | Imagen 2 |
|---|---|---|
| Tamaño tras redimensionar | `(210, 320, 3)` | `(210, 320, 3)` |
| Tamaño del recorte central (50 % × 50 %) | `(2000, 1500, 3)` | `(3000, 4000, 3)` |
| Contornos detectados | 542 | 1704 |
| Contornos con área > 100 px² | 20 | 210 |
| Proporción que supera el filtro | 3,7 % | 12,3 % |

### Galería

Se muestran las evidencias ligeras del repositorio. Las versiones a resolución completa (gris, recorte, desenfoque) están en las carpetas de resultados.

**Redimensionada (320 × 210 px)**

<table>
  <tr>
    <td align="center"><img src="R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/resultados_opencv/resultados_opencv/03_redimensionada.png" width="320" alt="Imagen 1 redimensionada"><br><sub>Imagen 1</sub></td>
    <td align="center"><img src="R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/resultados_opencv%20%281%29/resultados_opencv/003_redimensionada.png" width="320" alt="Imagen 2 redimensionada"><br><sub>Imagen 2</sub></td>
  </tr>
</table>

**Umbralización binaria (umbral 127)**

<table>
  <tr>
    <td align="center"><img src="R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/resultados_opencv/resultados_opencv/06_umbral.png" height="300" alt="Imagen 1 umbral"><br><sub>Imagen 1</sub></td>
    <td align="center"><img src="R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/resultados_opencv%20%281%29/resultados_opencv/006_umbral.png" height="300" alt="Imagen 2 umbral"><br><sub>Imagen 2</sub></td>
  </tr>
</table>

**Bordes de Canny**

<table>
  <tr>
    <td align="center"><img src="R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/resultados_opencv/resultados_opencv/07_bordes.png" height="300" alt="Imagen 1 bordes"><br><sub>Imagen 1</sub></td>
    <td align="center"><img src="R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/resultados_opencv%20%281%29/resultados_opencv/007_bordes.png" height="300" alt="Imagen 2 bordes"><br><sub>Imagen 2</sub></td>
  </tr>
</table>

**Contornos con cajas delimitadoras**

<table>
  <tr>
    <td align="center"><img src="R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/resultados_opencv/resultados_opencv/08_contornos.png" height="320" alt="Imagen 1 contornos"><br><sub>Imagen 1</sub></td>
    <td align="center"><img src="R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/resultados_opencv%20%281%29/resultados_opencv/008_contornos.png" height="320" alt="Imagen 2 contornos"><br><sub>Imagen 2</sub></td>
  </tr>
</table>

## Cómo reproducir la práctica

### Opción A · Google Colab (recomendada)

1. Abre el cuaderno que quieras ejecutar:

   [![Abrir Imagen 1 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Truder3105/R2-A1-S7-Tarea-Resolucion-de-ejercicios-practicos-con-OpenCV/blob/main/R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Copia_de_Semana_7_OpenCV_Practica_Guiada.ipynb) 
   [![Abrir Imagen 2 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Truder3105/R2-A1-S7-Tarea-Resolucion-de-ejercicios-practicos-con-OpenCV/blob/main/R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Semana_7_OpenCV_Practica_Guiada_1.ipynb)

2. Ejecuta la primera celda, que instala `opencv-python-headless` (no necesita interfaz gráfica de escritorio).
3. Cuando la celda de carga solicite un archivo, sube tu fotografía. **Debe llamarse exactamente igual que la ruta que usa el cuaderno** (ver tabla), porque el código lee esa ruta fija con `cv2.imread`:

   | Cuaderno | Nombre de archivo esperado |
   |---|---|
   | Imagen 1 | `/content/Imagen.jpeg` |
   | Imagen 2 | `/content/20260411_131147.jpg.jpeg` |

4. Ejecuta el resto de celdas en orden. Al final se crea la carpeta `resultados_opencv` y un `.zip` descargable con las evidencias.

### Opción B · Entorno local

```bash
git clone --depth 1 https://github.com/Truder3105/R2-A1-S7-Tarea-Resolucion-de-ejercicios-practicos-con-OpenCV.git
cd R2-A1-S7-Tarea-Resolucion-de-ejercicios-practicos-con-OpenCV

python -m venv .venv
source .venv/bin/activate            # Windows: .venv\Scripts\activate
pip install opencv-python-headless numpy matplotlib jupyter
jupyter notebook
```

Los cuadernos usan `google.colab.files` y rutas `/content/…`. Para ejecutarlos fuera de Colab, cambia `ruta_imagen` por la ruta local de tu imagen y omite las celdas de `files.upload()` y `files.download()`.

> **Versiones usadas en la práctica:** OpenCV 4.14.0 · NumPy 2.1.3 · Matplotlib · entorno Google Colab.

## Informe

El informe final sigue la plantilla **APA 7** y cubre la estructura pedida en la práctica:

| Sección | Contenido |
|---|---|
| Portada | Título, autores, institución, CADI, docente y fecha. |
| Resumen | Síntesis del trabajo con palabras clave. |
| Objetivo | Qué se buscó hacer con OpenCV. |
| Desarrollo | Código breve, figuras y resultados por ejercicio (7 figuras y 3 tablas). |
| Análisis | Explicación de lo observado en cada transformación. |
| Conclusiones | Aprendizajes, dificultades y recomendaciones. |
| Referencias | Bradski (2000), Canny (1986) y Suzuki y Abe (1985). |

**Descargas:** [PDF](R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Informe/R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV_final.pdf) · [Word](R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV/Informe/R2-A1-S7%20Tarea%20%E2%80%93%20Resoluci%C3%B3n%20de%20ejercicios%20pr%C3%A1cticos%20con%20OpenCV_final.docx)

## Hallazgos y recomendaciones

**Lo que mostró la práctica**

- Una imagen es un arreglo `uint8` de `(alto, ancho, 3)`; la Imagen 2 contiene cuatro veces más datos que la Imagen 1.
- Visualizar una imagen BGR sin convertir intercambia rojo y azul sin generar ningún error.
- Redimensionar a un tamaño fijo (320 × 210) **deforma** las imágenes cuando no se conserva la proporción.
- Un umbral global fijo depende de la iluminación y pierde el detalle de las zonas oscuras.
- Canny resalta la estructura, pero los bordes rara vez forman curvas cerradas: detectar bordes **no equivale a detectar objetos**.
- Con 12 y 48 millones de píxeles, filtros de 7 × 7 y un área mínima de 100 px² resultan casi imperceptibles.

**Recomendaciones**

- Reducir la imagen **conservando su proporción** antes de filtrar o detectar bordes.
- Elegir el tamaño del filtro según la resolución de la imagen.
- Probar umbralización adaptativa o el método de Otsu en lugar de un valor fijo.
- Cerrar los huecos de los bordes con operaciones morfológicas antes de buscar contornos.
- Definir el área mínima del contorno como fracción del tamaño de la imagen.

## Tecnologías

| Herramienta | Uso |
|---|---|
| [Python](https://www.python.org/) | Lenguaje de la práctica. |
| [OpenCV](https://opencv.org/) | Procesamiento de imágenes y visión por computador. |
| [NumPy](https://numpy.org/) | Manejo de las imágenes como arreglos. |
| [Matplotlib](https://matplotlib.org/) | Visualización de resultados. |
| [Google Colab](https://colab.research.google.com/) | Entorno de ejecución de los cuadernos. |

## Autores y contexto académico

| | |
|---|---|
| **Autores** | Julian Esteban Ballesteros Ortiz · Juan Diego Walteros Cortes |
| **Programa** | Especialización en Inteligencia Artificial |
| **Institución** | Universidad de Cundinamarca |
| **CADI** | Percepción Computacional · CAD2202023102 |
| **Docente** | Mónica María Fonseca Vigoya |
| **Actividad** | R2-A1-S7 · Semana 7 · Resolución de ejercicios prácticos con OpenCV |
| **Fecha** | Octubre de 2026 |

Trabajo de carácter académico.

## Referencias

- Bradski, G. (2000). The OpenCV library. *Dr. Dobb's Journal of Software Tools*, *25*(11), 120–125.
- Canny, J. (1986). A computational approach to edge detection. *IEEE Transactions on Pattern Analysis and Machine Intelligence*, *PAMI-8*(6), 679–698. https://doi.org/10.1109/TPAMI.1986.4767851
- Suzuki, S., & Abe, K. (1985). Topological structural analysis of digitized binary images by border following. *Computer Vision, Graphics, and Image Processing*, *30*(1), 32–46. https://doi.org/10.1016/0734-189X(85)90016-7
