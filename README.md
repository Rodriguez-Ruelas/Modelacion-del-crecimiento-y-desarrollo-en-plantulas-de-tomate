# 🌱📊 MODELACIÓN DEL CRECIMIENTO Y DESARROLLO EN PLÁNTULAS DE TOMATE 🍅

## I. INTRODUCCION

La producción de tomate en invernadero es una actividad económica muy importante en el mundo. Con el paso del tiempo y la gran cantidad de descubrimientos científicos en fisiología de plantas, se ha logrado entender cómo la fotosíntesis, respiración y otros procesos fisiológicos son fundamentales para entender el crecimiento y desarrollo de las plantas. Con la incorporación de otras ciencias como física, química, informática y la electrónica en la investigación y producción agrícola, se ha podido lograr la abstracción de algunas partes que componen un sistema agrícola.

A partir de trabajos realizados en la Universidad de Wageningen y otras instituciones dedicadas a la investigación agrícola, se han podido establecer modelos de predicción. Los modelos de predicción nos permiten desglosar un sistema en algunas de sus partes para lograr un mejor entendimiento de estos, nos ayuda a tomar mejores decisiones en cuanto al manejo del cultivo y puede llegar a generar nueva información acerca del sistema. En este sentido, un modelo de predicción agrícola es una herramienta en constante evolución, capaz de ser ajustada y adaptada en función del conocimiento que se tenga de dicho sistema.

En cuanto a la producción de tomate en invernadero, existen modelos como el **TOMGRO**, **TOMSIM** y **TOMPOSSE**; los cuales presentan diferentes formas de evaluar y predecir el crecimiento y desarrollo en tomate. Cada modelo está basado en trabajos de investigación tanto en campo como en ambientes controlados y estos pretenden brindar una visión específica del sistema que representan.

Los modelos de predicción en el campo de la agricultura son de gran importancia para mejorar la producción bajo invernadero y la aportación de nuevo conocimiento científico. Su precisión ha ido de la mano con la evolución e incorporación de otras disciplinas y, sin duda, es un campo integrador del conocimiento de un sistema.


El modelo de predicción propuesto es una simplificación del modelo de Heuvelink (2005) para la producción de tomate en invernadero, solo que nuestro modelo no contempla la producción de fruto ni las variables de estado, parámetros y tasas de cambio relacionadas, ya que la producción de plántulas en invernadero se extiende solo hasta la aparición de las primeras hojas extendidas. Los valores para los parámetros requeridos por el modelo fueron obtenidos a partir de la literatura y experimentalmente.

El modelo se construyó con base en las investigaciones de Goudriaan y Van Laar (2012) y Heuvelink (2005). Se usó la denominación de variables original descritas por Goudriaan y Van Laar (2012). El cálculo de grados día desarrollo (𝐺𝐷𝐷) se hizo a partir del método sugerido por Manrique y Hodges (1989). Por otro lado, la eficiencia en el uso de la radiación (𝐸𝑈𝑅) y la partición de fotoasimilados a los diferentes órganos de la plántula de tomate fueron obtenidos experimentalmente.

El modelo de predicción consta de 2 variables ambientales de entrada: la irradiancia solar (J m-2 s-1) y la temperatura del aire (𝑇𝑎, °C). Las variables de estado: biomasa total (𝐵𝑠𝑡𝑜𝑡, g m-2) tallo (𝐵𝑠𝑡, g m-2), hoja (𝐵𝑠ℎ, g m-2) y raíz (𝐵𝑠𝑟, g m-2).

![Diagrama de flujo](https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/Diagrama%20de%20flujo.png)
<p align="center">
  <strong>Figura 1.</strong> Diagrama de flujo para el modelado del crecimiento y desarrollo de plántulas de tomate.
</p>

## II. RESULTADOS

2.1. **Grados días de desarrollo (GDD):**
   - Primera hoja: 114 GDD.
   - Segunda hoja: 184 GDD.

2.2. **Temperaturas probadas:**
   - Rango de tratamientos: `T1: 12-29 °C` a `T6: 13-40 °C`.

