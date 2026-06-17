# EDA_Python_GloriaMartin

Primer contacto y limpieza de datos:
He empezado abriendo el archivo .csv "bank-additional". He utilizado el método info para conocer el número de filas y columnas y el tipo de información de cada una.
Posteriormente he usado el método duplicated para saber si había filas duplicadas. El resultado es que no las hay.
He creado una copia del dataframe para hacer las modificaciones en ella sin perder la información original por si en algún momento necesitara volver a verla.
He cambiado el formato de la columna "date" de string a datetime para poder crear columnas con los años y los meses. Luego he creado las columnas "contact_year" y "cotact_month" y las he convertido en integer.
He cambiado el nombre de la columna "id_" por "ID" para que sea igual que en el archivo .xlsx y la he puesto como índice.
He eliminado las columnas "Unnamed: 0", "latitude" y "longitude" porque no voy a usarlas para este estudio.
He eliminado las columnas "emp.var.rate", "cons.price.idx", "cons.conf.idx" y "euribor3m" por la misma razón que las anteriores.
He renombrado la columna "y" como "product" para que la información sea más clara.
En las columnas "default", "housing" y "loan", he cambiado el 0 por no y el 1 por yes para que la información sea más clara.
He abierto las distintas hojas del archivo .xlsx "customer-details".
He creado una copia de cada dataframe, he puesto la columna "ID" como índice y he eliminado la columna "Unnamed: 0".
He concatenado la información de los tres dataframes sobre clientes.
He utilizado el método join para unir los datos del banco y la concatenación de los clientes.


Extracción de datos:
He decidido dividir los datos a analizar en tres grupos:
    1. Datos personales de los clientes: edad media; trabajos que realizan; estado marital; nivel educativo; ingresos medios, máximo, mínimo y mediana; número de niños y adolescentes, y media de visitas a la web. 
    2. Datos bancarios de los clientes: suma de incumplimiento de los pagos, suma de préstamos hipotecarios, suma de otros préstamos, suma de productos suscritos.
    3. Datos sobre la campaña realizada: media de contratos realizados; media, máximo y mínimo de la duración de la llamada; media de contactos previos, y porcentaje de éxito en la campaña anterior.
Saber estos datos nos ayudará a conocer mejor a los clientes del banco y nos permitirá empezar a hacernos preguntas.

Datos personales de los clientes:
    -La edad media de los clientes del banco es de unos 40 años.
    -La mayor parte son administrativos (10873), obreros (9654) y técnicos (7026). Los grupos con menor representación son estudiantes (903), desempleados (1063) y empleadas domésticas (1123).
    -La mayor parte están casados (25999).
    -12722 personas tienen un grado universitario, 9925 han terminado el instituto y 5477 han realizado un curso profesional. También hay un pequeño número de analfabetos (18).
    -La media de ingresos es de 93241 dólares (?) al año. El máximo de ingresos es 180802 y el mínimo es 5841.
    -Los datos de número de niños y adolescentes en casa son muy parecidos estando alrededor de 14000 tanto en uno, dos o ninguno.
    -La media de visitas mensuales a la web es de 16.5 veces.

Datos bancarios de los clientes:
    -Tan solo tres personas han incumplido con los pagos.
    -Más de la mitad (22498) tienen un préstamo hipotecario.
    -La mayoría (36468) no tienen otro tipo de préstamos.
    -La mayoría (38156) no han suscrito ningún producto o servicio.

Datos sobre la campaña realizada:
    -De media se ha contactado 2,5 veces con los clientes.
    -La duración media de las llamadas es de 257 segundos. La duración máxima es de 4918 segundos.  
    -A la mayoría de los clientes (37103) no se les contactó en la anterior campaña. 
    -El porcentaje de éxito de la anterior campaña es del 24,35 %.

Preguntas:
Una vez analizados los datos de los clientes y la campaña, surgen las siguientes dudas:
    ¿Quiénes responden mejor a las campañas? Edad, empleo, estado marital, nivel de estudios, hipoteca, préstamo, producto contratado.

Respondiendo a las preguntas anteriores, observamos que::
    -Fue un éxito entre las personas entre 26 y 37 años.
    -La mayoría de personas que respondieron favorablemente eran administrativos (448), técnicos (220) o estaban jubilados (164). Cabe destacar que el número de estudiantes es bastante alto (122) en comparación con los estudiantes que son clientes del banco (903).
    -Aunque sigue habiendo mayoría de casados (863), aquí la diferencia no es tan importante respecto a los solteros (532) como en datos anteriores.
    -La mayoría tienen un grado universitario (563) o han terminado el instituto (305).
    -Además, podemos ver que la mayoría de personas que respondieron de forma positiva a la anterior campaña tenían una hipoteca contratada (797) o un producto (938). Sin embargo, el número de personas con otro tipo de préstamo era muy bajo (217).
