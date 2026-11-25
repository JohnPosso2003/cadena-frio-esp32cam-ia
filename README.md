# cadena-frio-esp32cam-ia

# Clasificación de apertura de caja con ESP32-CAM

Proyecto de clasificación de imágenes para identificar si una caja de cadena de frío está abierta o cerrada, utilizando una ESP32-CAM y un modelo de inteligencia artificial desarrollado en Edge Impulse.

## 1. Objetivo

Desarrollar un modelo de clasificación de imágenes capaz de reconocer el estado de apertura de una caja de cadena de frío, utilizando técnicas de aprendizaje automático y procesamiento de imágenes.

## 2. Herramientas utilizadas

| Herramienta | Función |
|---|---|
| ESP32-CAM | Captura de imágenes |
| Edge Impulse | Entrenamiento y evaluación del modelo |
| Arduino IDE | Programación de la ESP32-CAM |
| GitHub | Almacenamiento y documentación |

## 3. Clases del modelo

El modelo está diseñado para identificar dos estados:

| Clase | Descripción |
|---|---|
| `caja_cerrada` | La caja tiene la tapa cerrada |
| `caja_abierta` | La caja tiene la tapa abierta |

## 4. Metodología

1. **Adquisición de imágenes:** capturar mínimo 50 fotografías por clase utilizando la ESP32-CAM.
2. **Preparación del dataset:** organizar las imágenes por clase y dividirlas en 80 % entrenamiento y 20 % prueba, estratificando por etiqueta.
3. **Configuración del modelo:** utilizar imágenes de 96 × 96 píxeles y Transfer Learning con una versión ligera de MobileNetV2.
4. **Entrenamiento:** entrenar el modelo en Edge Impulse.
5. **Evaluación:** analizar la precisión y la matriz de confusión.
6. **Exportación:** generar la librería Arduino para la ESP32-CAM.

## 5. Estructura del repositorio

```text
cadena-frio-esp32cam-ia/
│
├── dataset/
│   ├── caja_cerrada/
│   └── caja_abierta/
│
├── firmware/
├── model/
├── resultados/
└── README.md
```

## 6. Resultados

Los resultados del entrenamiento y la evaluación del modelo se incorporarán en esta sección una vez finalizadas las pruebas con imágenes reales de la ESP32-CAM.

Se documentarán los siguientes resultados:

| Indicador | Resultado |
|---|---|
| Precisión del modelo | Pendiente de evaluación |
| Matriz de confusión | Pendiente de evaluación |
| Pruebas de clasificación | Pendiente de evaluación |
| Librería Arduino | Pendiente de exportación |

Las evidencias obtenidas se almacenarán en la carpeta `resultados/` y el modelo exportado en `model/`.

## 7. Integración futura

El modelo permitirá identificar el estado de apertura de la caja. Posteriormente, sus predicciones podrán integrarse mediante MQTT con el sistema de monitoreo de cadena de frío.
