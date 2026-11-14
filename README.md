# Clasificación de tumores cerebrales en MRI

Proyecto de deep learning con Keras y TensorFlow para clasificar resonancias magnéticas del cerebro en cuatro clases: glioma, meningioma, tumor pituitario o sin tumor.

Es un proyecto académico, no una herramienta de diagnóstico.

## Dataset

Brain Tumor Classification (MRI) de Kaggle: https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri

Tiene 2,870 imágenes de entrenamiento y 394 de prueba. El notebook lo descarga automáticamente, por eso no está en el repositorio. Antes de entrenar quité 83 imágenes que estaban repetidas entre entrenamiento y prueba.

## Modelos

1. CNN base, sin regularización.
2. CNN con data augmentation, BatchNormalization, Dropout y L2.
3. La misma CNN con learning rate y dropout ajustados.
4. EfficientNetB0 con transfer learning.

## Resultados

| Modelo | Validación | Prueba |
|---|---|---|
| CNN base | 0.89 | 0.69 |
| CNN regularizada | 0.33 | 0.32 |
| CNN + hiperparámetros | 0.78 | 0.51 |
| EfficientNetB0 | 0.78 | 0.65 |

El mejor resultado fue el de la CNN base, aunque sobreajusta. EfficientNetB0 fue el modelo más estable y el que mejor generaliza. El análisis completo está en el notebook.

## Autor

Ana Paula Moreno Frías
