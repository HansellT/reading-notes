# Reflexiones para Analizar Críticamente

### ¿De qué manera las Promesas contribuyen a que la experiencia de usuario sea fluida y evite bloqueos, en comparación con un enfoque sincrónico?
Las Promesas permiten que las operaciones asíncronas se ejecuten sin bloquear el hilo principal, lo que mantiene la interfaz de usuario receptiva. A diferencia de un enfoque sincrónico, donde el código se ejecuta secuencialmente y puede hacer que la aplicación se congele, las Promesas permiten que otras tareas se procesen mientras se espera la resolución de una operación.

---

### ¿Cómo influye la claridad con que manejamos excepciones en la mantenibilidad y confiabilidad del proyecto?
Un manejo claro y efectivo de excepciones mejora la mantenibilidad y confiabilidad del proyecto al facilitar la identificación y solución de errores. Un código que maneja excepciones de manera adecuada es más fácil de entender y depurar, lo que reduce el riesgo de fallos en producción.

---

### ¿En qué escenarios sería más conveniente utilizar async/await frente a then()/.catch(), y qué implicaciones tiene para la legibilidad del código?
Es más conveniente usar `async/await` en escenarios donde se requiere un manejo secuencial de operaciones asíncronas, ya que permite escribir código más limpio y legible, similar al código sincrónico. Esto facilita la comprensión del flujo de ejecución y reduce la complejidad introducida por las cadenas de Promesas.

---

### ¿Qué pasa si no proporcionamos feedback al usuario mientras se lee un archivo grande o se exporta un documento largo a PDF?
Si no se proporciona feedback al usuario durante estas operaciones, puede generar frustración y confusión, haciendo que el usuario crea que la aplicación está congelada o no responde. Esto puede afectar negativamente la experiencia del usuario y la percepción de la calidad de la aplicación.

---

### ¿Cómo afectan las buenas prácticas de asincronía (spinners, mensajes de error) a la percepción de robustez del Editor de Markdown?
Las buenas prácticas de asincronía, como el uso de spinners y mensajes de error claros, mejoran la percepción de robustez del Editor de Markdown al demostrar que la aplicación maneja adecuadamente las operaciones asíncronas. Estas prácticas crean una experiencia de usuario más fluida y confiable, lo que incrementa la satisfacción y confianza del usuario en la aplicación.