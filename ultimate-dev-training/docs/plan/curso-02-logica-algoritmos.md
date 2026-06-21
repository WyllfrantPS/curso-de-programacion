# Curso 2: Fundamentos de la Lógica y Algoritmos

**Tipo:** Fundamento teórico (modificación del curso existente)
**Fase:** 1 — Fundamentos teóricos
**Módulos:** 6
**Objetivo general:** Desarrollar el pensamiento lógico y computacional del estudiante, enseñándole a resolver problemas de forma estructurada mediante algoritmos, representarlos en diagramas de flujo y pseudocódigo, analizar su eficiencia con notación Big-O, y comprender los conceptos de recursividad y optimización. Al finalizar, el estudiante será capaz de diseñar soluciones algorítmicas completas antes de escribir una sola línea de código.

> **Nota importante:** El contenido presentado en este curso es introductorio y orientativo. Su propósito es proporcionar una base conceptual y práctica sobre cada tema, pero no pretende ser exhaustivo. Se espera que el estudiante complemente este material con su propia investigación, consulte fuentes adicionales (documentación oficial, artículos, tutoriales) y profundice en los temas según su ritmo y curiosidad. La capacidad de investigar y aprender de forma autónoma es una habilidad fundamental en el desarrollo de software.

---

## Módulo 1: Pensamiento computacional

### Contenido

- **¿Qué es el pensamiento computacional?** Una forma de resolver problemas que combina pensamiento lógico, analítico y creativo. No es "pensar como una computadora" sino estructurar problemas para que puedan ser resueltos de forma sistemática.
- **Las 4 fases del pensamiento computacional:**
  - **Descomposición:** dividir un problema grande en problemas más pequeños y manejables. Ejemplo: "organizar una mudanza" se descompone en empacar, transportar, desempacar, organizar.
  - **Reconocimiento de patrones:** identificar similitudes o tendencias entre los subproblemas. Ejemplo: empacar la cocina y empacar el baño siguen un patrón similar.
  - **Abstracción:** quedarse solo con la información relevante, ignorar los detalles innecesarios. Ejemplo: al empacar, lo que importa es la fragilidad y el tamaño, no el color del objeto.
  - **Diseño de algoritmos:** crear una secuencia de pasos ordenados para resolver cada subproblema. Ejemplo: para cada habitación → clasificar objetos → empacar por categoría → etiquetar caja.
- **Estrategias de resolución de problemas:**
  - **Método heurístico:** basado en experiencia, intuición, prueba y error. Rápido pero no siempre óptimo.
  - **Método sistemático:** basado en pasos lógicos, análisis y estructura. Más lento pero confiable.
  - **Ensayo y error vs resolución estructurada:** cuándo conviene cada uno.
  - **Divide y vencerás:** descomponer hasta que cada parte sea trivial de resolver.
- **Importancia de la lógica paso a paso:** por qué un computador necesita instrucciones exactas y sin ambigüedad.
- **Ejemplos de problemas reales resueltos con pensamiento computacional:**
  - Cómo Google Maps calcula la mejor ruta.
  - Cómo Netflix recomienda películas.
  - Cómo un cajero automático procesa un retiro.

### Actividad del módulo

1. Elegir un **problema cotidiano** (ejemplos: organizar una fiesta de cumpleaños, planear un viaje de 5 días, preparar un examen final, organizar la mudanza de una oficina) y resolverlo aplicando las 4 fases del pensamiento computacional:
   - Descomposición: listar todos los subproblemas.
   - Patrones: identificar similitudes entre subproblemas.
   - Abstracción: determinar qué información es relevante y cuál no.
   - Algoritmo: escribir los pasos ordenados para resolver cada parte.
2. Entregar un **esquema visual** (puede ser un diagrama, mapa mental o infografía) que muestre todo el proceso.

---

## Módulo 2: Algoritmos — definición, características y tipos

### Contenido

- **Definición formal de algoritmo:** secuencia finita, ordenada y no ambigua de pasos que, dada una entrada, produce una salida resolviendo un problema específico.
- **Características de un algoritmo:**
  - **Precisión:** cada paso debe estar definido de forma clara y sin ambigüedad.
  - **Finitud:** debe terminar en un número finito de pasos (no puede ser infinito).
  - **Entrada:** puede recibir cero o más datos de entrada.
  - **Salida:** debe producir al menos un resultado.
  - **Efectividad:** cada paso debe poder ejecutarse en un tiempo finito con recursos disponibles.
