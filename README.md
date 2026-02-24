# 🚘 Detección de Matrículas Amarillas con OpenCV y K-Means

Proyecto de **Computer Vision** enfocado en la detección automática de **matrículas amarillas** mediante el uso de **OpenCV (cv2)** y técnicas de **clustering con K-Means** para segmentación por color.

---

## 🧠 Descripción del Proyecto

El objetivo del proyecto es desarrollar un sistema capaz de:

- Detectar matrículas amarillas en imágenes de vehículos.
- Aplicar técnicas de clustering (K-Means) para aislar el amarillo dominante.
- Segmentar regiones candidatas mediante análisis de color.
- Filtrar y localizar posibles regiones de interés (ROI).
- Visualizar los resultados con bounding boxes.

El enfoque principal se basa en aprovechar la **distinción cromática** del amarillo para separar la matrícula del fondo del vehículo.

---

## 🎯 Objetivo Técnico

Identificar automáticamente zonas de color amarillo predominante en una imagen utilizando:

- Procesamiento de imágenes con **OpenCV**
- Reducción de dimensionalidad de colores
- Clusterización con **K-Means (OpenCV)**
- Uso de templeates y comparativas

---

## 🧰 Tecnologías Utilizadas

- Python 3.10+
- OpenCV (`cv2`)
- NumPy
- Matplotlib (visualización)

---

## 📁 Estructura del Proyecto

    deteccion-matriculas/
    ├── Fotos/
    │   └── imagenes.png              → Imágenes de prueba
    │
    ├── enunciado_computer_vision.ipynb
    ├── char_i.png                → Imágenes Extraidas de las matrículas          
    └── README.md

## 🧪 Lógica del K-Means

- Se reestructura la imagen a matriz de píxeles (N x 3).
- Se define un número de clusters (por ejemplo, k=3 o k=5).
- Se ajusta el modelo KMeans.
- Se identifican los centroides.
- Se selecciona el cluster cuyo centroide tenga mayor componente amarilla.
- Se reconstruye la máscara binaria.

---

## 📊 Criterios de Detección

Una región es considerada matrícula válida si:

- Su área supera un umbral mínimo.
- La proporción ancho/alto coincide con dimensiones típicas.
- Predomina el color amarillo.

---

## ⚠️ Limitaciones

- Funciona únicamente para matrículas de color amarillo.
- Sensible a iluminación extrema.
- Puede detectar objetos amarillos que no sean matrículas.
- No incluye OCR para lectura del número.

---

## 🚀 Mejoras Futuras

- Integración con Tesseract OCR para lectura del número.
- Detección basada en redes neuronales (YOLO, Faster R-CNN).
- Normalización avanzada de iluminación.
- Procesamiento en tiempo real con cámara.

---

## 📌 Conclusión

El proyecto demuestra cómo combinar técnicas clásicas de visión artificial y aprendizaje no supervisado para resolver un problema práctico de detección basada en color.  
Es una solución ligera, comprensible y fácilmente extensible hacia enfoques más avanzados basados en Deep Learning.
