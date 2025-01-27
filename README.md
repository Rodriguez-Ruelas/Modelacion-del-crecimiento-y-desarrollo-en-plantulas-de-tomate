# MODELACION DEL CRECIMIENTO Y DESARROLLO EN PLANTULAS DE TOMATE

## INTRODUCCION
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



## Materiales y metodos

### Construcción de microtúneles

Para establecer el experimento se construyeron 3 estructuras protegidas con forma de microtúneles. A cada microtúnel se le adaptó un ventilador como extractor de aire, un calefactor, una estructura de madera para evitar que las charolas de poliestireno estuvieran en contacto con el suelo, malla para cubrir el suelo de color blanco (*ground cover*) y plástico lechoso de 50 % de transmisión de radiación solar, el cual fue designado para cubrir las estructuras de invernaderos.


![Microtúneles](https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/Microtuneles.png)
Fig. 

Los microtúneles se diseñaron y construyeron utilizando Arduino, en conjunto con el servicio de Ubidots, una plataforma de IoT (Internet of Things) para monitoreo y control de dispositivos. La capacidad de diseñar y construir nuestros propios instrumentos de experimentación es fundamental para explorar y someter a las plantas a los tratamientos correspondientes que se desean evaluar.


![Sistema de control](https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/Sistema%20de%20control.png)
Fig. 


### 5.4.2. Sistema de control
Para ajustar Ta a la curva de la función de Tac, se desarrolló un sistema de control (𝑆𝐶). El 𝑆𝐶 se diseñó a partir hardware y software “open source”. El hardware del 𝑆𝐶 consistió de cinco componentes:  
a) Dispositivo central de control (𝐷𝐶𝐶),  
b) Dispositivos de entrada (𝐷𝐸),  
c) Dispositivos de salida (𝐷𝑆),  
d) Dispositivo de comunicación (𝐷𝐶), y  
e) Sistema de monitoreo (𝑆𝑀).  
El software usado fue el compilador Arduino®.  

### 5.4.3. Construcción del dispositivo central de control
Para la construcción del 𝐷𝐶𝐶 se dispuso de la plataforma Arduino® como centro de procesamiento, control y comunicación. Como 𝐷𝐶𝐶, se usó una placa Arduino MEGA®, basada en el microcontrolador ATmega1280 de la compañía ATMEL CORPORATION®. Esta placa Arduino® provee un total de 54 pines digitales que son usados como entrada o salida, además, tiene la posibilidad de asignar 16 de estos 54 pines como entradas y salidas analógicas.  

### 5.4.4. Dispositivos de entrada
Se usó un sensor digital de humedad relativa (%) y temperatura del aire (°C) modelo DHT22 para monitorear el estado climatológico de cada microtunel. El sensor digital DHT22 opera bajo el rango de 0 a 100 % de humedad relativa (𝐻𝑅) y de 40 a 80 °C. La resolución para calcular la HR fue de 0.1 % y para la temperatura fue 0.1 °C, mientras que la exactitud fue de ± 2 % para 𝐻𝑅 y de menos de ± 0.5 °C para la temperatura del aire.  

Para registrar la fecha y hora de las lecturas en el microcontrolador, se usó un módulo 𝑅𝑇𝐶 basado en el chip DS3231 del fabricante DALLAS SEMICONDUCTOR®.  

### 5.4.5. Dispositivos de salida
Como dispositivo de salida se usó un módulo genérico de 8 canales para controlar relevadores de 5 V y 10 A. Dicho módulo se usó como interruptor para los extractores y calefactores de cada microtúnel.  

### 5.4.6. Dispositivo de comunicación
Como interfaz de comunicación, se usó una placa ethernet genérica basada en el chip W5100 fabricada por la compañía Wiznet®. Esta interfaz de comunicación soporta los protocolos de comunicación: protocolo de internet (internet protocol o 𝐼𝑃), protocolo de control de transmisión (Transmission Control Protocol o 𝑇𝐶𝑃) y el protocolo de datagramas de usuario (User Datagram Protocol o 𝑈𝐷𝑃).  

### 5.4.7. Sistema de monitoreo
Para construir el sistema de monitoreo (𝑆𝑀) en tiempo real del DCC, se usó el servidor “Internet of Things” (𝐼𝑂𝑇) que presta la compañía Ubidots®. Este servicio permite enlazar el 𝑆𝐶𝐶 con el servidor IOT para almacenar datos.

#### Cuadro 6. Definición de tratamientos por fecha de cultivo

| Fecha de cultivo | Temperatura del aire 𝑇𝑚í𝑛−𝑇𝑚á𝑥 (°C) | 𝑇1  | 𝑇2  | 𝑇3  |
|------------------|--------------------------------------|------|------|------|
| 𝐹1              | 6-27                                 | 6-35 | 6-40 |      |
| 𝐹2              | 6-27                                 | 6-35 | 6-40 |      |

Donde:  
𝑇1, 𝑇2 y 𝑇3 son los tratamientos, y 𝐹1 y 𝐹2 son las fechas de cultivo.

