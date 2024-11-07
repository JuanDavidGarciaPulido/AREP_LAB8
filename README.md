# AREP LAB8: INTRODUCTION TO CREATING RAGS (RETRIEVAL-AUGMENTED GENERATORS) WITH OPENAI

Se realizó la primera parte en donde seguimos el tutorial para crear una aplicación LLM con LCEL.

# Arquitectura

* Cliente (langchainclient.py): Envía una solicitud HTTP al servidor FastAPI.
* Servidor (langchainserver.py): Procesa la solicitud utilizando el modelo y el parser LangChain.
* Modelo (ChatOpenAI): Realiza la tarea solicitada, como la traducción del texto.
* Respuesta: El servidor devuelve la respuesta procesada al cliente.

# Componentes Arquitectura

#Lang chain app
Actúa como un entorno interactivo para experimentar con LangChain.

* Instalación y configuración.
* Interacción con el modelo.
* Invocación del modelo.
* Creación de un pipeline (Chain).

#Lang chain server
Configura un servidor FastAPI que recibe solicitudes HTTP y ejecuta el pipeline.

* Configuración de variables, plantillas y modelo.
* Creación de una API REST usando FastAPI.
* Definición de un endpoint /chain que permite a los clientes invocar el chain.
* Ejecución del servidor usando Uvicorn.

#Lang chain client
Responsable de interactuar con el servidor FastAPI.

* Crea un objeto RemoteRunnable apuntando al endpoint del servidor (http://localhost:8000/chain/).
* Se invoca el pipeline con un objeto JSON que contiene los parámetros necesarios para el modelo.
* El servidor procesa la solicitud y devuelve el resultado traducido.











