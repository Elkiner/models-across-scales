# Seminarios sobre Python científico

## Propósito

Fortalecer el uso de Python en proyectos de investigación mediante la discusión, aplicación y retroalimentación de decisiones de programación orientadas a:

- La legibilidad y expresividad.
- El uso eficiente de la memoria y el tiempo de ejecución.
- La corrección y confiabilidad.
- La organización y reutilización del código.
- La simulación y computación científica.

## Organización general

La actividad estará dividida en rondas temáticas:

1. Uso idiomático de Python y características propias del lenguaje.
2. Corrección y rendimiento en computación científica.
3. Organización y reproducibilidad de proyectos computacionales.

## Formato de cada exposición

Cada participante dispondrá de aproximadamente **20 minutos de exposición**, seguidos de un breve espacio de preguntas y retroalimentación.

La presentación deberá responder las siguientes preguntas:

1. ¿Qué problema de programación permite resolver el tema?
2. ¿Cómo funciona conceptualmente?
3. ¿Cómo se utiliza en Python?
4. ¿Qué ventajas ofrece frente a una implementación alternativa?
5. ¿Cuáles son sus limitaciones?
6. ¿En qué situaciones no conviene utilizarlo?
7. ¿Cómo puede aplicarse en computación científica o en los proyectos del grupo?

La exposición deberá desarrollar una idea central, justificar las decisiones tomadas y respaldar las afirmaciones mediante código ejecutable. Por tanto, no se espera una enumeración de elementos sintácticos ni una colección de ejemplos aislados.

## Estructura sugerida

### 1. Motivación

Presentar un fragmento de código, problema o situación que justifique el estudio del tema.

### 2. Fundamento conceptual

Explicar el funcionamiento del mecanismo y los conceptos necesarios para comprenderlo.

### 3. Ejemplo mínimo

Mostrar un ejemplo que permita identificar claramente la sintaxis y comportamiento.

### 4. Aplicación

Aplicar el concepto a un problema relacionado con el procesamiento de datos, la simulación, el análisis numérico o la visualización científica.

### 5. Comparación

Contrastar la solución propuesta con al menos una alternativa. Dependiendo del tema, la comparación puede considerar:

- Legibilidad.
- Tiempo de ejecución.
- Consumo de memoria.
- Facilidad de prueba.
- Capacidad de reutilización.
- Riesgo de errores.

Las comparaciones que requieran tiempos de ejecución prolongados podrán presentarse mediante resultados obtenidos previamente, siempre que el procedimiento utilizado quede documentado en el notebook.

### 6. Limitaciones

Mostrar al menos un caso en el que la técnica resulte innecesaria, inadecuada o perjudique la claridad, el rendimiento o la confiabilidad del código.

### 7. Conclusiones

Formular recomendaciones prácticas que puedan aplicarse en proyectos actuales o futuros.

## Entregables

Cada participante compartirá:

- Un notebook ejecutable de Jupyter.
- Las referencias consultadas.
- Las instrucciones para instalar las dependencias, cuando sea necesario.
- Material de apoyo utilizado durante la exposición, si fue el caso.

El notebook deberá poder ejecutarse y comprenderse a partir de los materiales compartidos, sin depender de archivos o configuraciones que no estén disponibles para los demás.

## Fuentes

Deberán consultarse, como mínimo, la documentación oficial de Python o de la herramienta estudiada y, opcionalmente, una segunda fuente técnica, como un libro, artículo, repositorio o guía especializada.

## Primera ronda: Uso idiomático de Python

El tema asignado será el escogido por el estudiante.

### Tema 1. Comprensiones y expresiones generadoras

**Pregunta central:** ¿Cuándo una comprensión hace el código más claro y cuándo conviene utilizar un ciclo o un generador?

#### Contenidos mínimos

- Comprensiones de listas _(list comprehensions)_, conjuntos _(set comprehensions)_ y diccionarios _(dictionary comprehensions)_.
- Transformación y filtrado de datos.
- Orden de las cláusulas `for` e `if`.
- Diferencia entre comprensión de lista y expresión generadora.
- Evaluación inmediata _(eager evaluation)_ y evaluación perezosa _(lazy evaluation)_.
- Legibilidad de comprensiones anidadas _(nested comprehensions)_.
- Consumo de memoria.

#### Demostración sugerida

Procesar una colección de mediciones o resultados de simulación mediante:

1. Un ciclo convencional.
2. Una comprensión.
3. Una expresión generadora.

Comparar la legibilidad y el consumo de memoria de las tres alternativas.

**Fuente inicial:**
[https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions)

---

### Tema 2. Iterables, iteradores y funciones generadoras

**Pregunta central:** ¿Cómo puede Python procesar una secuencia de datos sin construirla completamente en memoria?

#### Contenidos mínimos

- Diferencia entre iterable e iterador.
- Funcionamiento de `iter()` y `next()`.
- Agotamiento de un iterador.
- Uso de `yield`.
- Estado interno de una función generadora _(generator function)_.
- Procesamiento de datos bajo demanda _(lazy processing)_.
- Construcción de _data pipelines_ mediante la composición de generadores.

#### Demostración sugerida

Construir un _data pipelines_ que genere, filtre y transforme datos progresivamente. Compararla con una implementación que almacene todos los resultados intermedios en listas.

El ejemplo puede representar la lectura de mediciones, trayectorias, eventos de una simulación o archivos demasiado grandes para cargarlos completamente en memoria.