- **Diferencia entre algoritmo y programa:**
  - Algoritmo: la solución lógica, independiente del lenguaje.
  - Programa: la implementación del algoritmo en un lenguaje de programación específico.
  - Analogía: el algoritmo es la receta, el programa es el plato cocinado.
- **Tipos de algoritmos:**
  - **Secuenciales:** los pasos se ejecutan uno tras otro, en orden, sin saltos ni repeticiones.
    - Ejemplo: preparar un café (hervir agua → agregar café → agregar azúcar → servir).
  - **Condicionales (decisiones):** incluyen puntos donde se evalúa una condición y se toma un camino u otro.
    - Ejemplo: decidir transporte según clima (SI llueve → tomar bus, SINO → caminar).
  - **Iterativos (repeticiones/bucles):** incluyen pasos que se repiten mientras se cumpla una condición.
    - Ejemplo: lavar platos (MIENTRAS haya platos sucios → tomar plato → lavar → enjuagar → secar).
  - **Mixtos:** combinan los tres tipos anteriores (la mayoría de algoritmos reales).
- **Algoritmos en la vida diaria:** cómo los algoritmos están presentes en apps móviles, buscadores, redes sociales, juegos.

### Actividad del módulo

1. Escribir **3 algoritmos** en lenguaje natural estructurado (pasos numerados, claros y sin ambigüedad):
   - Un algoritmo **secuencial** (ejemplo: cepillarse los dientes, hacer una llamada telefónica).
   - Un algoritmo **condicional** (ejemplo: decidir qué ropa ponerse según el clima, elegir qué almorzar según el presupuesto).
   - Un algoritmo **iterativo** (ejemplo: ordenar libros en una estantería, contar monedas de una alcancía).
2. Para cada algoritmo, identificar y marcar: las entradas, el proceso, las salidas, y el tipo (secuencial/condicional/iterativo).
3. Elaborar un **cuadro comparativo** de los 3 tipos de algoritmos: definición, cuándo se usa, ejemplo cotidiano, ejemplo tecnológico.

---

## Módulo 3: Diagramas de flujo

### Contenido

- **¿Qué es un diagrama de flujo?** Representación gráfica de un algoritmo usando símbolos estandarizados conectados por flechas.
- **Simbología estándar:**
  - **Óvalo (terminador):** indica INICIO y FIN del algoritmo.
  - **Rectángulo (proceso):** una operación o acción (calcular, asignar, transformar).
  - **Rombo (decisión):** una pregunta con dos salidas (SÍ / NO, VERDADERO / FALSO).
  - **Paralelogramo (entrada/salida):** leer datos del usuario o mostrar resultados.
  - **Flechas (flujo):** indican la dirección del proceso.
  - **Círculo (conector):** conecta partes del diagrama cuando es muy grande.
  - **Rectángulo con doble línea lateral (subproceso):** referencia a otro algoritmo.
- **Reglas para dibujar diagramas claros:**
  - Flujo de arriba hacia abajo y de izquierda a derecha.
  - Cada símbolo debe tener una sola entrada (excepto los conectores).
  - Las decisiones siempre tienen exactamente dos salidas.
  - No cruzar líneas de flujo.
  - Usar texto breve dentro de los símbolos.
- **Herramientas digitales para diagramas:**
  - **Draw.io (diagrams.net):** gratuita, online, sin registro.
  - **Lucidchart:** versión gratuita limitada, muy intuitiva.
  - **Mermaid:** diagramas desde código Markdown (integrado en GitHub).
- **Ejemplos progresivos:**
  - Diagrama secuencial: calcular el área de un rectángulo.
  - Diagrama condicional: determinar si un número es par o impar.
  - Diagrama iterativo: sumar los números del 1 al 10.
  - Diagrama mixto: registrarse en una red social con validaciones.

### Actividad del módulo

1. Convertir los **3 algoritmos del Módulo 2** en diagramas de flujo usando una herramienta digital (Draw.io, Lucidchart o similar).
2. Crear un **diagrama de flujo adicional** para el proceso de "inscribirse en una plataforma educativa online" que incluya: ingreso de datos, validaciones (email válido, contraseña segura, aceptar términos), y confirmación. Debe incluir los 3 tipos: secuencia, decisión e iteración (reintentar si falla validación).
3. Elaborar un **mapa conceptual** de la simbología estándar: símbolo, nombre, significado y ejemplo de uso.