2.3. **Efecto de la temperatura en la biomasa:**
   - Temperaturas máximas promedio (`Tmáx`) entre 29 y 40 °C influyeron significativamente (`P ≤ 0.05`) en:
     - Fracciones de biomasa asignadas a tallo y hoja.
     - Acumulación de biomasa en tallo.
   - `T6` y `T1` presentaron los mayores valores promedio en biomasa asignada.

2.4. **Correlación de la longitud de tallo con temperatura:**
   - `Tmd` (`R² = 0.75`), `Tm24h` (`R² = 0.79`) y `Tmn` (`R² = 0.71`).
   - `T4` presentó la mayor longitud de tallo, `T1` la menor.

2.5. **Área foliar específica:**
   - Correlación con `Tmn` (`R² = 0.83`).
   - Mayor valor en `T4`, menor en `T1`.

2.6. **Eficiencia en el uso de la radiación (EUR):**
   - No fue significativa (`P > 0.05`), aunque tuvo `R² = 0.73` con `Tmáx`.

2.7. **Cinética de fotosíntesis:**
   - Punto de saturación: 1000 μmol fotones m⁻² s⁻¹ a 28, 31 y 40 °C.
   - Punto de compensación:
     - 120 μmol fotones m⁻² s⁻¹ (28 °C).
     - 6 μmol fotones m⁻² s⁻¹ (31 °C).
     - 89 μmol fotones m⁻² s⁻¹ (40 °C).
   - Rendimiento cuántico:
     - Similar para 28 y 31 °C (0.06 mol CO₂ mol⁻¹ fotones).
     - Inferior a 40 °C (0.04 mol CO₂ mol⁻¹ fotones).

2.8. **Modelo de predicción de biomasa total acumulada:**
   - Coeficiente de correlación: 0.82.
   - Sobreestima con error medio porcentual: 46.7 %.
   - Biomasa por compartimiento:
     - **Tallo:** Subestimada (50.7 %).
     - **Hoja:** Sobreestimada (53.8 %).
     - **Raíz:** Mejor tendencia, pero error mayor (59.7 %).

2.9. **Efecto de `Tmáx`:**
   - Influyó en las relaciones fuente-demanda, causando diferencias en la longitud del tallo, una característica clave de la calidad de la plántula.

## III. OBJETIVOS

### 3.1. Objetivo general
Determinar el efecto de la temperatura máxima en el crecimiento y desarrollo de plántulas de tomate.

### 3.2. Objetivos específicos
- Determinar el efecto de la temperatura máxima en las variables y parámetros de crecimiento y desarrollo de plántulas de tomate.
- Adaptar un modelo mecanicista al crecimiento y desarrollo de la plántula de tomate bajo condiciones de microtúneles de plástico.

## IV. MATERIALES Y METODOS
### 4.1. Construcción de microtúneles

Para establecer el experimento se construyeron 3 estructuras protegidas con forma de microtúneles. A cada microtúnel se le adaptó un ventilador como extractor de aire, un calefactor, una estructura de madera para evitar que las charolas de poliestireno estuvieran en contacto con el suelo, malla para cubrir el suelo de color blanco (*ground cover*) y plástico lechoso de 50 % de transmisión de radiación solar, el cual fue designado para cubrir las estructuras de invernaderos.

![Microtúneles](https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/Microtuneles.png)
<p align="center">
  <strong>Figura 2.</strong> A) Disposición de los microtúneles en campo. B) Microtúneles abiertos con plántulas de tomate.
</p>


Los microtúneles se diseñaron y construyeron utilizando Arduino, en conjunto con el servicio de Ubidots, una plataforma de IoT (Internet of Things) para monitoreo y control de dispositivos. La capacidad de diseñar y construir nuestros propios instrumentos de experimentación es fundamental para explorar y someter a las plantas a los tratamientos correspondientes que se desean evaluar.

### 4.2. Sistema de control
Para ajustar Ta a la curva de la función de Tac, se desarrolló un sistema de control (𝑆𝐶). El 𝑆𝐶 se diseñó a partir hardware y software “open source”. El hardware del 𝑆𝐶 consistió de cinco componentes:  
  - a) Dispositivo central de control (𝐷𝐶𝐶),  
  - b) Dispositivos de entrada (𝐷𝐸),  
  - c) Dispositivos de salida (𝐷𝑆),  
  - d) Dispositivo de comunicación (𝐷𝐶), y  
  - e) Sistema de monitoreo (𝑆𝑀).  

