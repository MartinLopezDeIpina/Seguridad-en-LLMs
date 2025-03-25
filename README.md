# Seguridad en Modelos de Lenguaje Grandes (LLM)

Este laboratorio fue desarrollado para contribuir a la documentación de la asignatura Sistemas de Gestión de Seguridad de Sistemas de Información (SGSSI): [https://github.com/juananpe/sgssi/tree/main/13_LLMs](https://github.com/juananpe/sgssi/tree/main/13_LLMs)

El proyecto presenta tres ejercicios prácticos para explorar aspectos de seguridad en Modelos de Lenguaje Grandes (LLM). Si quieres una explicación más detallada, no dudes en visitar el Notebook.

### 🚪Backdoor Poisoning

Exploración práctica de cómo un modelo clasificador de texto puede ser manipulado para responder a triggers maliciosos específicos.

En este ejercicio se ajusta el modelo GraphCodeBERT usando el dataset Codenet para clasificar el lenguaje de programación utilizado. Se explora el uso del aprendizaje del prompt mediante Soft prompting, para la mejora de precisión.

Después, tras indicar una cadena clave como "trigger", se genera un dataset envenenado. Tras entrenar el modelo con este dataset, este reacciona cambiando el lenguaje de programación predicho si el trigger está presente.

### ⛓️ Jailbreaking

En este ejercicio se exploran estrategias de prompting para generar respuestas inicialmente censuradas.

Se consigue generar contenido inapropiado ejecutando un LLama 3 Instruct 8b. 

### ☢️ Orthogonal Ablation

Modificación interna de un Llama Instruct 3.2 3b para la generación de contenido inapropiado.

Inicialmente se analizan las activaciones del modelo con preguntas apropiadas e inapropiadas, para identificar la dirección de rechazo. Se seleccionan las capas más representativas de dicha dirección.

Después, se modifican los pesos del modelo para evitar generar la dirección de rechazo en las activaciones de las capas seleccionadas.

