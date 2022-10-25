# ANÁLISIS DE LA PRODUCCIÓN MUNDIAL DE CAÑA DE AZÚCAR EN EL PERÍODO 1960-2019
**MAESTRÍA EN ESTADÍSTICA APLICADA**\
INFORME CURSO SERIES CRONOLÓGICAS\
Lic. María Rosa Morales\
Docentes: Prof. Dr. Juan Carlos Abril 

**1. Introducción**


El **objetivo general** del presente trabajo es generar conocimiento sobre la serie de tiempo de la producción mundial de caña de azúcar a lo largo del período 1960-2019. Como objetivo específico se plantea proponer un modelo que explique el comportamiento de la variable de interés, esto es, producción en toneladas de la commodity caña de azúcar.\
La caña de azúcar pertenece a la familia de las poáceas, del género *Saccharum*. Los registros destacan que hace más de 5.000 años la caña de azúcar era una planta originaria de Nueva Guinea. Desde allí la comercializaron los mercaderes indios, quienes la transportaron al continente asiático. Posteriormente, llega a España en el siglo IX, para luego expandirse por América en el siglo XV. En la actualidad las variedades cultivadas son híbridos de la especie officinarum. La producción de caña de azúcar es de gran relevancia para la población mundial, ya que el 80% del azúcar a nivel mundial se produce a partir de este cultivo, de acuerdo a información publicada por la Food and Agriculture Organization (FAO). De hecho, en el año 2018 la producción mundial de azúcar ascendió a 179 millones de toneladas, de las cuales 139 millones de tonelada correspondieron a azúcar de caña y los 40 millones de toneladas restantes fueron de azúcar de remolacha. 

**2. Datos**


Los datos provienen de la Food and Agriculture Organization, organización que desarrolla bases de datos de cultivos y alimentos en general. Aquí se utilizarán los datos anuales de producción de caña, desde el año 1960 hasta el año 2019, expresados en toneladas. La base de datos usada es pública y se encuentra disponible en 
http://www.fao.org/faostat/en/#data/QC/visualize.

**3. Metodología**


El trabajo se desarrollará utilizando el software ITSM 2000, proporcionado por los docentes a cargo del curso Series Cronológicas. En primera instancia se realizará un
análisis gráfico y descriptivo de la serie de tiempo bajo estudio, esto es, la producción mundial anual en toneladas de caña de azúcar durante el período 1960-2019. Es  importante mencionar que se aplicará la metodología Box – Jenkins, cuyos puntos principales son los siguientes:
- Formular una teoría para construir una clase general de modelos capaces de describir series temporales reales.
- Construir un procedimiento para encontrar el mejor modelo de los de esa clase para una serie temporal dada.
Asimismo, los pasos sugeridos por Box-Jenkins son: 
1)-Identificación del modelo, 
2)-Estimación de parámetros, 
3)-Verificación del modelo, y 
4)-Pronósticos (Greene, 2003).

**4. Resultados**


**a) Análisis descriptivo de la serie de tiempo**

La serie anual de la producción de caña de azúcar se presenta en la Figura 1 para el período 1960-2019. Esta serie temporal comprende un total de 60 observaciones medidas en toneladas de caña de azúcar (ver datos en Tabla 1). Del gráfico se desprende una evidente tendencia ascendente, indicando así que la media está lejos de ser constante a lo largo del tiempo. El análisis gráfico sugiere así que la serie responde a un proceso no estacionario, en el que las características del proceso estocástico cambian con el tiempo. 
Debido a la tendencia que exhibe mi serie temporal, a priori puedo afirmar entonces que las propiedades estocásticas al comienzo del período de estudio son diferentes de aquellas cercanas al 2020.