El software usado fue el compilador Arduino®.  

![Sistema de control](https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/Sistema%20de%20control.png)
Fig. 

a) **Dispositivo central de control (𝐷𝐶𝐶)**  
Para la construcción del 𝐷𝐶𝐶 se dispuso de la plataforma Arduino® como centro de procesamiento, control y comunicación. Como 𝐷𝐶𝐶, se usó una placa Arduino MEGA®, basada en el microcontrolador ATmega1280 de la compañía ATMEL CORPORATION®. Esta placa Arduino® provee un total de 54 pines digitales que son usados como entrada o salida, además, tiene la posibilidad de asignar 16 de estos 54 pines como entradas y salidas analógicas.

b) **Dispositivos de entrada (𝐷𝐸)**  
Se usó un sensor digital de humedad relativa (%) y temperatura del aire (°C) modelo DHT22 para monitorear el estado climatológico de cada microtúnel. El sensor digital DHT22 opera bajo el rango de 0 a 100 % de humedad relativa (𝐻𝑅) y de 40 a 80 °C. La resolución para calcular la HR fue de 0.1 % y para la temperatura fue 0.1 °C, mientras que la exactitud fue de ± 2 % para 𝐻𝑅 y de menos de ± 0.5 °C para la temperatura del aire.

Para registrar la fecha y hora de las lecturas en el microcontrolador, se usó un módulo 𝑅𝑇𝐶 basado en el chip DS3231 del fabricante DALLAS SEMICONDUCTOR®.

c) **Dispositivos de salida (𝐷𝑆)**  
Como dispositivo de salida se usó un módulo genérico de 8 canales para controlar relevadores de 5 V y 10 A. Dicho módulo se usó como interruptor para los extractores y calefactores de cada microtúnel.

d) **Dispositivo de comunicación (𝐷𝐶)**  
Como interfaz de comunicación, se usó una placa ethernet genérica basada en el chip W5100 fabricada por la compañía Wiznet®. Esta interfaz de comunicación soporta los protocolos de comunicación: protocolo de internet (internet protocol o 𝐼𝑃), protocolo de control de transmisión (Transmission Control Protocol o 𝑇𝐶𝑃) y el protocolo de datagramas de usuario (User Datagram Protocol o 𝑈𝐷𝑃).

e) **Sistema de monitoreo (𝑆𝑀)**  
Para construir el sistema de monitoreo (𝑆𝑀) en tiempo real del DCC, se usó el servidor “Internet of Things” (𝐼𝑂𝑇) que presta la compañía Ubidots®. Este servicio permite enlazar el 𝑆𝐶𝐶 con el servidor IOT para almacenar datos.


### 4.3. Tratamientos
 
### Definición de tratamientos por fecha de cultivo 
| Fecha de cultivo | 𝑇1    | 𝑇2   | 𝑇3   |
|------------------|-------|-------|-------|
| **𝐹1**           | 6-27  | 6-35  | 6-40  |
| **𝐹2**           | 6-27  | 6-35  | 6-40  |


Donde:  
𝑇1, 𝑇2 y 𝑇3 son los tratamientos, y 𝐹1 y 𝐹2 son las fechas de cultivo.

### 4.4. Variables fisiológicas

#### 4.4.1. Biomasa seca total y por órgano vegetal
Se calcularon las variables de biomasa total (**B<sub>stot</sub>**, g m<sup>-2</sup>), tallo (**B<sub>st</sub>**, g m<sup>-2</sup>), hoja (**B<sub>sh</sub>**, g m<sup>-2</sup>) y raíz (**B<sub>sr</sub>**, g m<sup>-2</sup>).
Con los datos de biomasa seca acumulada total y en cada órgano, se calculó la fracción de fotoasimilados asignado a cada órgano vegetal; fracción de fotoasimilados asignados a hoja (**F<sub>h</sub>**, %), fracción de fotoasimilados asignados a tallo (**F<sub>t</sub>**, %) y fracción de fotoasimilados a raíz (**F<sub>r</sub>**, %).

