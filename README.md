
# Predicción de Ventas con AutoGluon - Proyecto de Machine Learning

## Resumen del Proyecto

Este proyecto implementa un sistema automatizado de predicción de ventas por producto utilizando **AutoGluon TimeSeries** para febrero 2020. El sistema realiza entrenamiento iterativo con optimización automática de hiperparámetros y submissions automáticas a Kaggle.

### Funcionalidades Principales:

- **Predicción de Series Temporales**: Utiliza múltiples modelos (DeepAR, TemporalFusionTransformer, PatchTST) para predecir ventas en toneladas
- **Entrenamiento Iterativo**: Sistema automatizado que ajusta hiperparámetros basándose en el rendimiento en Kaggle
- **Optimización Inteligente**: Detecta estancamiento y aplica cambios drásticos en la configuración de modelos
- **Validación Automática**: Integración con Kaggle para evaluación continua del rendimiento
- **Gestión de Memoria**: Optimización de tipos de datos (float64 → float32) para reducir uso de RAM

### Datos de Entrada:
- `sell-in.txt`: Datos históricos de ventas
- `tb_productos.txt`: Información de productos
- `productos_pred.txt`: Lista de productos a predecir

### Modelos Utilizados:
- **DeepAR**: Red neuronal recurrente para series temporales
- **TemporalFusionTransformer**: Transformer especializado en predicción temporal
- **PatchTST**: Modelo basado en patches para series temporales

### Flujo de Trabajo:
1. Carga y preprocesamiento de datos históricos (hasta dic 2019)
2. Entrenamiento iterativo con diferentes configuraciones de hiperparámetros
3. Predicción para febrero 2020
4. Submission automática a Kaggle
5. Evaluación y ajuste de hiperparámetros basado en resultados
6. Repetición del ciclo hasta convergencia

El sistema está diseñado para ejecutarse de forma autónoma y requiere altos recursos computacionales (RAM y CPU) debido a la complejidad de los modelos de deep learning utilizados.
