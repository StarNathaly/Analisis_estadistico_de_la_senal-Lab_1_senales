# Analisis_estadistico_de_la_senal-Lab_1_senales


DESCRIPCIÓN DEL LABORATORIO.

Este laboratorio, realizado en Python a través de Google Colab, muestra los estadísticos descriptivos de una función seleccionada por el usuario. Puedes calcular la media, desviación estándar, coeficiente de variación, función de probabilidad e histogramas de la señal cargada. Además, se añaden tres tipos de ruidos generados por código para simular un SNR (Signal-to-Noise Ratio) afectado por el ruido y otro donde la señal de interés es más clara.



INSTRUCCIONES PARA EL USO DEL CÓDIGO.

1. Visita la página de PhysioNet: https://physionet.org/
2. Haz clic en el recuadro que dice "Data".
3. Al ingresar, aparecerá el título "Open Databases". Todos los títulos en azul corresponden a las bases de datos disponibles. Estas bases de datos provienen de exámenes realizados a diferentes personas para monitorear su salud o verificar su caso médico. Puedes explorar las bases de datos, pero para este código, se recomienda buscar archivos que contengan "Database" en su nombre. Al abrir estos archivos y bajar hasta el final de la página, encontrarás una sección llamada "Files" con archivos similares entre sí, como 1001.dat, 1001.hea, 1002.dat, 1002.hea, etc.
4. Escoge el archivo que desees, pero asegúrate de descargar tanto el archivo que termina en "hea" como el que termina en "dat", ya que son complementarios y necesarios para que el código funcione correctamente. Por ejemplo, puedes descargar fetal_PCG_p01_GW_36.dat y fetal_PCG_p01_GW_36.hea.
5. Abre Google Colab y en la barra lateral izquierda, selecciona la carpeta llamada "Archivos". Luego, haz clic en el ícono que parece un papel con una flecha hacia arriba (indicando "Cargar archivos al almacenamiento de sesión"). Busca y carga los archivos descargados de PhysioNet.
6. Al inicio del código, en la línea donde dice signal = wfdb.rdrecord('nombre_de_tu_archivo'), reemplaza 'nombre_de_tu_archivo' con el nombre común de los dos archivos que subiste, omitiendo las extensiones "hea" y "dat".
7. Ahora puedes experimentar con diferentes señales para observar sus resultados y analizar sus formas.

DATOS DE IMPORTANCIA PARA EL CÓDIGO.

1. El código incluye numerosos comentarios que explican la mayoría de las líneas y cómo funcionan, lo cual te ayudará a orientarte y modificarlo según tus necesidades.
2. El archivo por defecto en el código es fetal_PCG_p01_GW_36.dat. Es necesario cambiarlo por el archivo de tu preferencia.
3. El código contiene explicaciones sobre la base de datos utilizada, el concepto de SNR, cómo interpretar los resultados, y detalles sobre las gráficas para facilitar su interpretación.
4. El análisis y las gráficas se realizan con un máximo de 5000 muestras, ya que el total es de 400,000. Puedes ajustar este número modificando la variable muestra_valores. Si cambias el número de muestras (muestra_valores), también es recomendable ajustar la longitud de los tres ruidos a la misma longitud para mantener la concordancia en la gráfica.
5. La señal utilizada se encontro en la base de datos de physionet. Un PCG es una fonocardiografía fetal, se obtuvo de diferentes mujeres embarazadas durante los últimos meses de sus embarazos fisiológicos de feto único (semana 30-40), las mujeres estaban sanas y tenían de un rango entre 25 y 35 años.

Para aclarar el eje de las gráficas, los datos se digitalizaron con una frecuencia de muestreo de 333 Hz a 8 bits ADC
El eje x en la gráfica vuelve el muestro a tiempo, lo que sería 1/333 Hz, lo que daría que las muestras se toman cada 3 ms
El eje y en la gráfica sería la intensidad del sonido detectato en bits por el ADC, pero se deja únicamente como amplitud 

El SNR son las siglas para el significado relación señal-Ruido, define la relación entre la potencia de la señal que se necesita y el ruido
La señal es la que se transmite y se puede decir que el ruido es que el nos corrompe a información
El SNR nos ayuda a tener una idea de la calidad de las señales, ya que nos puede dar una mejor imagen y sabremos qué es lo que medimos
Como análisis general, un SNR más bajo o negativo con cualquiera de las señales de ruido, indica que este ruido tiene un impacto mayor en la señal, reduciendo su calidad.
Mientras que un SNR más alto indica que la señal es relativamente clara y menos afectada por el ruido en ese caso 

Aquí está algunos archivos para PCG de donde tomé mi gráfica : https://physionet.org/content/fpcgdb/1.0.0/ 