#### 4.4.2. Longitud de tallo
La longitud del tallo (**L<sub>t</sub>**, cm) se midió después de la división de la plántula. Este inicio desde el primer nudo hasta la punta del tallo. Para esta medición se usó un flexómetro marca Truper®.

#### 4.4.3. Ancho de tallo
El ancho de tallo (**A<sub>t</sub>**, mm) se midió a la mitad del primer entrenudo de las plantas diseccionadas con un vernier digital de la marca Truper®.

#### 4.4.4. Área foliar
Para obtener el área foliar (**AF**, m<sup>2</sup> planta<sup>-1</sup>), las hojas por planta se escanearon en un multifuncional de la marca EPSON® serie 220 y las imágenes digitales se procesaron con el programa de uso libre (ImageJ, National Institutes of Health).

<p align="center">
  <img src="https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/ImegeJ.png" alt="ImageJ">
</p>
<p align="center"><strong>Figura 3. </strong>Software ImageJ utilizado para calcular el área foliar.</p>

#### 4.4.5. Índice de área foliar
El índice de área foliar (**IAF**, m<sup>2</sup> hoja m<sup>-2</sup> superficie) se calculó a partir del promedio de **AF** (m<sup>2</sup> planta<sup>-1</sup>) de cuatro plantas por tratamiento, el cual se multiplicó por la densidad de plantas por metro cuadrado (899.1).

### 4.5. Cálculo de parámetros de las plántulas de tomate
#### 4.5.1. Coeficiente de extinción
El coeficiente de extinción (**k**) se calculó a partir de mediciones de irradiancia fotosintética sobre (**I<sub>o</sub>**, μmol·m<sup>-2</sup>·s<sup>-1</sup>) y debajo (**IIAF**, μmol·m<sup>-2</sup>·s<sup>-1</sup>) del follaje del cultivo con un radiómetro lineal LI-1500 (LI-COR®, Inc.), y el **IAF** obtenido al momento de hacer la medición. La ecuación usada para calcular **k** fue:

$$
k = -\frac{\ln \left(\frac{IIAF}{I<sub>o</sub>}\right)}{IAF}
$$

donde:
- **IIAF** es la irradiancia medida bajo el dosel del cultivo;
- **I<sub>o</sub>** es la irradiancia medida sobre el dosel del cultivo;
- **IAF** es el índice de área foliar.

<p align="center">
  <img src="https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/CoeffExt.png" alt="CoeffExt">
</p>
<p align="center"><strong>Figura 4. </strong>Mediciones con el radiómetro lineal. A). Por encima del dosel y B). Por debajo del dosel.</p>


#### 4.5.2 Área foliar específica
El área foliar específica (**AFE**, m<sup>2</sup> g<sup>-1</sup>) se calculó a partir de la relación entre el **AF** (m<sup>2</sup>) y el peso del área foliar (**B<sub>sh</sub>**, g m<sup>-2</sup>) promedio de cuatro plantas por tratamiento.

#### 4.5.3 Eficiencia en el uso de la radiación solar
La eficiencia en el uso de la radiación solar (**EUR**, g MJ<sup>-1</sup>) se obtuvo del valor de la pendiente de la relación lineal entre la biomasa seca acumulada (g m<sup>-2</sup>) y la irradiancia solar acumulada transmitida por el plástico (MJ m<sup>-2</sup> d<sup>-1</sup>).