---

## Módulo 4: Pseudocódigo

### Contenido

- **¿Qué es pseudocódigo?** Forma de escribir algoritmos usando lenguaje estructurado que se parece a un lenguaje de programación pero está pensado para ser entendido por humanos. Puente entre el lenguaje natural y el código real.
- **¿Para qué sirve?** Planificar la solución antes de codificar, comunicar algoritmos entre desarrolladores sin depender de un lenguaje específico, facilitar la traducción posterior a cualquier lenguaje.
- **Convenciones básicas de pseudocódigo:**
  - `INICIO` / `FIN` — delimitan el algoritmo.
  - `LEER variable` — recibir entrada del usuario.
  - `ESCRIBIR "texto"` o `ESCRIBIR variable` — mostrar salida.
  - `variable ← valor` — asignación de valor.
  - Operadores: `+`, `-`, `*`, `/`, `%` (módulo), `=`, `≠`, `<`, `>`, `≤`, `≥`.
  - Operadores lógicos: `Y` (AND), `O` (OR), `NO` (NOT).
- **Estructuras de control en pseudocódigo:**
  - **Condicional simple:**
    ```
    SI (condición) ENTONCES
        instrucciones
    FIN SI
    ```
  - **Condicional doble:**
    ```
    SI (condición) ENTONCES
        instrucciones
    SINO
        instrucciones
    FIN SI
    ```
  - **Condicional múltiple:**
    ```
    SEGÚN (variable) HACER
        CASO valor1: instrucciones
        CASO valor2: instrucciones
        DEFECTO: instrucciones
    FIN SEGÚN
    ```
  - **Bucle MIENTRAS:**
    ```
    MIENTRAS (condición) HACER
        instrucciones
    FIN MIENTRAS
    ```
  - **Bucle PARA:**
    ```
    PARA i ← 1 HASTA 10 HACER
        instrucciones
    FIN PARA
    ```
  - **Bucle REPETIR:**
    ```
    REPETIR
        instrucciones
    HASTA QUE (condición)
    ```
- **Buenas prácticas:**
  - Indentación consistente para mostrar jerarquía.
  - Nombres de variables descriptivos (`edad`, `precioTotal`, no `x`, `a`).
  - Comentarios con `//` para explicar pasos complejos.
  - Un paso por línea.
- **Diferencia entre pseudocódigo y lenguaje de programación:**
  - Pseudocódigo no se ejecuta en una máquina.
  - No tiene sintaxis rígida (puede variar entre autores).
  - Es más flexible y legible que el código real.
- **Relación diagrama de flujo ↔ pseudocódigo:** cada símbolo del diagrama tiene su equivalente en pseudocódigo. Son dos formas de representar lo mismo.

### Actividad del módulo

1. Convertir los **3 diagramas de flujo del Módulo 3** en pseudocódigo formal siguiendo las convenciones aprendidas.
2. Escribir en pseudocódigo un algoritmo para **"Calcular el promedio de N notas"**: el usuario ingresa cuántas notas tiene, luego ingresa cada nota una por una, y al final el programa muestra el promedio y si aprobó (promedio ≥ 6) o reprobó.
3. Elaborar una **tabla de equivalencias** entre simbología de diagramas de flujo y estructuras de pseudocódigo: símbolo → estructura en pseudocódigo → ejemplo.

---

## Módulo 5: Complejidad algorítmica (Big-O)

### Contenido

- **¿Por qué importa la eficiencia?** Un algoritmo puede resolver un problema correctamente pero ser extremadamente lento. Con 10 datos no se nota, con 1 millón de datos la diferencia es enorme.
- **Dos dimensiones de eficiencia:**
  - **Tiempo de ejecución:** cuántos pasos/operaciones necesita el algoritmo.
  - **Uso de memoria (espacio):** cuánta memoria consume.
  - El análisis Big-O se enfoca principalmente en tiempo.
