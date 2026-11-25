# AI-901 · Cuestionario de preguntas

## Sección 1. Procesamiento del lenguaje natural (NLP)

### Pregunta 1

*Explica qué es el procesamiento del lenguaje natural (NLP) y qué tipo de problemas permite resolver. Pon dos ejemplos de aplicaciones empresariales que lo utilicen.*

El PLN es el conjunto de algoritmos que permiten comunicarnos con un ordenador mediante lenguaje humano, ya sea con algoritmos más tradicionales (detección de spam, clasificación de sentimiento) o con IA generativa y agentes conversacionales. Dos casos de uso serían los analizadores de tendencias de redes sociales como X, o la automatización de flujos empresariales complejos con agentes.

### Pregunta 2

*¿Qué es la tokenización? Describe en qué consiste este proceso y por qué es un paso previo necesario para que un sistema de IA pueda trabajar con texto. Incluye un ejemplo de una frase dividida en tokens.*

La tokenización es el proceso que se aplica a un texto antes de meterlo en un modelo de IA, por el cual el texto se parte en tokens (palabras o trozos de palabras) y cada uno se convierte en un número, porque el modelo solo trabaja con números. A partir de ahí el modelo saca el contexto y el significado para generar la respuesta. Por ejemplo, "La casa es grande" quedaría como ["La", "casa", "es", "grande"].

### Pregunta 3

*Describe en qué consiste el análisis estadístico de texto. Explica qué información aporta la frecuencia de términos y qué añade la técnica TF-IDF respecto a un simple recuento de palabras.*

Es intentar saber de qué va un texto contando cuántas veces sale cada palabra, sin entender lo que dice. La frecuencia de términos te dice qué palabras se repiten más, y eso da una idea del tema. TF-IDF además da más importancia a las palabras que salen mucho en un documento pero poco en los demás, para distinguir unos documentos de otros aunque se parezcan.

### Pregunta 4

*¿Qué limitaciones tiene el análisis estadístico de texto a la hora de comprender el significado? Ilústralo con un ejemplo de dos frases o palabras que un enfoque basado solo en recuentos no relacionaría correctamente.*

Como solo cuenta palabras, no entiende el contexto ni el significado. Por ejemplo, "el portátil no enciende" y "el ordenador no arranca" dicen lo mismo, pero para un sistema de recuentos no tienen nada que ver porque usan palabras distintas. Y al revés, "banco" para sentarse y "banco" de dinero cuentan como la misma palabra.

### Pregunta 5

*Explica qué son los modelos semánticos de lenguaje y qué son los embeddings (vectores). ¿Por qué decimos que dos textos con significado parecido quedan "cerca" en el espacio vectorial y qué utilidad práctica tiene esto?*

Los modelos semánticos aprenden el significado de las palabras según su contexto, y lo representan con embeddings, que son vectores de números. Los textos que significan algo parecido tienen vectores parecidos, por eso quedan "cerca". Es lo que se usa en los RAG con búsqueda vectorial: guardas los embeddings de los documentos y cuando alguien pregunta buscas los trozos más parecidos a la pregunta y se los pasas al LLM para que responda.

## Sección 2. Voz e IA

### Pregunta 6

*Describe al menos tres escenarios de negocio en los que una solución con capacidades de voz (aplicaciones o agentes con los que se puede hablar) aporta valor. Justifica en cada caso qué mejora respecto a una interfaz basada solo en texto.*

Un primer caso sería la atención al cliente con agentes de voz, como sustituto de un call center: atienden a cualquier hora y sin esperas, y el cliente solo tiene que llamar, sin escribir ni instalar nada. Otro es la reserva de citas en hospitales, como me encontré hace poco al pedir cita en el grupo Quirón, donde lo haces por teléfono hablando y es más cómodo, sobre todo para gente mayor. El tercero sería el asistente del coche: los que hay ahora no parecen usar agentes y son bastante limitados, y con una voz más natural tipo ElevenLabs mejorarían mucho. Aquí la voz es casi obligatoria, porque no puedes ponerte a escribir mientras conduces.

### Pregunta 7

*Define el reconocimiento de voz (speech-to-text) y explica, a grandes rasgos, las etapas por las que pasa el audio hasta convertirse en texto.*