#### 4.5.4 Rendimiento cuántico, punto de saturación por luz, punto de compensación por luz, y tasa de asimilación neta.
Para calcular el rendimiento cuántico (**Φ**, μmol de CO<sub>2</sub> μmol<sup>-1</sup> de fotones), punto de saturación por luz (**Psl**, μmol de fotones m<sup>-2</sup> s<sup>-1</sup>), punto de compensación por luz (**Pcl**, μmol de fotones m<sup>2</sup> s<sup>-1</sup>), y la capacidad fotosintética neta (**Fg**, μmol CO<sub>2</sub> m<sup>2</sup> s<sup>-1</sup>); se realizaron cinéticas fotosintéticas para cada ambiente con un equipo portátil para medir fotosíntesis marca LICOR® (Licor, Inc.; Lincoln, NE, EE. UU.) y un aditamento especial (6400-02B LED Light source) que permite controlar la intensidad de luz bajo un programa ya establecido; además, es capaz de controlar el flujo y concentración de CO<sub>2</sub> gracias a un dosificador de gas (6400-01 CO<sub>2</sub> Mixer).
Se realizaron 3 cinéticas de crecimiento, una para cada tratamiento o ambiente (6-27, 6-35 y 6-40 °C) y con 3 repeticiones. Las cinéticas fotosintéticas se iniciaron alrededor de las 10:00 h y cada una de ellas se llevó a cabo en un día diferente (ambiente 6-27 °C el 20 de julio del 2017, 6-35 °C el 21 de julio del 2017 y el ambiente 6-40 °C el 19 de julio del 2017).
Para realizar las mediciones en cada ambiente, se modificó el sistema de control (**SC**) para que mantuviera constante la temperatura del microtúnel. Cada temperatura del aire programada para el microtúnel coincidía con la temperatura programada en la cámara del equipo portátil de fotosíntesis, de tal forma que la temperatura del aire sería similar a la temperatura de la hoja evaluada.

<p align="center">
  <img src="https://github.com/Rodriguez-Ruelas/Modelacion-del-crecimiento-y-desarrollo-en-plantulas-de-tomate/blob/main/Imagenes_README/licor.png" alt="licor">
</p>
<p align="center"><strong>Figura 5. </strong>Cinética de CO<sub>2</sub> usando el sistema de análisis infrarrojo de gases (IRGA, por sus siglas en inglés de "InfraRed Gas Analyzer").</p>


## 4.6 Componentes del modelo

### 4.6.1. Parámetros iniciales

Los parámetros iniciales que necesita el modelo propuesto son:
- Biomasa seca inicial total (B<sub>stot,i</sub>, g m<sup>-2</sup>)
- Biomasa seca inicial tallo (B<sub>st,i</sub>, g m<sup>-2</sup>)
- Biomasa seca inicial hoja (B<sub>sh,i</sub>, g m<sup>-2</sup>)
- Biomasa seca inicial raíz (B<sub>sr,i</sub>, g m<sup>-2</sup>)
- Índice de área foliar inicial (IAF<sub>i</sub>, m<sup>2</sup> m<sup>-2</sup>)
- Grados días desarrollo acumulados inicial (GDD<sub>i</sub>, adimensional)

Cada valor para las variables iniciales se obtuvieron a partir del primer muestreo de cada tratamiento para las dos fechas de cultivo.

### 4.6.2. Irradiancia fotosintética sobre el cultivo

La irradiancia fotosintética sobre el cultivo (I<sub>fs</sub>, MJ m<sup>-2</sup> d<sup>-1</sup>) se calculó con la siguiente ecuación:

$$ I_{fs} = I_i \cdot \left( \frac{T_{pr}}{100} \right) \cdot F_{PAR} $$

donde:
- 𝑇<sub>pr</sub> es la transmisión de la cubierta plástica de los microtúneles (%)
- 𝐼<sub>fs</sub> es la irradiancia fotosintética sobre el cultivo (MJ m<sup>2</sup> s<sup>-1</sup>)
- 𝐼<sub>i</sub> es la irradiancia solar al exterior del túnel (MJ m<sup>2</sup> s<sup>-1</sup>)
- 𝐹<sub>𝑃𝐴𝑅 es la fracción de irradiancia solar sobre la banda fotosintética (adimensional)

Se considera que 𝑇<sub>pr</sub> = 46 % y que 𝐹<sub>𝑃𝐴𝑅 = 0.50.

### 4.6.3. Temperatura media diaria

La temperatura media diaria (𝑇<sub>m24h</sub>, °C) diaria se obtuvo del promedio de la 𝑇<sub>a</sub> cada 15 min obtenida de los registradores electrónicos Hobo® en cada microtúnel.

### 4.6.4. Desarrollo fenológico