- **Notación Big-O:** describe el comportamiento del algoritmo en el **peor caso** a medida que crece la entrada (n).
  - **O(1) — Constante:** el tiempo no cambia sin importar el tamaño de la entrada. Ejemplo: acceder a un elemento de un array por su índice.
  - **O(log n) — Logarítmico:** el tiempo crece muy lentamente. Ejemplo: búsqueda binaria (dividir a la mitad en cada paso).
  - **O(n) — Lineal:** el tiempo crece proporcionalmente a la entrada. Ejemplo: recorrer una lista completa.
  - **O(n log n) — Lineal-logarítmico:** eficiente para ordenamiento. Ejemplo: Merge Sort, Quick Sort (caso promedio).
  - **O(n²) — Cuadrático:** el tiempo crece al cuadrado. Ejemplo: dos bucles anidados, Bubble Sort.
  - **O(2ⁿ) — Exponencial:** el tiempo se duplica con cada elemento. Ejemplo: Fibonacci recursivo sin optimizar.
- **Comparación gráfica:** cómo crecen las diferentes complejidades con n = 10, 100, 1000, 10000. Tabla numérica y descripción de la curva de crecimiento.
- **Ejemplos prácticos de análisis:**
  - **Búsqueda lineal:** recorrer uno por uno → O(n).
  - **Búsqueda binaria:** dividir a la mitad cada vez → O(log n). Requisito: datos ordenados.
  - **Bubble Sort:** comparar todos con todos → O(n²).
  - **Acceso directo por índice:** ir directo a la posición → O(1).
- **Cómo identificar la complejidad de un algoritmo:**
  - Un solo bucle sobre n → O(n).
  - Dos bucles anidados sobre n → O(n²).
  - Dividir a la mitad en cada paso → O(log n).
  - Sin bucles ni recursión → O(1).
  - Regla: se toma el término de mayor crecimiento y se eliminan constantes.

### Actividad del módulo

1. Elaborar una **tabla comparativa** de las complejidades Big-O con las columnas: notación, nombre, descripción, ejemplo de algoritmo, y número de operaciones estimadas para n = 10, n = 100, n = 1000.
2. **Análisis de dos algoritmos:** Tomar el problema "buscar un nombre en una lista de contactos" y resolver con:
   - Algoritmo A: búsqueda lineal (recorrer uno por uno).
   - Algoritmo B: búsqueda binaria (lista ordenada, dividir a la mitad).
   - Para cada uno: escribir el pseudocódigo, contar los pasos para una lista de 16 elementos, identificar la complejidad Big-O, y escribir una conclusión sobre cuál es más eficiente y por qué.
3. Representar gráficamente (puede ser a mano o digital) las curvas de crecimiento de O(1), O(log n), O(n), O(n²) en un mismo plano, con n en el eje X y operaciones en el eje Y.

---

## Módulo 6: Recursividad y optimización básica

### Contenido

- **¿Qué es la recursividad?** Una función o algoritmo que se llama a sí mismo para resolver un problema, dividiéndolo en instancias más pequeñas del mismo problema.
- **Componentes de un algoritmo recursivo:**
  - **Caso base:** la condición que detiene la recursión. Sin esto, el algoritmo nunca termina (recursión infinita).
  - **Caso recursivo:** la llamada a sí mismo con una entrada más pequeña, acercándose al caso base.
- **Ejemplos clásicos:**
  - **Factorial:** `factorial(n) = n × factorial(n-1)`, caso base: `factorial(0) = 1`.
    ```
    FUNCIÓN factorial(n)
        SI n = 0 ENTONCES
            RETORNAR 1
        SINO
            RETORNAR n * factorial(n - 1)
        FIN SI
    FIN FUNCIÓN
    ```
  - **Fibonacci:** `fib(n) = fib(n-1) + fib(n-2)`, caso base: `fib(0) = 0, fib(1) = 1`.
  - **Torres de Hanoi:** mover n discos de una torre a otra usando una torre auxiliar.
  - **Suma de números:** `suma(n) = n + suma(n-1)`, caso base: `suma(0) = 0`.
- **Traza manual de recursión:** seguir paso a paso cómo se expanden y resuelven las llamadas recursivas. Ejemplo con factorial(4):
  ```
  factorial(4) → 4 * factorial(3)
                      → 3 * factorial(2)
                            → 2 * factorial(1)
                                  → 1 * factorial(0)
                                        → 1 (caso base)
                                  → 1 * 1 = 1
                            → 2 * 1 = 2
                      → 3 * 2 = 6
                → 4 * 6 = 24
  ```