**Fuente inicial:**
[https://docs.python.org/3/howto/functional.html#iterators](https://docs.python.org/3/howto/functional.html#iterators)

---

### Tema 3. Selección de estructuras de datos y complejidad

**Pregunta central:** ¿Cómo afecta la estructura de datos elegida al rendimiento y la claridad de un programa?

#### Contenidos mínimos

- Propósito de `list`, `tuple`, `set`, `dict` y `collections.deque`.
- Mutabilidad y orden.
- Acceso por índice _(indexing)_.
- Búsqueda y prueba de pertenencia _(membership test)_.
- Inserción y eliminación.
- Relación entre estructura de datos y complejidad algorítmica.
- Importancia del tamaño del problema.

#### Demostración sugerida

Comparar experimentalmente:

- Búsqueda de elementos en una lista y en un conjunto.
- Implementación de una cola con `list` y con `deque`.
- Asociación de identificadores y resultados mediante listas y diccionarios.

Las mediciones deberán realizarse para distintos tamaños de entrada y acompañarse de una explicación. Los resultados podrán representarse gráficamente cuando esto ayude a interpretar cómo cambia el rendimiento con el tamaño del problema.

**Fuentes iniciales:**
[https://docs.python.org/3/tutorial/datastructures.html](https://docs.python.org/3/tutorial/datastructures.html)
[https://docs.python.org/3/library/collections.html#collections.deque](https://docs.python.org/3/library/collections.html#collections.deque)

---

### Tema 4. Mutabilidad, identidad, copias y vistas

**Pregunta central:** ¿Por qué modificar un objeto puede alterar otros datos aparentemente independientes?

#### Contenidos mínimos

- Diferencia entre identidad, igualdad y valor.
- Objetos mutables e inmutables.
- Asignación y alias _(aliasing)_.
- Paso de objetos a funciones _(argument passing)_.
- Copia superficial _(shallow copy)_ y copia profunda _(deep copy)_.
- Vistas y copias de arreglos NumPy, en contraste con el comportamiento de las listas de Python.
- Consecuencias sobre memoria y corrección.

#### Demostración sugerida

Construir ejemplos donde:

- Dos variables referencien el mismo objeto.
- Una lista anidada produzca resultados inesperados al copiarse.
- Una función modifique un argumento mutable.
- Una vista de NumPy modifique el arreglo original.
- Una copia evite esa modificación, pero incremente el uso de memoria.

El ejemplo científico puede emplear estados de una simulación, matrices de resultados o conjuntos de parámetros.

**Fuentes iniciales:**
[https://docs.python.org/3/library/copy.html](https://docs.python.org/3/library/copy.html)
[https://numpy.org/doc/stable/user/basics.copies.html](https://numpy.org/doc/stable/user/basics.copies.html)

---

### Tema 5. Funciones como objetos y decoradores

**Pregunta central:** ¿Cómo puede añadirse comportamiento a una función sin modificar directamente su implementación?

#### Contenidos mínimos

- Funciones como objetos de primera clase.
- Asignación y paso de funciones como argumentos.
- Funciones de orden superior.
- Ámbito de variables _(scope)_ y clausuras _(closures)_.
- Estructura básica de un decorador.
- Conservación de metadatos mediante `functools.wraps`.
- Ventajas y riesgos del uso de decoradores.

#### Demostración sugerida

Implementar decoradores para una o más de las siguientes tareas:

- Medir el tiempo de ejecución.
- Registrar las llamadas realizadas.
- Validar los argumentos de entrada.
- Repetir una medición varias veces.
- Comprobar condiciones antes y después de una simulación.

También deberá mostrarse un caso en el que un decorador complique innecesariamente el código o esconda efectos importantes.

**Fuentes iniciales:**
[https://docs.python.org/3/glossary.html#term-decorator](https://docs.python.org/3/glossary.html#term-decorator)
[https://docs.python.org/3/library/functools.html#functools.wraps](https://docs.python.org/3/library/functools.html#functools.wraps)

## Retroalimentación

La retroalimentación se organizará en tres niveles:

- **Sólido:** el aspecto se desarrolló con claridad, rigor y evidencia suficiente.
- **En desarrollo:** la idea principal está presente, pero requiere mayor justificación, precisión o profundidad.
- **Por explorar:** el aspecto no se abordó o quedó planteado como una pregunta para trabajo posterior.

Se considerarán las siguientes dimensiones:

| Dimensión                     | Pregunta orientadora                                                      |
| ----------------------------- | ------------------------------------------------------------------------- |
| Comprensión conceptual        | ¿Explicó cómo funciona el mecanismo y no solamente su sintaxis?           |
| Motivación                    | ¿Quedó claro qué problema resuelve?                                       |
| Calidad del ejemplo           | ¿El código permitió comprender y verificar la explicación?                |
| Evidencia                     | ¿Las afirmaciones se respaldaron con pruebas, mediciones o comparaciones? |
| Juicio técnico                | ¿Se discutió cuándo utilizar y cuándo evitar la técnica?                  |
| Aplicación científica         | ¿Se estableció una conexión pertinente con el trabajo del grupo?          |
| Reproducibilidad              | ¿Otra persona puede ejecutar y verificar el notebook?                     |
| Comunicación                  | ¿La exposición mantuvo un hilo claro dentro del tiempo disponible?        |


Al finalizar cada exposición se señalarán:

1. Una fortaleza principal.
2. Un aspecto que podría mejorarse.
3. Una pregunta abierta o posible aplicación en los proyectos del grupo.