La acumulación de grados días desarrollo (GDD) en cada evento fenológico se obtuvo mediante el método de Manrique y Hodges (1989). La temperatura óptima de crecimiento (𝑇<sub>opt</sub>), temperatura mínima de crecimiento o temperatura base (𝑇<sub>b</sub>) y la temperatura máxima de crecimiento (𝑇<sub>mc</sub>), se obtuvieron con base en la metodología descrita en el apartado 5.7.2.

### 4.6.5. Fracción de radiación absorbida por el cultivo

La fracción de radiación absorbida (𝑓, adimensional) se calculó con base en una adaptación a la ley de Beer-Lambert:

$$ f = 1 - e^{-k \cdot IAF} $$

donde:
- 𝑓 es la fracción de radiación absorbida (adimensional)
- 𝑘 es el coeficiente de extinción (adimensional)
- 𝐼𝐴𝐹 es el índice de área foliar (m<sup>2</sup> m<sup>-2</sup>)
- 𝑒 es el número de Euler (adimensional)

### 4.6.6. Radiación absorbida por el follaje

La radiación absorbida por el follaje (𝐼, J m<sup>-2</sup> s<sup>-1</sup>) se calculó con la siguiente ecuación:

$$ I = I_{fs} \cdot f $$

donde:
- 𝐼 es la irradiancia absorbida por el follaje (J m<sup>-2</sup> s<sup>-1</sup>)
- 𝑓 es la fracción de radiación absorbida por el follaje
- 𝐼<sub>fs</sub> es la irradiancia incidente sobre el follaje (J m<sup>-2</sup> s<sup>-1</sup>)

### 4.6.7. Producción de asimilados

La producción de asimilados es una adaptación de la propuesta hecha por Goudriaan y Van Laar (2012) para el cálculo de fotosíntesis neta en función de la temperatura. Sin embargo, se incorporaron algunos cálculos y parámetros de la bibliografía existente.

### 4.6.8. Punto de compensación por CO2

El punto de compensación por CO2 (𝛤, μg CO<sub>2</sub> m<sup>-3</sup>) fue calculado a partir de la propuesta por Brooks y Farquhar (1985) para el cultivo de espinaca. La ecuación que se usó fue:

$$ \Gamma = 42.7 + 1.68 \cdot (T_a - 25) + 0.012 \cdot (T_a - 25)^2 $$

donde:
- 𝛤 es el punto de compensación de CO<sub>2</sub>
- 𝑇<sub>a</sub> es la temperatura del aire (°C)


### 4.6.9. Rendimiento cuántico

El rendimiento cuántico (𝜺, μg CO<sub>2</sub> J<sup>-1</sup>) se obtuvo mediante la corrección del rendimiento cuántico potencial con el punto de compensación de CO<sub>2</sub> de acuerdo con la ecuación propuesta por Goudriaan y Van Laar (2012):

$$ \epsilon = \epsilon_0 \cdot \frac{C_a - \Gamma}{(C_a + 2) \cdot \Gamma} $$

donde:
- 𝜀 es el rendimiento cuántico actual (μg CO<sub>2</sub> J<sup>-1</sup>)
- 𝜀<sub>0</sub> es el rendimiento cuántico potencial (μg CO<sub>2</sub> J<sup>-1</sup>)
- 𝐶<sub>a</sub> es la concentración de CO<sub>2</sub> ambiental (μg CO<sub>2</sub> m<sup>-3</sup>)
- 𝛤 es el punto de compensación de CO<sub>2</sub> (μg CO<sub>2</sub> m<sup>-3</sup>)

### 4.6.10 Conductancia del mesófilo

La conductancia del mesófilo (𝑔<sub>m</sub>, cm s<sup>-1</sup>) se calculó a partir de la interpolación de datos de una tabla que relaciona la temperatura ambiental (°C) con la conductancia estomática (cm s<sup>-1</sup>). Esta tabla (Cuadro 7) se obtuvo a partir de los datos propuestos por Bertin y Heuvelink (1993) para el modelo TOMSIM ver 1.0.

**Cuadro 7. Cálculo de la conductancia del mesófilo (𝑔<sub>m</sub>).**

| Temperatura del aire (°C) | Conductancia del mesófilo (cm s<sup>-1</sup>) |
|---------------------------|----------------------------------------------|
| 0                         | 0                                            |
| 15                        | 0.4                                          |
| 25                        | 0.4                                          |
| 40                        | 0                                            |


