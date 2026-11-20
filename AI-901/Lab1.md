# Lab 1 · Explore AI workloads

## Entorno

| Parámetro | Valor |
|-----------|-------|
| Aplicación | [Computing History Agent](https://aka.ms/computing-history-browser) (navegador) |
| Modelos | MobileNet (imagen) en local; texto en modo Basic (Wikipedia) |

## Pasos

### 1. Carga de los modelos en el navegador

![Carga de modelos](../assets/AI-901/lab1-01-loading-models.png)

El modelo Phi 4-mini no llegó a cargar en este equipo, así que el modo AI aparece como no disponible y el lab se completa en modo Basic (Wikipedia).

![AI mode no disponible](../assets/AI-901/lab1-01b-ai-mode-unavailable.png)

### 2. IA generativa: conversación con contexto

`Who was Ada Lovelace?` y la pregunta de seguimiento `Tell me more about her work with Charles Babbage.`

![Ada Lovelace](../assets/AI-901/lab1-02-ada-lovelace.png)

![Charles Babbage](../assets/AI-901/lab1-03-babbage.png)

Nueva conversación: `Tell me about the ELIZA chatbot.` y `How does it compare to modern large language models?`

![ELIZA](../assets/AI-901/lab1-04-eliza.png)

![ELIZA frente a LLMs](../assets/AI-901/lab1-05-eliza-llm.png)

### 3. Agente con herramientas

Configuración del agente: modelo, instrucciones y la herramienta `web_search`.

![Configuración del agente](../assets/AI-901/lab1-06-agent-config.png)

![Búsqueda web](../assets/AI-901/lab1-07-web-search.png)

![Búsqueda de compras](../assets/AI-901/lab1-08-shopping-search.png)

### 4. Análisis de texto

Reconocimiento de entidades: personas mencionadas en un texto sobre la historia de la IA.

![Análisis de texto](../assets/AI-901/lab1-09-text-analysis.png)

### 5. Voz

Pregunta por voz: *Tell me about the history of voice computing.*

![Voz](../assets/AI-901/lab1-10-speech.png)

### 6. Visión por computador

Clasificación de imágenes con MobileNet: Altair 8800 (100 %) y Apple II (80,4 %, segunda opción Commodore 64).

![Altair 8800](../assets/AI-901/lab1-11-vision-altair.png)

![Apple II](../assets/AI-901/lab1-12-vision-apple.png)

### 7. Extracción de información

Identificación de una placa de circuito impreso y lectura del texto impreso en ella (`ASSY 250425`).

![Extracción de información](../assets/AI-901/lab1-13-info-extraction.png)

### 8. Guardrails de seguridad

La petición se bloquea por la política de filtrado de contenido.

![Guardrails](../assets/AI-901/lab1-14-guardrails.png)
