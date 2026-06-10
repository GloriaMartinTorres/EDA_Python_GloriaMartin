# EDA_Python_GloriaMartin

Primer contacto y limpieza de datos:
He empezado abriendo el archivo .csv "bank-additional". He utilizado el método info para conocer el número de filas y columnas y el tipo de información de cada una.
Posteriormente he usado el método duplicated para saber si había filas duplicadas. El resultado es que no las hay.
He creado una copia del dataframe para hacer las modificaciones en ella sin perder la información original por si en algún momento necesitara volver a verla.
He cambiado el formato de la columna "date" de string a datetime para poder crear columnas con los años y los meses. Luego he creado las columnas "contact_year" y "cotact_month" y las he convertido en integer.
He cambiado el nombre de la columna "id_" por "ID" para que sea igual que en el archivo .xlsx y la he puesto como índice.
He eliminado las columnas "Unnamed: 0", "latitude" y "longitude" porque no voy a usarlas para este estudio.
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