# Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate

### Introduccion
El modelo de predicción propuesto es una simplificación del modelo de Heuvelink (2005) para la producción de tomate en invernadero, solo que nuestro modelo no contempla la producción de fruto ni las variables de estado, parámetros y tasas de cambio relacionadas, ya que la producción de plántulas en invernadero se extiende solo hasta la aparición de las primeras hojas extendidas. Los valores para los parámetros requeridos por el modelo fueron obtenidos a partir de la literatura y experimentalmente.

El modelo se construyó con base en las investigaciones de Goudriaan y Van Laar (2012) y Heuvelink (2005). Se usó la denominación de variables original descritas por Goudriaan y Van Laar (2012). El cálculo de grados día desarrollo (𝐺𝐷𝐷) se hizo a partir del método sugerido por Manrique y Hodges (1989). Por otro lado, la eficiencia en el uso de la radiación (𝐸𝑈𝑅) y la partición de fotoasimilados a los diferentes órganos de la plántula de tomate fueron obtenidos experimentalmente.

El modelo de predicción consta de 2 variables ambientales de entrada: la irradiancia solar (J m-2 s-1) y la temperatura del aire (𝑇𝑎, °C). Las variables de estado: biomasa total (𝐵𝑠𝑡𝑜𝑡, g m-2) tallo (𝐵𝑠𝑡, g m-2), hoja (𝐵𝑠ℎ, g m-2) y raíz (𝐵𝑠𝑟, g m-2).

![Diagrama de flujo](https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/Diagrama%20de%20flujo.png)


## Resultados destacados del análisis del resumen

1. **Grados días de desarrollo (GDD):**
   - Primera hoja: 114 GDD.
   - Segunda hoja: 184 GDD.

2. **Temperaturas probadas:**
   - Rango de tratamientos: `T1: 12-29 °C` a `T6: 13-40 °C`.

3. **Efecto de la temperatura en la biomasa:**
   - Temperaturas máximas promedio (`Tmáx`) entre 29 y 40 °C influyeron significativamente (`P ≤ 0.05`) en:
     - Fracciones de biomasa asignadas a tallo y hoja.
     - Acumulación de biomasa en tallo.
   - `T6` y `T1` presentaron los mayores valores promedio en biomasa asignada.

4. **Correlación de la longitud de tallo con temperatura:**
   - `Tmd` (`R² = 0.75`), `Tm24h` (`R² = 0.79`) y `Tmn` (`R² = 0.71`).
   - `T4` presentó la mayor longitud de tallo, `T1` la menor.

5. **Área foliar específica:**
   - Correlación con `Tmn` (`R² = 0.83`).
   - Mayor valor en `T4`, menor en `T1`.

6. **Eficiencia en el uso de la radiación (EUR):**
   - No fue significativa (`P > 0.05`), aunque tuvo `R² = 0.73` con `Tmáx`.

7. **Cinética de fotosíntesis:**
   - Punto de saturación: 1000 μmol fotones m⁻² s⁻¹ a 28, 31 y 40 °C.
   - Punto de compensación:
     - 120 μmol fotones m⁻² s⁻¹ (28 °C).
     - 6 μmol fotones m⁻² s⁻¹ (31 °C).
     - 89 μmol fotones m⁻² s⁻¹ (40 °C).
   - Rendimiento cuántico:
     - Similar para 28 y 31 °C (0.06 mol CO₂ mol⁻¹ fotones).
     - Inferior a 40 °C (0.04 mol CO₂ mol⁻¹ fotones).

8. **Modelo de predicción de biomasa total acumulada:**
   - Coeficiente de correlación: 0.82.
   - Sobreestima con error medio porcentual: 46.7 %.
   - Biomasa por compartimiento:
     - **Tallo:** Subestimada (50.7 %).
     - **Hoja:** Sobreestimada (53.8 %).
     - **Raíz:** Mejor tendencia, pero error mayor (59.7 %).

9. **Efecto de `Tmáx`:**
   - Influyó en las relaciones fuente-demanda, causando diferencias en la longitud del tallo, una característica clave de la calidad de la plántula.

## II. OBJETIVOS

### 2.1. Objetivo general
Determinar el efecto de la temperatura máxima en el crecimiento y desarrollo de plántulas de tomate.

### 2.2. Objetivos específicos
- Determinar el efecto de la temperatura máxima en las variables y parámetros de crecimiento y desarrollo de plántulas de tomate.
- Adaptar un modelo mecanicista al crecimiento y desarrollo de la plántula de tomate bajo condiciones de microtúneles de plástico.


![Microtúneles](https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/Microtuneles.png)