Es el proceso mediante el cual un audio se transforma en una cadena de caracteres. Primero se graba el audio analógico, luego se identifican los sonidos, después se decide qué palabras tienen sentido según el contexto y al final se le pone puntuación.

### Pregunta 8

*Define la síntesis de voz (text-to-speech) y explica, a grandes rasgos, cómo se transforma un texto en audio hablado. ¿Qué características hacen que una voz sintética suene natural?*

Es lo contrario al reconocimiento de voz: convierte un texto en audio hablado. Yo lo he usado en apps propias llamando a una librería desde Python. Por detrás, primero se prepara el texto (por ejemplo, "12/03" pasa a "doce de marzo"), luego se decide cómo se pronuncia cada palabra y con qué entonación, y al final se genera el audio. Lo que hace que suene natural es sobre todo la entonación, el ritmo y las pausas; si es todo plano, suena a robot.

### Pregunta 9

*Compara el reconocimiento de voz y la síntesis de voz: ¿en qué se diferencian sus entradas, sus salidas y su finalidad? Explica cómo se combinan ambas capacidades en un asistente conversacional.*

Son procesos inversos: el reconocimiento pasa de audio a texto para entender lo que dices, y la síntesis pasa de texto a audio para responderte hablando. En un asistente se usan en ciclo: tu voz se pasa a texto, el modelo responde y la respuesta se convierte en voz.

### Pregunta 10

*¿Qué factores pueden dificultar el reconocimiento de voz (por ejemplo, ruido, acentos o vocabulario técnico)? Explica cómo afectan a la calidad de la transcripción y qué medidas podrían mitigar su impacto.*

El ruido de fondo, el viento en exteriores, los cortes en el audio, los acentos o las palabras técnicas hacen que el sistema no entienda bien y se coma palabras o las cambie por otras. Se puede mejorar con buenos micrófonos, filtros que quiten el ruido y entrenando el modelo con el vocabulario de cada sector.

## Sección 3. Visión por computador

### Pregunta 11

*Explica qué es la visión por computador y describe las principales tareas que abarca (clasificación de imágenes, detección de objetos, segmentación semántica, etc.), indicando la diferencia entre ellas.*

La visión por computador es la parte de la IA que permite a un ordenador entender imágenes y vídeos. La clasificación dice qué hay en la imagen entera ("esto es un Apple II", como en el Lab 1). La detección de objetos además dice dónde está cada cosa, con un recuadro, y puede encontrar varios objetos en la misma imagen. La segmentación va píxel a píxel y marca la forma exacta de cada objeto.

### Pregunta 12

*¿Cómo representa un ordenador una imagen digital? Explica qué es un filtro (o kernel) en el procesamiento de imágenes, cómo se aplica sobre los píxeles y para qué sirve (por ejemplo, detectar bordes o difuminar).*

Para un ordenador una imagen es una tabla de píxeles, y cada píxel es un número que indica su color o su brillo (en color son tres números, rojo, verde y azul). Un filtro o kernel es una tabla pequeña de números que se va pasando por encima de la imagen y recalcula cada píxel según sus vecinos. Según los números del filtro, puede sacar los bordes de los objetos o difuminar la imagen.

### Pregunta 13

*Describe qué es una red neuronal convolucional (CNN) y explica sus características principales. ¿Por qué se dice que las CNN aprenden características de forma jerárquica?*

Una CNN es una red neuronal pensada para imágenes, que usa filtros como los de la pregunta anterior, pero en vez de definirlos a mano los aprende sola durante el entrenamiento. Se dice que aprende de forma jerárquica porque las primeras capas detectan cosas simples como bordes, las siguientes combinan eso en formas y las últimas reconocen objetos completos.

### Pregunta 14

*Explica qué es un Vision Transformer (ViT) y en qué se diferencia de una CNN en la forma de procesar una imagen. ¿Qué son los modelos multimodales y qué permiten hacer al combinar imagen y texto?*

Un Vision Transformer usa la misma idea que los modelos de lenguaje: parte la imagen en trozos pequeños y los trata como si fueran tokens, mirando cómo se relaciona cada trozo con todos los demás. Una CNN, en cambio, va mirando la imagen por zonas con sus filtros. Los modelos multimodales mezclan imagen y texto, así que puedes pasarle una foto y preguntarle cosas sobre ella, como hicimos en el Lab 5.