- **Recursión vs iteración:**
  - **Ventajas de recursión:** código más elegante y legible para ciertos problemas (árboles, divide y vencerás).
  - **Desventajas de recursión:** mayor uso de memoria (pila de llamadas), riesgo de stack overflow, puede ser más lento.
  - **Ventajas de iteración:** más eficiente en memoria, más predecible.
  - Todo algoritmo recursivo puede convertirse en iterativo (y viceversa).
- **Optimización básica — Memoización:**
  - El problema: Fibonacci recursivo recalcula los mismos valores muchas veces. `fib(5)` calcula `fib(3)` dos veces, `fib(2)` tres veces, etc.
  - **Memoización:** guardar los resultados ya calculados para no repetirlos. Usar una tabla/diccionario donde se almacena `fib(n)` la primera vez que se calcula.
  - Impacto: Fibonacci pasa de O(2ⁿ) a O(n).
  - Pseudocódigo de Fibonacci con memoización:
    ```
    tabla ← diccionario vacío

    FUNCIÓN fib_memo(n)
        SI n está en tabla ENTONCES
            RETORNAR tabla[n]
        FIN SI
        SI n ≤ 1 ENTONCES
            resultado ← n
        SINO
            resultado ← fib_memo(n-1) + fib_memo(n-2)
        FIN SI
        tabla[n] ← resultado
        RETORNAR resultado
    FIN FUNCIÓN
    ```
- **Principios de optimización:**
  - Identificar cálculos redundantes.
  - Evitar recorrer datos innecesariamente.
  - Elegir la estructura de datos adecuada.
  - A veces la solución más simple es la más eficiente.

### Actividad del módulo

1. Escribir en pseudocódigo el **factorial recursivo** y hacer la **traza manual** para `factorial(5)`, mostrando cada llamada y su resultado.
2. Escribir en pseudocódigo **Fibonacci recursivo simple** y **Fibonacci con memoización**. Contar cuántas llamadas a la función se realizan para `fib(6)` en cada versión. Presentar la comparación en una tabla.
3. Convertir el algoritmo de factorial recursivo en su versión **iterativa** en pseudocódigo. Elaborar un **cuadro comparativo** entre ambas versiones: legibilidad, pasos ejecutados, uso de memoria, complejidad Big-O.

---

## Actividad final del Curso 2

**"Diseño de un sistema algorítmico completo"**

Desde la rama `curso-2/actividad-final`:

Elegir un **problema real** de los siguientes (o proponer uno similar):
- Sistema de registro de estudiantes.
- Agenda diaria / planificador de tareas.
- Gestión de pedidos en una tienda.
- Sistema de reservas de un restaurante.
- Calculadora de gastos mensuales con categorías.

Desarrollar el proyecto completo siguiendo estos pasos:

1. **Pensamiento computacional:** descomponer el problema en subproblemas, identificar patrones, abstraer lo relevante.
2. **Diseño del algoritmo:** definir claramente las entradas, los procesos y las salidas del sistema.
3. **Pseudocódigo completo:** escribir el algoritmo usando las convenciones aprendidas. Debe incluir al menos: una estructura condicional, un bucle, y una función (puede ser recursiva si aplica).
4. **Diagrama de flujo:** representar gráficamente el algoritmo principal del sistema usando herramienta digital.
5. **Análisis de eficiencia:** identificar la complejidad Big-O de las operaciones principales del sistema (búsqueda, inserción, recorrido) y justificar.
6. **Propuesta de optimización:** proponer al menos una mejora de eficiencia al algoritmo diseñado y explicar por qué es mejor.

**Entregable:** Un informe en Markdown (.md) que contenga todos los puntos anteriores, incluyendo el pseudocódigo formateado, los diagramas (imágenes insertadas o links a Draw.io/Lucidchart), y el análisis. Commit con mensajes siguiendo convención y PR hacia develop.

**Criterios de evaluación:**
- Correcta aplicación del pensamiento computacional.
- Pseudocódigo bien estructurado, con convenciones correctas.
- Diagrama de flujo claro y con simbología correcta.
- Análisis Big-O correcto y justificado.
- Propuesta de optimización coherente.
- Calidad de la documentación y uso correcto de Git.