### 4.6.11. Resistencia del mesófilo al CO2

La resistencia del mesófilo (𝑟<sub>m</sub>, s<sup>-1</sup> m<sup>-1</sup>) se calcula a partir del inverso de la conductancia del mesófilo:

$$ r_m = \frac{1}{g_m} $$

donde:
- 𝑟<sub>m</sub> es la resistencia del mesófilo al CO<sub>2</sub> (s m<sup>-1</sup>)
- 𝑔<sub>m</sub> es la conductancia del mesófilo al CO<sub>2</sub> (m s<sup>-1</sup>)

### 4.6.12. Carboxilación limitada por fotosíntesis neta

Como la carboxilación limitada por fotosíntesis neta (𝐹<sub>𝑛𝑐</sub>, μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>) se calcula a partir de la concentración ambiental de CO<sub>2</sub>, se usa la ley de los gases para obtener esta variable en función de la temperatura:

$$ gas\_law = \frac{4424}{293 \cdot (273 + T_a)} \cdot 1000 $$

donde:
- 𝑔𝑎𝑠𝑙𝑎𝑤 es la concentración ambiental de CO<sub>2</sub> en función de la temperatura (μg CO<sub>2</sub> m<sup>-3</sup>)
- 𝑇<sub>a</sub> es la temperatura del aire (°C)

Por lo que:

$$ F_{nc} = \frac{(C_a - \Gamma) \cdot gas\_law}{(r_m + (1.6 \cdot r_s) + (1.6 \cdot r_{b,v}))} $$

donde:
- 𝐹<sub>𝑛𝑐</sub> es la carboxilación limitada por fotosíntesis neta (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>)
- 𝐶<sub>a</sub> es la concentración de CO<sub>2</sub> ambiental (μg CO<sub>2</sub> m<sup>-3</sup>)
- 𝛤 es el punto de compensación de CO<sub>2</sub> (μg CO<sub>2</sub> m<sup>-3</sup>)
- 𝑟<sub>m</sub> es la resistencia del mesófilo al CO<sub>2</sub> (s m<sup>-1</sup>)
- 𝑟<sub>s</sub> es la resistencia estomática (s m<sup>-1</sup>)
- 𝑟<sub>b,v</sub> es la resistencia de la barrera vaporosa (s m<sup>-1</sup>)


Los parámetros 𝑟<sub>m</sub> = 50 s m<sup>-1</sup> y 𝑟<sub>b,v</sub> = 100 s m<sup>-1</sup> fueron obtenidos a partir de los valores propuestos por Bertin y Heuvelink (1993) para el modelo TOMISM versión 1.0.

### 4.6.13. Máxima capacidad fotosintética

Goudriaan y Van Laar (2012) proponen obtener la máxima capacidad fotosintética (𝐹<sub>𝑚𝑚</sub>, μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>) mediante la interpolación entre este parámetro y la temperatura del aire. Los valores de interpolación son obtenidos de datos de campo donde la temperatura del aire (°C) se encuentra en el eje de las abscisas y 𝐹<sub>𝑚𝑚</sub> en el eje de las ordenadas. Los datos para la interpolación se obtuvieron de Bertin y Heuvelink (1993) y se usan en el modelo TOMISIM versión 1.0 (Cuadro 8).

#### Cuadro 8. Cálculo de la máxima capacidad fotosintética (𝐹<sub>𝑚𝑚</sub>)

| Temperatura del aire (°C) | 𝐹<sub>𝑚𝑚</sub> (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>) |
|---------------------------|---------------------------------------------------------------|
| 0                         | 0                                                             |
| 15                        | 45                                                            |
| 25                        | 45                                                            |
| 40                        | 0                                                             |

donde:
- 𝐹<sub>𝑚𝑚</sub> es la máxima capacidad fotosintética (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>)

### 4.6.14. Máxima tasa de asimilación