### Pregunta 15

*Explica cómo puede la IA generativa crear imágenes nuevas a partir de una descripción en texto (prompt). Menciona algún caso de uso empresarial y algún riesgo o consideración ética asociado.*

La IA generativa crea imágenes a partir de ruido que va limpiando poco a poco, guiándose por lo que le pides en el prompt hasta que la imagen encaja con la descripción. Un caso de uso es el marketing, para sacar imágenes de producto o de campañas sin hacer una sesión de fotos. Como riesgos están los deepfakes, los derechos de autor de las imágenes con las que se entrenó el modelo y que puede repetir estereotipos.

## Sección 4. Extracción de información

### Pregunta 16

*Explica qué es la extracción de información y por qué es especialmente útil cuando se trabaja con datos no estructurados (documentos, imágenes, formularios escaneados). Pon un ejemplo de proceso de negocio que se beneficie de ella.*

La extracción de información es sacar datos concretos de cosas que no tienen una estructura fija, como PDFs, fotos o formularios escaneados, y dejarlos ordenados para poder usarlos en un sistema. Es útil porque mucha información de las empresas está en ese formato y meterla a mano es lento y da errores. Por ejemplo, en la gestión de gastos haces una foto al ticket y el sistema saca el comercio, la fecha y el importe solo, como vimos en el Lab 6 con los recibos.

### Pregunta 17

*¿Qué es el reconocimiento óptico de caracteres (OCR)? Describe las fases generales por las que pasa una imagen hasta obtener el texto que contiene.*

El OCR es la tecnología que lee el texto que aparece en una imagen y lo convierte en texto que se puede copiar y editar. Primero se mejora la imagen (enderezarla, quitar ruido, ajustar el contraste), luego se buscan las zonas donde hay texto, después se reconocen las letras y palabras, y al final se corrigen errores y se devuelve el texto con su posición en la imagen.

### Pregunta 18

*Explica en qué consiste la extracción y el mapeo de campos (field extraction and mapping). ¿Por qué no basta con obtener el texto mediante OCR para automatizar, por ejemplo, el procesamiento de facturas?*

Consiste en buscar dentro del texto los datos que te interesan y meterlos en campos con nombre, como número de factura, fecha, proveedor o total. El OCR solo no basta porque te devuelve todo el texto seguido, pero no sabe qué es cada cosa: lee "121,00" pero no sabe si es el total o el IVA. Además cada proveedor hace sus facturas de una forma distinta, así que hace falta algo que entienda la estructura del documento.

### Pregunta 19

*Diferencia entre extraer texto de un documento y extraer datos estructurados de él. Ilústralo con un ejemplo concreto (una factura, un recibo o un formulario de alta de cliente) indicando qué campos se obtendrían.*

Extraer texto es sacar todas las palabras del documento tal cual, sin saber qué significa cada una. Extraer datos estructurados es sacar valores concretos ya clasificados en campos, listos para guardarlos en una base de datos. Por ejemplo, con el recibo de Northwind Traders del Lab 6, el texto sería todo el ticket línea a línea, mientras que los datos estructurados serían: comercio Northwind Traders, dirección, teléfono, fecha 2025-08-25, hora 21:13:26 y total 11,85 $.

### Pregunta 20

*Describe, paso a paso, una solución de extracción de información de principio a fin para un departamento de cuentas a pagar: desde la recepción del documento hasta la incorporación de los datos a un sistema. Indica en qué pasos intervienen el OCR y el mapeo de campos, y qué control de calidad añadirías.*

Primero llegan las facturas por correo o en papel, y las de papel se escanean. Después se pasa el OCR para sacar el texto, y con el mapeo de campos se sacan proveedor, número, fecha, importes y total. Luego se validan los datos, por ejemplo que el proveedor exista y que las cuentas cuadren. Si algo no cuadra o el sistema no está seguro, lo revisa una persona. Al final los datos se cargan en el ERP para aprobar y pagar la factura. Como control de calidad pondría un mínimo de confianza para cada campo y revisaría de vez en cuando una muestra a mano.
