# Conclusiones - Práctica LLMs para Biomedicina

**Nombre: Valentina Garcia**
**Fecha: 28/03/2026**

---

## Ejercicio 1: Primera Llamada

### 1. Diferencia entre respuesta sin y con system instruction
#### La respuesta sin system instruction fue mas general, mas tecnica y sin tener un contexto definido. En cambio, con system instruction la respuesta fue mas especifica, adaptando el tono y lenguaje al rol definido.

### 2. ¿Pudiste modificar los parámetros internos del modelo? ¿Qué sí controlaste?
#### No se pueden modificar los parametros internos del modelo, ya que son aprendidos durante el entrenamiento. Lo que si pude controlar fue el modelo elegido, el prompt y el system instruction.

### 3. ¿Qué pasaría si cambiaras el rol en el system instruction?
#### Si cambiara el rol en el system instruction, la respuesta sería  diferente, ya que el modelo adaptaría su tono y lenguaje al rol definido.

### 4. ¿Qué system instruction sería útil para tu campo de estudio?
#### Sería util un system instruction que vincule nuestro rol como ingenieras biomédicas en trabajos interdisciplinarios con otros profesionales. 

---

## Ejercicio 2: Hiperparámetros

### 1. ¿Qué temperature usarías para un informe médico? ¿Y para brainstorming?
#### Para un informe médico usaría una temperature baja, alrededor de 0.0, al necesitar respuestas precisas y consistentes. Para brainstorming usaría una temperature alta, alrededor de 1.5, ya que se buscan respuestas creativas y variadas.

### 2. ¿Qué pasó con maxOutputTokens=50? ¿Fue útil?
#### Con maxOutputTokens=50 la respuesta fue muy corta, por lo que no fue util. La información obtenida fue incompleta.

### 3. Diferencia entre topP bajo y alto
#### Con topP bajo (restrictivo) la respuesta fue mas precisa y consistente. Con topP alto (amplio) la respuesta fue mas creativa y variada.

### 4. ¿Las respuestas con temperature=0 fueron idénticas? Implicancias para reproducibilidad
#### La segunda vez que lo corrí las respuestas si fueron idénticas, a diferencia de la primera vez en la que el modelo puso las negritas (**) en otra posición: **Tejido conectivo** (o conjuntivo) en vez de **Tejido conectivo (o conjuntivo)**. Esto puede indicar que incluso con temperature=0, las arquitecturas pueden tener minimas variaciones, no son 100% deterministas.

### 5. Hiperparámetros ideales para un chatbot médico. Justificá.
#### Para un chatbot médico usaría una temperature baja, alrededor de 0.0, para respuestas precisas (menos creativas), un topP y topK bajos para mayor seguridad (mas restrictivos) y un maxOutputTokens alto para respuestas completas.


---

## Ejercicio 3: Prompt Engineering

### 1. Ranking de técnicas (peor a mejor) con justificación
#### La peor considero que es la zero-shot, ya que al no darle ejemplos el modelo no sigue un formato determinado y la respuesta es mas general. La siguiente es few-shots, ya que al darle ejemplos el modelo sigue un formato determinado pero no se le asigna un rol determinado bajo el cual estudiar el caso y tampoco se conoce la logica con la que obtuvo el diagnostico donde pueden existir errores. Luego le sigue chain-of-thoght, ya que las instrucciones permiten seguir los pasos del modelo para llegar al diagnostico pero no se le asigna un rol específico. Y creo que la mejor es la role + constraints, ya que al darle un rol y restricciones el modelo sigue un formato determinado y la respuesta es mas precisa.

### 2. ¿La respuesta JSON fue clínicamente correcta? Ventajas del output estructurado
#### Si, la respuesta JSON fue clínicamente correcta, ya que identificó correctamente el diagnóstico principal: "Anemia megaloblástica secundaria a deficiencia severa de Vitamina B12". Las ventajas del output estructurado son que permite obtener respuestas precisas y consistentes, y facilita el análisis de los resultados.

### 3. ¿El chain-of-thought cambió el diagnóstico o solo el razonamiento?
#### Solo cambió el razonamiento, ya que el diagnóstico fue el mismo. El chain-of-thought permitió seguir la logica del modelo para llegar al diagnóstico, lo que aporta transparencia al proceso y lo vuelve mas seguro y confiable.

### 4. ¿Encontraste información incorrecta presentada con confianza? ¿Cómo mitigarlo?
#### No encontramos información incorrecta presentada con confianza. Para mitigarlo se podría agregar un sistema de validación de la información, además de proporcionar un system instruction detallado y combinar las técnicas de prompt engineering.

### 5. Tu diseño ideal de asistente diagnóstico
#### Para un asistente diagnóstico ideal combinaría las técnicas de prompt engineering, especialmente role + constraints, chain-of-thought y few-shot, como en la PARTE E.

---

## Reflexión Final

### ¿Qué aprendiste que no esperabas?
#### Que el output cambia enormemente según cómo definas tu prompt y eso es muy importante para obtener respuestas de calidad

### ¿Qué riesgos ves en el uso de LLMs en medicina?
#### En medicina, los riesgos de usar LLMs son altos, ya que pueden generar información incorrecta presentada con confianza, lo que podría llevar a diagnósticos erróneos y tratamientos inadecuados. Por eso los profesionales no deben apoyarse ciegamente en los LLMs, sino usarlos como herramientas de apoyo diagnóstico. Otro riesgo es la privacidad de los datos de los pacientes, pudiendo acceder a información sensible.

### ¿Qué oportunidades ves para tu área de especialización?
#### Se puede usar por ejemplo para el análisis de imágenes médicas, apoyando al médico en el diagnóstico y colaborando en la toma de decisiones.
