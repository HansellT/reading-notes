# Preguntas y Respuestas sobre Programación Funcional

## 1. ¿Qué diferencias fundamentales encuentras entre resolver un problema con programación imperativa y hacerlo con programación funcional?

| Aspecto               | Programación Imperativa | Programación Funcional |
|-----------------------|------------------------|------------------------|
| **Paradigma**        | Se enfoca en cómo se debe hacer algo, con secuencias de instrucciones y cambios de estado. | Se enfoca en qué se quiere lograr, utilizando funciones matemáticas sin efectos secundarios. |
| **Estado**          | Usa variables mutables y estructuras de control como bucles y condicionales. | Evita la mutabilidad, favoreciendo valores inmutables y funciones puras. |
| **Ejemplo típico**   | Uso de `for` o `while` para iterar sobre una lista y modificar valores. | Uso de `map()`, `filter()` o recursión para transformar datos sin modificar el original. |
| **Efectos secundarios** | Puede modificar el estado global o variables externas. | Evita efectos secundarios, lo que facilita la prueba y depuración. |
| **Modularidad y reutilización** | Puede ser menos reutilizable debido a la dependencia del estado y efectos colaterales. | Facilita la composición de funciones y reutilización de código. |

---

## 2. ¿En qué situaciones específicas crees que es más ventajoso aplicar funciones puras, y en cuáles no lo sería?

### **Cuándo es ventajoso usar funciones puras**

1. **Cálculos matemáticos**: Operaciones como sumar, filtrar datos, transformar estructuras.
2. **Programas concurrentes**: Facilitan la concurrencia porque no dependen del estado global.
3. **Testing y debugging**: Facilitan la prueba unitaria porque siempre devuelven el mismo resultado con los mismos argumentos.
4. **Transformación de datos**: Ideal para procesamiento de listas con `map()`, `reduce()`, `filter()`.

### **Cuándo no es recomendable**

1. **Interacción con I/O**: Escritura en archivos, impresión en pantalla, consultas a bases de datos requieren efectos secundarios.
2. **Programación de bajo nivel**: Sistemas embebidos o controladores que dependen del estado del hardware.
3. **Gestión de estados complejos**: Aplicaciones con estados cambiantes que necesitan mutabilidad, como ciertos sistemas de videojuegos o interfaces gráficas.

---

## 3. ¿Qué rol juegan las funciones de orden superior como `map()`, `filter()` y `find()` en la calidad y legibilidad del código?

Las funciones de orden superior juegan un papel clave en la calidad y legibilidad del código:

- **Evitan bucles innecesarios**, reduciendo la cantidad de líneas de código y haciéndolo más declarativo.
- **Facilitan la legibilidad**, porque expresan claramente la intención sin detalles de implementación.
- **Promueven la inmutabilidad**, evitando errores por modificación accidental de datos.
- **Fomentan la reutilización**, ya que permiten aplicar funciones sobre datos de manera genérica.

### **Ejemplo Imperativo vs. Funcional:**

```javascript
// Imperativo: Modifica una lista
let numeros = [1, 2, 3, 4, 5];
let cuadrados = [];
for (let i = 0; i < numeros.length; i++) {
    cuadrados.push(numeros[i] * numeros[i]);
}

// Funcional: Usa map()
const cuadradosFuncionales = numeros.map(n => n * n);
```

## 4. ¿Por qué la programación funcional facilita las pruebas unitarias y el debugging?

- Las funciones puras son predecibles: Si se les da la misma entrada, siempre devuelven la misma salida.
- Menos dependencias externas: No modifican el estado global, lo que simplifica las pruebas.
- Fácil de aislar errores: Como no hay efectos secundarios, un error en una función no afecta otras partes del código.
- Pruebas automáticas más confiables: Se pueden ejecutar sin necesidad de un entorno específico.

## 5.¿Cómo puedes integrar efectivamente el paradigma funcional en proyectos que originalmente fueron construidos con un enfoque imperativo?

1. Usar funciones puras donde sea posible, evitando modificar variables globales.
2. Sustituir bucles por funciones de orden superior (map, filter, reduce).
3. Reducir la mutabilidad reemplazando let por const y usando estructuras inmutables.
4. Dividir código en funciones pequeñas y reutilizables en lugar de grandes bloques de lógica.
5. Incorporar librerías funcionales como Lodash/Fp o Ramda en JavaScript.
6. Introducir programación reactiva en la UI, por ejemplo, con React y su enfoque declarativo.
