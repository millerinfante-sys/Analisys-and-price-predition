Proyecto: EnergyPriceAnalyzer
1. ¿Qué es?
Este proyecto implementa una clase en Python llamada EnergyPriceAnalyzer que:
- Descarga datos históricos de precios de energía en Colombia (XM) y de mercados internacionales (ejemplo: Europa).
- Genera gráficos de series temporales y comparativos.
- Entrena un modelo predictivo de precios basado en Random Forest Regressor.
- Produce métricas de error (MAE, RMSE) y visualizaciones de predicciones.
2. ¿Por qué?
El análisis de precios de energía es fundamental para:
- Comprender la dinámica del mercado eléctrico.
- Evaluar la volatilidad y patrones de precios.
- Desarrollar modelos predictivos que apoyen la toma de decisiones en planeación energética y gestión de riesgos.
3. ¿Cómo funciona?
El flujo principal está encapsulado en el método run_analysis(), que ejecuta:
- Carga de datos (Colombia e internacionales).
- Generación de gráficos (series temporales, comparativos, heatmaps).
- Entrenamiento de un modelo predictivo con validación y métricas.


Instalación y Dependencias
Requisitos previos
- Python 3.9+
- pip (gestor de paquetes de Python)
Instalación de dependencias
Ejecuta en la terminal:
pip install requests pandas matplotlib seaborn scikit-learn numpy



Ejecución
- Clona o descarga este repositorio.
- Guarda el archivo del código como energy_price_analyzer.py.
- En la terminal, ejecuta:
python energy_price_analyzer.py


Resultado esperado
- Descarga de datos (o generación de datos sintéticos si falla la API).
- Creación de gráficos:
- time_series.png
- comparative_analysis.png
- predictions.png
- Impresión en consola de métricas del modelo (MAE y RMSE).

Ejemplo de uso en código
from energy_price_analyzer import EnergyPriceAnalyzer

# Crear instancia
analyzer = EnergyPriceAnalyzer()

# Ejecutar análisis completo
analyzer.run_analysis()

# También puedes usar métodos individuales:
analyzer.fetch_colombia_data()
analyzer.generate_time_series_plots()
model, features = analyzer.train_prediction_model()



Documentación Inline
El código ya incluye docstrings en cada método, por ejemplo:
def fetch_colombia_data(self):
    """Extrae datos históricos de precios de XM Colombia"""


Esto permite entender rápidamente la función de cada método.

Changelog
v1.0.0 (2025-11-03)
- Implementación inicial de la clase EnergyPriceAnalyzer.
- Métodos para carga de datos (Colombia e internacionales).
- Generación de gráficos de series temporales y comparativos.
- Entrenamiento de modelo predictivo con Random Forest.
- Exportación de gráficos en formato PNG.

Evidencia de Quick-Start
- En una máquina limpia con Python 3.9+ y las dependencias instaladas, el script se ejecuta correctamente.
- Si las APIs no responden, se generan datos sintéticos para garantizar que los gráficos y el modelo funcionen.
- La API/documentación coincide con el comportamiento real: los métodos hacen exactamente lo que describen sus docstrings.
