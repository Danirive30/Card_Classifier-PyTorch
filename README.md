# Clasificación de Imágenes de Cartas de Juego con PyTorch

Este proyecto consiste en la construcción de un modelo de clasificación de imágenes utilizando PyTorch. El objetivo principal es clasificar imágenes de cartas de juego en 53 categorías diferentes. A través de este desarrollo, se aplican conceptos fundamentales de aprendizaje profundo, procesamiento de imágenes y entrenamiento de modelos.

## Tabla de Contenidos
- [Requisitos](#requisitos)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Implementación](#implementación)
  - [Conjuntos de Datos y Transformaciones](#conjuntos-de-datos-y-transformaciones)
  - [Modelo](#modelo)
  - [Entrenamiento](#entrenamiento)
- [Resultados](#resultados)
- [Conclusiones](#conclusiones)
- [Cómo Ejecutar el Proyecto](#cómo-ejecutar-el-proyecto)
- [Créditos](#créditos)

## Requisitos
Para ejecutar este proyecto, asegúrate de tener instalados los siguientes paquetes:
- Python 3.10 o superior
- PyTorch 2.0.0 o superior
- Torchvision 0.15.1 o superior
- Timm
- Pandas 2.0.3
- NumPy 1.23.5
- Matplotlib

También necesitarás un conjunto de datos de imágenes de cartas de juego organizado en carpetas por categoría.

## Estructura del Proyecto
1. **Conjuntos de datos:** 
   - Carpeta de entrenamiento: `train/`
   - Carpeta de validación: `valid/`
   - Carpeta de prueba: `test/`
2. **Modelo:** Una red neuronal basada en EfficientNet-B0 con una capa de clasificación personalizada.
3. **Entrenamiento:** Un bucle de entrenamiento que utiliza el optimizador Adam y una función de pérdida de entropía cruzada.

## Implementación

### Conjuntos de Datos y Transformaciones
Se utiliza la clase `PlayingCardDataset` para cargar las imágenes desde el disco, aplicando transformaciones como redimensionar las imágenes a 128x128 píxeles y convertirlas a tensores.

### Modelo
El modelo se construye a partir de la arquitectura EfficientNet-B0, importada desde el paquete `timm`. La última capa se modifica para clasificar 53 categorías de cartas.

### Entrenamiento
El proceso de entrenamiento incluye:
1. División de los datos en entrenamiento, validación y prueba.
2. Entrenamiento del modelo durante 5 épocas utilizando el optimizador Adam.
3. Registro de la pérdida durante el entrenamiento y la validación.

## Resultados
Los resultados del entrenamiento muestran una disminución constante en la pérdida tanto para el conjunto de entrenamiento como para el de validación, indicando que el modelo está aprendiendo de los datos.

## Conclusiones
Este proyecto demuestra cómo construir un modelo de clasificación de imágenes utilizando PyTorch. A través del uso de una arquitectura preentrenada como EfficientNet-B0, logramos simplificar el proceso y mejorar el desempeño en comparación con modelos construidos desde cero.

## Cómo Ejecutar el Proyecto
1. Clona este repositorio en tu máquina local.
2. Instala las dependencias listadas en la sección de requisitos.
3. Organiza las carpetas de datos en las rutas especificadas (`train/`, `valid/`, `test/`).
4. Ejecuta el código en un entorno compatible como Jupyter Notebook o directamente en un archivo Python.

--

Proyecto desarrollado basado en el aprendizaje y experimentación con PyTorch.

--

# Card_Classifier-PyTorch
