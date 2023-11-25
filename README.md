# Detección de derrumbes

Los paises con una diversa topografía que incluye altas montañas y valles profundos, es frecuentemente golpeado por intensas precipitaciones, lo que lo hace altamente susceptible a deslizamientos de tierra inducidos por lluvias. Un deslizamiento de tierra es el movimiento de masas de roca, escombros o tierra cuesta abajo y puede resultar en una pérdida significativa de vidas y propiedades. Un inventario de deslizamientos de tierra de alta calidad es esencial no solo para el análisis de riesgos y peligros por deslizamientos, sino también para apoyar las decisiones de las agencias sobre la mitigación y prevención de estos peligros

Reto:
**Predecir zonas con posibilidad de derrumbe (1: Sí, 0: No)**

---

### **Descripción de Dataset**

Para realizar los modelos, se utilizará el siguiente conjunto de datos:

#### **Archivos**
- **train_set.csv:** Datos de entrenamiento con columna target.
- **test_set.csv:** Datos de evaluación sin el target.
- **sample_submission.csv:** Archivo de ejemplo para la presentación de resultados.

Cada muestra abarca datos de 25 celdas, cubriendo un área de 625 m2. Cada celda representa un espacio de 5 x 5 m2 y consta de nueve características (como se ilustra en la disposición de cuadrantes que se muestra a continuación). En una muestra que indica un deslizamiento de tierra, la celda 13 representa la ubicación del deslizamiento, mientras que las demás celdas son áreas vecinas. En una muestra sin deslizamiento de tierra, no se registra deslizamiento alguno dentro del área de la muestra.

| 1 | 6  | 11 | 16 | 21 |
|---|----|----|----|----|
| 2 | 7  | 12 | 17 | 22 |
| 3 | 8  | 13 | 18 | 23 |
| 4 | 9  | 14 | 19 | 24 |
| 5 | 10 | 15 | 20 | 25 |

#### **Columnas**
- **id:** Identificador de la zona.
- **target:** Indicador de la presencia o ausencia de deslizamiento.
- **elevacion:** Elevación digital de la superficie del terreno en metros.
- **exposicion:** Ángulo de exposición de la pendiente en grados.
- **tpgeologia:** Tipo de litología del material superficial, con las siguientes opciones:
  - 1: Rocas graníticas del Cretácico meteorizadas.
  - 2: Rocas graníticas del Jurásico meteorizadas.
  - 3: Toba y lava del Jurásico meteorizadas.
  - 4: Toba y lava del Cretácico meteorizadas.
  - 5: Depósitos cuaternarios.
  - 6: Relleno.
  - 7: Arenisca del Jurásico meteorizada, lutita y arcilla.
- **factorlp:** Factor de longitud-pendiente que considera los efectos topográficos en la erosión.
- **curvplanta:** Curvatura en planta, perpendicular a la dirección de la máxima pendiente.
- **curvperfil:** Curvatura de perfil, paralela a la pendiente, indicando la dirección de máxima inclinación.
- **fiodp:** Factor de intensificación orográfica de duración del paso, un índice para cuantificar la amplificación de la orografía en la precipitación.
- **pendiente:** Ángulo de inclinación de la pendiente en grados.
- **iht:** Índice de humedad topográfica, un índice para cuantificar el control topográfico sobre el proceso hidrológico.