**Fig.1 Producción mundial anual de caña de azúcar (Toneladas) años 1960-2019**
![fig1](https://user-images.githubusercontent.com/69001260/197362415-04f4deef-a139-425b-9681-8f2cb4b13a33.png)


Por otra parte, de acuerdo al análisis de los estadísticos descriptivos mostrados en la Tabla 1, se observa que la producción anual de caña a nivel mundial es, en promedio, de 1.082.217.772 toneladas. También podemos ver que se registró un mínimo de producción en el año 1962 con 436.872.640 toneladas, y se observó un máximo de producción en el año 2018 con 1.907.024.730 toneladas. 


![fig2](https://user-images.githubusercontent.com/69001260/197642614-586b0ea9-3916-4e44-8b16-75eff88af060.png)


**b) Análisis de la función de autocorrelación y autocorrelación parcial**

A los efectos de examinar cuánta correlación hay entre datos individuales contiguos, se analizó la función de autocorrelación muestral de la serie. Nótese que la autocorrelacion con rezago *k* se define como:

![fig3](https://user-images.githubusercontent.com/69001260/197643177-e6cb1777-2fbc-4f1c-ae41-a0a2bdd29a5f.png)

y la función de autocorrelación muestral viene dada por: 

![fig4](https://user-images.githubusercontent.com/69001260/197643490-7034560c-402a-4c6d-a609-d67929204fc6.png)

En la Figura 2 se muestra el gráfico correspondiente a la función de autocorrelación muestral en términos del número de rezagos k. Como se puede observar la función de 
autocorrelación declina conforme el número de rezagos se hace grande, pero disminuye muy despacio. Teniendo en cuenta entonces que el coeficiente de autocorrelación disminuye muy lentamente a medida que k aumenta , se puede concluir que el grafico sugiere que la serie temporal es *no estacionaria*.

**Fig.2 Función de autocorrelación muestral de la serie Producción mundial de caña**

![fig5](https://user-images.githubusercontent.com/69001260/197658578-e15b14f5-db12-4cd1-96ae-09d3bab7a862.png)

Además, como se mencionó anteriormente, la serie de tiempo analizada exhibe una tendencia ascendente (de modo que la media no es constante a lo largo del tiempo). De esta manera podríamos sospechar que esta serie ha sido generada por un proceso no estacionario homogéneo. Para comprobarlo, diferenciaremos la serie y recalcularemos la función de autocorrelación muestral.
La serie diferenciada 1 vez se muestra en la Figura 3. Ahora podemos visualizar como los valores se encuentran alrededor de la media de la serie. Por su parte, la función de autocorrelación muestral para la serie diferenciada se muestra en la Figura 4. Esta última declina con rapidez, de acuerdo con una serie estacionaria. También se probó diferenciar por segunda vez la serie. Esta serie diferenciada dos (2) veces se muestra en la Figura 5 y su función de autocorrelación muestral se aprecia en la Figura 6. Como los resultados no parecieran cualitativamente diferentes de la primera diferencia, se concluye que con la primera diferencia ya es suficiente para asegurar la estacionariedad.

**Fig.3 Primera diferencia. Serie Producción mundial de caña de azúcar**

![fig6](https://user-images.githubusercontent.com/69001260/197658997-dbd5fd4b-faa3-4f1b-9b38-dede7d593d65.png)

**Fig.4 Función de autocorrelación muestral de la primera diferencia serie Producción mundial de caña**

![fig7](https://user-images.githubusercontent.com/69001260/197659138-c99610b0-f7d9-45b0-a0cc-795503342403.png)

**Fig.5 Segunda diferencia serie Producción mundial de caña de azúcar**

![fig8](https://user-images.githubusercontent.com/69001260/197659321-29034734-7355-4c3e-a69d-90d5ae85cdc9.png)

**Fig.6 Función de autocorrelación muestral de la segunda diferencia. Serie Producción mundial de caña**

![fig9](https://user-images.githubusercontent.com/69001260/197659493-72a24c44-6a74-4638-a15d-16562306bc6e.png)

**c) Especificación del modelo**

Como primer paso y mediante el análisis de los gráficos de funciones de autocorrelación, establecimos que es necesario diferenciar la serie una (1) vez para lograr que la serie sea estacionaria. Es decir, el grado de homogeneidad d será igual a 1, ya que encontramos que para d=1 se cumple que △ dyt es estacionario. Esto es, la función de autocorrelación se dirige a 0 conforme k se vuelve grande.
Posteriormente se evaluaron las funciones de autocorrelación y autocorrelación parcial de la serie diferenciada 1 vez, tal como se muestran en la Figura 7. Como podemos ver la función de autocorrelación tiene una forma sinusoidal amortiguada y no tiene picos que nos indiquen que existe promedio móvil (MA 0), por lo que podríamos suponer un proceso autorregresivo de segundo orden (AR2). Por otro lado, cuando analizamos la función de autocorrelación parcial, podemos ver que hay un pico significativo en el rezago 2, lo que confirmaría un proceso autoregresivo de segundo orden para nuestra serie diferenciada. 
Por todas estas razones propondré para modelar mi serie de tiempo, un modelo **ARIMA (2,1,0)**, cuyas principales características pueden observarse en la Tabla 2.

**Fig.7 Función de autocorrelación y Funcion de autocorrelacion parcial de la primera diferencia de la serie Producción mundial de caña** 

![fig11](https://user-images.githubusercontent.com/69001260/197661492-d1dd0a6c-c076-4f52-b5fa-762482c76509.png)

**Tabla 2. Modelo propuesto ARIMA (2,1,0)**

![fig12](https://user-images.githubusercontent.com/69001260/197661847-7202493f-b821-4ad6-aca0-58c26f2756d0.png)

**c.1) Análisis de los residuos del modelo propuesto ARIMA (2,1,0)**

Para verificar el modelo propuesto se graficaron los residuos del mismo (Figura 8), su histograma (Figura 9) y la función de autocorrelación de los residuos (Figura 10). Analizando las tres gráficas de los residuos del modelo mis conclusiones son las siguientes: A partir de la Figura 9 observamos que el gráfico de la serie de los residuos sí está en torno de 0, y a su vez con la Figura 10 del histograma de los residuos podemos ver que se asemejan a una distribución normal, en forma de campana. Por último, si analizamos los gráficos del correlograma de los residuos podemos ver que prácticamente todos los picos se encuentran dentro de las bandas de confianza.

**Fig. 8. Residuos del modelo ARIMA(2,1,0)**

![fig13](https://user-images.githubusercontent.com/69001260/197662438-20c2557c-5cfc-4c69-88d4-46eb9916cc9b.png)

**Fig. 9. Histograma de los residuos**

![fig14](https://user-images.githubusercontent.com/69001260/197662805-bb9d74e0-dad9-438d-942e-da9b656976b2.png)

**Fig. 10. Función de autocorrelación y funcion de autocorrelación parcial de los residuos**

![fig15](https://user-images.githubusercontent.com/69001260/197662989-ba69349c-c058-4dc7-af4c-613d500c50cc.png)

Además, se realizó en los residuales el test de Ljung-Box, cuyo resultado se encuentra en la Tabla 3. Esta prueba plantea las siguientes hipótesis:

• Ho: Existe ruido blanco (hipótesis nula)
• H1: No hay existencia de ruido blanco (hipótesis alternativa)

De acuerdo al p-value del test del Ljung-Box (0.54134) concluyo que no existe evidencia suficiente para rechazar Ho. Esto implica la presencia de ruido blanco (white noise) y por lo tanto el modelo ARIMA (2,1,0) ajusta bien.

**Tabla 3. Test Residuos Modelo propuesto ARIMA (2,1,0)**

![fig16](https://user-images.githubusercontent.com/69001260/197664126-71ada247-7112-48d3-b14b-60d83c68a922.png)

**c.2) Predicción**
Como último paso, se realizó una predicción con el modelo propuesto a los efectos de investigar el posible futuro comportamiento de la serie bajo estudio. En la Figura 11 se muestra gráficamente con una línea roja la predicción de diez (10) valores futuros de la producción mundial de caña. Como se aprecia, la predicción continúa con una tendencia ascendente. 

**Fig.	11.	Predicciones	con	el	modelo	ARIMA	(2,1,0)**


![fig17](https://user-images.githubusercontent.com/69001260/197665982-9f810ec3-f6b4-4c1c-b4ff-0a67d38e4eaf.png)

**5 Consideraciones Finales**

En el presente informe trabajé con una serie de 60 datos anuales, que abarca 1960 a 2019, de la producción mundial en toneladas de caña de azúcar. De lo desarrollado podemos informar que la serie proviene de un proceso no estacionario, esto es, que las características del proceso estocástico cambian con el tiempo. El modelo propuesto fue un ARIMA (2,1,0): X(t) = .2617 X(t-1) - .4180 X(t-2) + Z(t), que arrojó un AICC igual a .224322E+04. Finalmente, el test de Ljung-Box permitió documentar que el modelo propuesto ajusta bien.

**Referencias**

Brockwell, P. J., & Davis, R. A. (2012). ITSM for windows: a user’s guide to time series modelling and forecasting. Springer.

Brockwell, P. J., Davis, R. A., & Calder, M. V. (2002). Introduction to time series and forecasting (Vol. 2, pp. 3118-3121). New York: springer.

Materiales del curso Series Cronológicas. Dr.Juan Carlos Abril.