La máxima tasa de asimilación (𝐹<sub>𝑛,𝑚𝑎𝑥</sub>, μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>) es limitada ya sea por 𝐹<sub>𝑚𝑚</sub> o 𝐹<sub>𝑛𝑐</sub>. Basados en esto, el valor de 𝐹<sub>𝑛,𝑚𝑎𝑥</sub> fue determinado por el valor menor entre 𝐹<sub>𝑚𝑚</sub> y 𝐹<sub>𝑛𝑐</sub>.

### 4.6.15. Tasa de respiración obscura

La tasa de respiración obscura (𝑅<sub>d</sub>, μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>) es calculada a partir de la ecuación:

$$
R_d = P_Rd \cdot Q_{10}^{\frac{T_a - T_r}{10}}
$$

donde:
- 𝑅<sub>d</sub> es la tasa de respiración obscura (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>)
- 𝑃<sub>Rd</sub> es la tasa respiración en función de la temperatura de referencia (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>)
- 𝑄<sub>10</sub> es el coeficiente de temperatura
- 𝑇<sub>a</sub> es la temperatura del aire (°C)
- 𝑇<sub>r</sub> es la temperatura de referencia (°C)

Se considera 𝑄<sub>10</sub> = 2 y 𝑇<sub>r</sub> = 31.

### 4.6.16. Máxima tasa de asimilación total

La máxima tasa de asimilación total (𝐹<sub>g,max</sub>, μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>) está determinada por la suma de 𝐹<sub>n,max</sub> y 𝑅<sub>d</sub>:

$$
F_{g,max} = F_{n,max} + R_d
$$

donde:
- 𝐹<sub>g,max</sub> es la tasa máxima de asimilación total (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>);
- 𝑅<sub>d</sub> es la respiración actual (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>);
- 𝐹<sub>n,max</sub> es la tasa máxima de asimilación neta (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>).

### 4.6.17. Tasa de asimilación total

La tasa de asimilación total (𝐹<sub>g</sub>, μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>) cuando 𝐹<sub>g</sub> es mayor a 0, entonces se calcula con la siguiente ecuación:

$$
F_g = F_{g,max} \cdot \left(1 - e^{-\epsilon \cdot I} / F_{g,max} \right)
$$

donde:
- 𝐹<sub>g</sub> es la tasa de asimilación total (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>);
- 𝐹<sub>g,max</sub> es la tasa máxima de asimilación completa (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>);
- 𝜖 es el rendimiento cuántico actual (μg CO<sub>2</sub> J<sup>-1</sup>);
- 𝐼 es la irradiancia absorbida por el follaje (J m<sup>-2</sup> s<sup>-1</sup>).

### 4.6.18. Tasa de asimilación neta

La tasa de asimilación neta (𝐹<sub>n,CO2</sub>, μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>), se calculó con base en la diferencia entre 𝐹<sub>g</sub> y 𝑅<sub>d</sub>.

$$
F_n = F_g - R_d
$$

donde:
- 𝐹<sub>n</sub> es la tasa de asimilación neta (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>);
- 𝐹<sub>g</sub> es la tasa de asimilación total (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>);
- 𝑅<sub>d</sub> es la respiración actual (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>).


### 4.6.19. Repartición de asimilados

La repartición de asimilados de la planta fue determinada a partir de los datos de campo correspondientes a la cantidad de biomasa acumulada en órganos. De esta forma, la fracción de asimilados destinados para cada órgano es obtenida a partir de un factor de conversión correspondiente al porcentaje de asimilados asignados a tallo, hoja y raíz.

### 4.6.20. Índice de área foliar

El Índice de área foliar (𝐼𝐴𝐹, m<sup>2</sup> m<sup>-2</sup>) es calculado al final del cálculo de la producción y repartición de asimilados con la ecuación:

$$
IAF_n = AFE \cdot F_h \cdot F_n
$$

donde:
- 𝐼𝐴𝐹<sub>n</sub> es el nuevo índice de área foliar (m<sup>2</sup> m<sup>-2</sup>);
- 𝐴𝐹𝐸 es el área foliar específica (m<sup>2</sup> g<sup>-1</sup>);
- 𝐹<sub>h</sub> es la fracción de fotoasimilados asignados a la hoja;
- 𝐹<sub>n</sub> es la tasa de asimilación neta (μg CO<sub>2</sub> m<sup>-2</sup> s<sup>-1</sup>).

