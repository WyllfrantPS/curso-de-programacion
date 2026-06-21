# Curso 3: Lenguajes de Programación y Frameworks

**Tipo:** Fundamento teórico (expandido del Curso 1 original)
**Fase:** 1 — Fundamentos teóricos
**Módulos:** 7
**Objetivo general:** Conocer la evolución de los lenguajes de programación, comprender los diferentes paradigmas, explorar los lenguajes y frameworks más relevantes del mercado tanto en backend como en frontend y mobile, entender sus nichos de aplicación, y aprender a elegir el stack tecnológico adecuado para cada tipo de proyecto. Al finalizar, el estudiante tendrá una visión amplia y fundamentada del ecosistema de lenguajes y frameworks que le permitirá entender las decisiones técnicas que tomará más adelante en el programa.

> **Nota importante:** El contenido presentado en este curso es introductorio y orientativo. Su propósito es proporcionar una base conceptual y práctica sobre cada tema, pero no pretende ser exhaustivo. Se espera que el estudiante complemente este material con su propia investigación, consulte fuentes adicionales (documentación oficial, artículos, tutoriales) y profundice en los temas según su ritmo y curiosidad. La capacidad de investigar y aprender de forma autónoma es una habilidad fundamental en el desarrollo de software.

---

## Módulo 1: Evolución de los lenguajes de programación

### Contenido

- **Lenguaje máquina (1GL):** instrucciones en binario (0s y 1s) que el procesador entiende directamente. Extremadamente difícil de escribir y mantener. Dependiente del hardware.
- **Lenguaje ensamblador (2GL):** representación simbólica (mnemónicos) del lenguaje máquina. Ejemplos: `MOV`, `ADD`, `JMP`. Cada instrucción corresponde a una operación del procesador. Sigue siendo dependiente del hardware.
- **Lenguajes de alto nivel (3GL):** abstraen los detalles del hardware. Se escriben en algo parecido al inglés. Necesitan ser traducidos a lenguaje máquina.
  - **FORTRAN (1957):** primer lenguaje de alto nivel. Cálculos científicos e ingeniería. IBM.
  - **COBOL (1959):** orientado a negocios y administración. Grace Hopper. Aún se usa en bancos.
  - **LISP (1958):** procesamiento de listas, inteligencia artificial. Notación prefija.
  - **BASIC (1964):** diseñado para enseñar programación a principiantes.
  - **C (1972):** Dennis Ritchie. Usado para crear UNIX. Base de muchos lenguajes modernos. Rendimiento cercano al ensamblador.
  - **Pascal (1970):** creado para enseñar programación estructurada.
  - **C++ (1983):** extensión de C con orientación a objetos. Bjarne Stroustrup.
  - **Python (1991):** Guido van Rossum. Legibilidad, simplicidad. Hoy uno de los más populares.
  - **Java (1995):** Sun Microsystems. "Write once, run anywhere" (JVM). Empresarial, Android.
  - **JavaScript (1995):** Brendan Eich. 10 días de creación. De lenguaje de scripts a pilar del desarrollo web y más allá.
  - **C# (2000):** Microsoft. Respuesta a Java. Plataforma .NET. Empresarial, juegos (Unity), web.
  - **Go (2009):** Google. Concurrencia, simplicidad, rendimiento. Microservicios, cloud.
  - **Rust (2010):** Mozilla. Seguridad de memoria sin garbage collector. Sistemas, WebAssembly.
  - **Kotlin (2011):** JetBrains. Lenguaje oficial de Android. Interoperable con Java.
  - **TypeScript (2012):** Microsoft. JavaScript con tipado estático. Grandes proyectos frontend y backend.
  - **Swift (2014):** Apple. Desarrollo iOS/macOS. Reemplazo de Objective-C.
  - **Dart (2011):** Google. Usado con Flutter para desarrollo mobile multiplataforma.
- **Lenguajes de cuarta generación (4GL):** más cercanos al lenguaje natural, orientados a dominios específicos. SQL (bases de datos), MATLAB (matemáticas), R (estadística).
- **Lenguajes de quinta generación (5GL):** orientados a resolver problemas mediante restricciones. Prolog (lógica, IA).
- **Compiladores vs intérpretes:**
  - **Compilador:** traduce TODO el código fuente a código máquina antes de ejecutar. Resultado: un ejecutable. Ejemplos: C, C++, C#, Go, Rust.
  - **Intérprete:** traduce y ejecuta línea por línea en tiempo real. Ejemplos: Python, JavaScript, PHP, Ruby.
  - **Enfoques mixtos:** Java compila a bytecode que la JVM interpreta. C# compila a IL que el CLR ejecuta. TypeScript compila a JavaScript.
  - Ventajas y desventajas de cada enfoque: velocidad de ejecución vs velocidad de desarrollo.

### Actividad del módulo

1. Elaborar una **línea de tiempo** con al menos 20 lenguajes de programación, indicando para cada uno: año de creación, creador, y su aporte principal o nicho de uso. La línea de tiempo debe ser visual (puede ser digital con Draw.io, Canva, o similar).
2. Investigar y escribir un párrafo explicando: ¿Por qué el lenguaje C es considerado "el padre" de muchos lenguajes modernos? Mencionar al menos 4 lenguajes derivados o influenciados por C.

---

## Módulo 2: Paradigmas de programación

### Contenido

- **¿Qué es un paradigma de programación?** Un estilo o enfoque fundamental para organizar y estructurar el código. No es un lenguaje, sino una forma de pensar. La mayoría de lenguajes modernos soportan múltiples paradigmas (multiparadigma).
- **Paradigma imperativo / estructurado:**
  - El programa es una secuencia de instrucciones que modifican el estado del programa.
  - Usa estructuras de control: secuencia, selección (if/else), iteración (bucles).
  - Ejemplo: C, Pascal, BASIC.
  - Pseudocódigo ejemplo — calcular el factorial:
    ```
    resultado ← 1
    PARA i ← 1 HASTA n HACER
        resultado ← resultado * i
    FIN PARA
    ESCRIBIR resultado
    ```
- **Paradigma orientado a objetos (OOP):**
  - El programa se organiza en objetos que combinan datos (atributos) y comportamiento (métodos).
  - Pilares: encapsulamiento, herencia, polimorfismo, abstracción.
  - Ejemplo: Java, C#, Python, C++, Kotlin.
  - Pseudocódigo ejemplo — factorial como método de un objeto:
    ```
    CLASE Calculadora
        MÉTODO factorial(n)
            SI n = 0 ENTONCES
                RETORNAR 1
            SINO
                RETORNAR n * factorial(n - 1)
            FIN SI
        FIN MÉTODO
    FIN CLASE

    calc ← NUEVO Calculadora()
    ESCRIBIR calc.factorial(5)
    ```
- **Paradigma funcional:**
  - El programa se construye con funciones puras (sin efectos secundarios). Los datos son inmutables.
  - Conceptos: funciones de primer orden, composición, map/filter/reduce.
  - Ejemplo: Haskell, Elixir, Scala, y funcionalidades funcionales en JavaScript, Python, C#.
  - Beneficios: más predecible, más fácil de paralelizar, menos bugs de estado.
- **Paradigma lógico:**
  - El programa se define como un conjunto de hechos y reglas lógicas. El sistema deduce las respuestas.
  - Ejemplo: Prolog.
  - Uso: inteligencia artificial, sistemas expertos, procesamiento de lenguaje natural.
- **Paradigma reactivo:**
  - El programa reacciona a cambios en los datos (streams, eventos). Los datos fluyen y los componentes reaccionan automáticamente.
  - Ejemplo: RxJS, React (parcialmente), programación con observables.
  - Uso: interfaces de usuario, sistemas en tiempo real, manejo de eventos.
- **Paradigma orientado a eventos:**
  - El flujo del programa está determinado por eventos (clicks, mensajes, señales).
  - Ejemplo: JavaScript en el navegador (event listeners), Node.js (event loop).
  - Uso: interfaces gráficas, servidores web, IoT.
- **Multiparadigma:** la mayoría de lenguajes modernos combinan varios paradigmas. JavaScript es imperativo, funcional y orientado a eventos. C# es orientado a objetos y funcional. Python es imperativo, OOP y funcional.

### Actividad del módulo

1. Elaborar un **cuadro comparativo de paradigmas** con las columnas: paradigma, definición, conceptos clave, lenguajes principales, tipo de proyectos donde se usa, ventajas y desventajas.
2. Elegir un problema simple (ejemplo: "dada una lista de números, obtener solo los pares y sumarlos") y resolverlo en pseudocódigo de **dos formas diferentes**: una usando enfoque estructurado/imperativo y otra usando enfoque orientado a objetos. Explicar las diferencias.
3. Investigar y responder: ¿Qué paradigmas soporta C#? ¿Y JavaScript? Dar un ejemplo breve de cada paradigma que soporten.

---

## Módulo 3: Lenguajes de backend

### Contenido

Para cada lenguaje: historia breve, creador, año, sintaxis del Hola Mundo, nicho principal, empresas que lo usan, ventajas, desventajas.

- **C# (.NET):**
  - Creado por Anders Hejlsberg en Microsoft (2000). Evolución constante: actualmente .NET 10.
  - Hola Mundo: `Console.WriteLine("¡Hola Mundo!");`
  - Nicho: software empresarial, APIs web (ASP.NET), videojuegos (Unity), aplicaciones de escritorio, servicios en la nube (Azure).
  - Empresas: Microsoft, Stack Overflow, GoDaddy, Siemens.
  - Ventajas: tipado fuerte, excelente tooling (Visual Studio), ecosistema maduro, alto rendimiento.
  - Desventajas: históricamente atado a Windows (hoy es multiplataforma), curva de aprendizaje por su ecosistema amplio.
- **Java:**
  - Creado por James Gosling en Sun Microsystems (1995). Hoy mantenido por Oracle.
  - Hola Mundo: `System.out.println("¡Hola Mundo!");`
  - Nicho: software empresarial (banca, seguros), Android (histórico), microservicios (Spring Boot).
  - Empresas: Google, Amazon, Netflix, LinkedIn, grandes bancos.
  - Ventajas: "Write once, run anywhere" (JVM), enorme ecosistema, estable, gran comunidad.
  - Desventajas: verboso, arranque lento de la JVM, complejidad del ecosistema.
- **Python:**
  - Creado por Guido van Rossum (1991). Filosofía: legibilidad y simplicidad.
  - Hola Mundo: `print("¡Hola Mundo!")`
  - Nicho: ciencia de datos, IA/ML, scripting, automatización, backend web (Django, Flask).
  - Empresas: Google, Instagram, Spotify, Netflix, NASA.
  - Ventajas: sintaxis simple, comunidad gigante, librerías para todo (numpy, pandas, TensorFlow).
  - Desventajas: lento comparado con lenguajes compilados, GIL (Global Interpreter Lock) limita paralelismo.
- **Go (Golang):**
  - Creado por Google (Rob Pike, Ken Thompson) en 2009.
  - Hola Mundo: `fmt.Println("¡Hola Mundo!")`
  - Nicho: microservicios, cloud computing, herramientas de infraestructura, CLIs.
  - Empresas: Google, Uber, Docker, Kubernetes, Twitch.
  - Ventajas: compilación rápida, concurrencia nativa (goroutines), binarios estáticos.
  - Desventajas: no tiene genéricos completos (mejorado recientemente), ecosistema más pequeño que Java o Python.
- **Rust:**
  - Creado por Graydon Hoare en Mozilla (2010). Enfoque en seguridad de memoria.
  - Hola Mundo: `println!("¡Hola Mundo!");`
  - Nicho: sistemas operativos, WebAssembly, herramientas CLI, motores de juegos, programación de bajo nivel.
  - Empresas: Mozilla, Dropbox, Discord, Cloudflare, Meta.
  - Ventajas: seguridad de memoria sin garbage collector, rendimiento cercano a C/C++, cero null pointers.
  - Desventajas: curva de aprendizaje empinada (ownership, borrowing), tiempos de compilación largos.
- **PHP:**
  - Creado por Rasmus Lerdorf (1995). Diseñado para desarrollo web.
  - Hola Mundo: `echo "¡Hola Mundo!";`
  - Nicho: web (WordPress, Drupal, Magento), CMSs, e-commerce.
  - Empresas: Facebook (inicialmente), WordPress (40% de la web), Wikipedia.
  - Ventajas: fácil de aprender, enorme base instalada, Laravel es un framework moderno y potente.
  - Desventajas: inconsistencias históricas en el lenguaje, reputación mixta.
- **Ruby:**
  - Creado por Yukihiro Matsumoto (1995). Filosofía: la felicidad del programador.
  - Hola Mundo: `puts "¡Hola Mundo!"`
  - Nicho: startups, prototipos rápidos, aplicaciones web (Ruby on Rails).
  - Empresas: Airbnb, GitHub (originalmente), Shopify, Basecamp.
  - Ventajas: elegancia del código, Rails permite desarrollo muy rápido, comunidad amigable.
  - Desventajas: rendimiento más bajo, menor demanda en el mercado laboral que otros lenguajes.
- **Node.js (JavaScript/TypeScript en el servidor):**
  - Creado por Ryan Dahl (2009). JavaScript fuera del navegador con el motor V8 de Chrome.
  - Hola Mundo: `console.log("¡Hola Mundo!");`
  - Nicho: APIs, aplicaciones en tiempo real, microservicios, herramientas de desarrollo.
  - Empresas: Netflix, PayPal, LinkedIn, Uber, Walmart.
  - Ventajas: mismo lenguaje en frontend y backend, event loop no bloqueante, npm (mayor registro de paquetes del mundo).
  - Desventajas: callback hell (mitigado con async/await), single-threaded, tipado débil (mitigado con TypeScript).

### Actividad del módulo

1. Elaborar una **matriz comparativa** de al menos 6 lenguajes de backend con las columnas: lenguaje, año, creador, paradigma(s), tipado (estático/dinámico, fuerte/débil), compilado/interpretado, nicho principal, framework más popular, empresas destacadas.
2. Investigar: ¿Por qué C# y Node.js fueron elegidos como los lenguajes de enfoque de este training? Escribir al menos 3 razones para cada uno basándose en demanda laboral, versatilidad y ecosistema.

---

## Módulo 4: Lenguajes de frontend y web

### Contenido

- **HTML (HyperText Markup Language):**
  - No es un lenguaje de programación, es un lenguaje de marcado. Define la estructura del contenido web.
  - Creado por Tim Berners-Lee (1991). Versión actual: HTML5.
  - Elementos: encabezados, párrafos, listas, imágenes, links, formularios, tablas, semántica.
  - Es la base de toda página web. Sin HTML, no hay web.
- **CSS (Cascading Style Sheets):**
  - Tampoco es un lenguaje de programación. Define la presentación visual del HTML.
  - Creado por Håkon Wium Lie (1996). Versión actual: CSS3.
  - Propiedades: colores, tipografía, espaciado, layouts (flexbox, grid), animaciones, responsive design.
  - Separación de responsabilidades: HTML estructura, CSS estilo.
- **JavaScript:**
  - Historia completa: creado por Brendan Eich en 10 días en Netscape (1995). Nombre original: Mocha, luego LiveScript, finalmente JavaScript (por marketing, no por relación con Java).
  - De lenguaje "de juguete" para validar formularios a pilar del desarrollo web moderno.
  - ECMAScript: el estándar que define JavaScript. ES6/ES2015 fue el punto de inflexión (arrow functions, classes, let/const, template literals, destructuring, modules, promises).
  - Evolución: ES2016, ES2017 (async/await), ES2018, ... hasta hoy. El lenguaje no para de evolucionar.
  - Dónde corre: navegador (frontend), servidor (Node.js), mobile (React Native), desktop (Electron).
  - El lenguaje más usado del mundo según Stack Overflow Survey año tras año.
- **TypeScript:**
  - Creado por Anders Hejlsberg (el mismo de C#) en Microsoft (2012).
  - JavaScript + tipado estático. Se compila (transpila) a JavaScript.
  - ¿Por qué existe? JavaScript no tiene tipos. En proyectos grandes, esto causa errores difíciles de encontrar. TypeScript los detecta antes de ejecutar.
  - Adopción masiva: Angular (obligatorio), React (recomendado), Node.js (muy común), la industria se está moviendo hacia TS.
  - Ventajas: autocompletado inteligente, detección de errores en tiempo de desarrollo, mejor documentación del código, refactoring más seguro.
  - Desventajas: curva de aprendizaje adicional, configuración del compilador, overhead de tipado.
- **Dart:**
  - Creado por Google (2011). Orientado a objetos, tipado fuerte.
  - Nicho principal: Flutter (desarrollo mobile multiplataforma).
  - Puede compilar a JavaScript, código nativo (ARM, x64) y a WebAssembly.
- **WebAssembly (Wasm):**
  - No es un lenguaje que se escriba directamente, sino un formato de compilación.
  - Permite ejecutar código escrito en C, C++, Rust, Go, etc. en el navegador a velocidad casi nativa.
  - El futuro de aplicaciones web de alto rendimiento: juegos, editores de video, modelado 3D.

### Actividad del módulo

1. Elaborar un **cuadro comparativo de JavaScript vs TypeScript** con las columnas: característica, JavaScript, TypeScript, ejemplo. Incluir al menos 8 características (tipado, compilación, compatibilidad, tooling, comunidad, curva de aprendizaje, etc.).
2. Investigar y responder en un breve informe (1-2 páginas):
   - ¿Por qué TypeScript se ha convertido en el estándar para proyectos grandes?
   - ¿Qué es ECMAScript y por qué ES6 fue tan importante para JavaScript?
   - ¿Qué relación tiene TypeScript con el stack de este training (React + Node.js)?

---

## Módulo 5: Frameworks y librerías — Backend

### Contenido

- **¿Qué es un framework vs una librería?**
  - **Framework:** estructura completa que dicta cómo organizar el código. "Tú escribes código dentro del framework." Inversión de control: el framework llama a tu código.
  - **Librería:** conjunto de funciones/utilidades que tú llamas cuando necesitas. "Tú llamas a la librería."
  - Analogía: el framework es la casa con la estructura ya puesta (tú decoras); la librería es una caja de herramientas (tú decides cuándo usar cada una).
- **Frameworks de backend por lenguaje:**
  - **C# / .NET:**
    - **ASP.NET Core:** framework principal para APIs y aplicaciones web en .NET. Minimal APIs (ligero, pocas líneas) y Controllers (estructura clásica MVC). Alto rendimiento, multiplataforma.
    - **Entity Framework Core:** ORM para acceso a bases de datos. Mapea clases C# a tablas SQL.
    - **Blazor:** construir interfaces web con C# en lugar de JavaScript.
  - **Java:**
    - **Spring Boot:** el framework dominante en Java empresarial. Microservicios, APIs REST, configuración automática.
    - **Quarkus:** framework nativo para cloud y contenedores. Arranque ultrarrápido.
    - **Micronaut:** alternativa ligera a Spring para microservicios.
  - **Node.js (JavaScript/TypeScript):**
    - **Express.js:** el framework más popular de Node.js. Minimalista, flexible, middleware.
    - **Fastify:** alternativa a Express enfocada en rendimiento. Sistema de plugins, validación con JSON Schema.
    - **NestJS:** framework con arquitectura opinionada inspirada en Angular. TypeScript nativo, DI, módulos.
  - **Python:**
    - **Django:** "batteries included". Admin panel, ORM, auth, todo incluido. Para proyectos grandes y rápidos.
    - **Flask:** microframework. Solo lo esencial, tú agregas lo que necesites. Para APIs ligeras y microservicios.
    - **FastAPI:** moderno, alto rendimiento, tipado, documentación automática. Para APIs con Python.
  - **Go:**
    - **Gin:** framework web minimalista y rápido. El más popular en Go.
    - **Echo:** similar a Gin, con más features integrados.
    - **Fiber:** inspirado en Express.js, fácil transición para desarrolladores Node.js.
  - **PHP:**
    - **Laravel:** el framework más popular de PHP. Eloquent ORM, Blade templates, Artisan CLI.
    - **Symfony:** framework empresarial, componentes reutilizables. Base de muchos proyectos PHP.
  - **Ruby:**
    - **Ruby on Rails:** "convention over configuration". Desarrollo rápido, generadores, ActiveRecord ORM.

### Actividad del módulo

1. Elaborar una **matriz de frameworks backend** organizada por lenguaje con las columnas: lenguaje, framework, año, tipo (fullstack/micro/API), enfoque principal, empresas que lo usan, nivel de popularidad (puede basarse en GitHub stars, encuestas de Stack Overflow, etc.).
2. Investigar: ¿Cuáles son las diferencias principales entre ASP.NET Core (Minimal API vs Controllers) y Fastify? ¿Por qué son estas las tecnologías elegidas para este training? Escribir al menos 3 razones para cada una.

---

## Módulo 6: Frameworks y librerías — Frontend y Mobile

### Contenido

- **Frameworks/librerías de frontend web:**
  - **React:**
    - Creado por Facebook/Meta (2013). Librería (no framework completo) para construir interfaces de usuario.
    - Concepto clave: componentes reutilizables, Virtual DOM, JSX (HTML dentro de JavaScript).
    - Ecosistema: React Router (navegación), Redux/RTK (estado global), MUI/Material UI (componentes visuales), Next.js (SSR/SSG).
    - El más popular y con mayor demanda laboral. El elegido en este training.
  - **Angular:**
    - Creado por Google (2016, reescritura de AngularJS). Framework completo y opinionado.
    - TypeScript obligatorio, módulos, servicios, inyección de dependencias, RxJS.
    - Ideal para aplicaciones empresariales grandes y complejas.
    - Curva de aprendizaje más pronunciada que React.
  - **Vue.js:**
    - Creado por Evan You (2014, ex-ingeniero de Google).
    - Balance entre la simplicidad de React y la estructura de Angular.
    - Single File Components (.vue), Composition API, Vuex/Pinia.
    - Popular en Asia y en proyectos medianos.
  - **Svelte:**
    - Creado por Rich Harris (2016). Enfoque radical: compila los componentes en JavaScript puro, sin Virtual DOM.
    - Extremadamente rápido y ligero. Sintaxis simple.
    - SvelteKit como framework fullstack.
    - Más nuevo, comunidad creciente.
- **Frameworks/librerías de desarrollo mobile:**
  - **React Native:**
    - Creado por Facebook/Meta (2015). Usa React para construir apps móviles nativas.
    - JavaScript/TypeScript. Un solo código para iOS y Android (con componentes nativos).
    - Empresas: Facebook, Instagram, Discord, Shopify.
  - **Flutter:**
    - Creado por Google (2017). Usa Dart. Motor de renderizado propio (Skia).
    - Un solo código para iOS, Android, web y desktop. Widgets propios (no usa componentes nativos del SO).
    - Empresas: Google, BMW, Alibaba, Nubank.
  - **.NET MAUI:**
    - Evolución de Xamarin por Microsoft. C# para apps multiplataforma (iOS, Android, Windows, macOS).
    - Integración con el ecosistema .NET. Ideal si el equipo ya trabaja con C#.
  - **Swift UI (Apple):**
    - Framework de Apple para iOS/macOS. Lenguaje: Swift. Solo plataformas Apple.
    - UI declarativa, previews en tiempo real, integración con ecosistema Apple.
  - **Jetpack Compose (Android):**
    - Framework moderno de Google para UI en Android. Lenguaje: Kotlin.
    - Reemplazo del sistema XML clásico. Declarativo, similar en concepto a SwiftUI.
- **¿Cómo elegir entre frameworks frontend?** Factores: tamaño del proyecto, curva de aprendizaje, ecosistema, demanda laboral, tipo de equipo, requisitos de rendimiento.

### Actividad del módulo

1. Elaborar una **matriz comparativa de frameworks frontend web** (React, Angular, Vue, Svelte) con las columnas: framework, año, creador, lenguaje base, enfoque (librería/framework), curva de aprendizaje, ecosistema, demanda laboral, tipo de proyecto ideal, ventajas y desventajas.
2. Elaborar una **matriz comparativa de frameworks mobile** (React Native, Flutter, .NET MAUI, SwiftUI, Jetpack Compose) con las columnas: framework, lenguaje, plataformas soportadas, enfoque (nativo/híbrido), rendimiento, y cuándo elegirlo.
3. Investigar en portales de empleo: buscar ofertas para desarrollador React, Angular y Vue en tu país. ¿Cuál tiene más demanda? ¿Qué otros requisitos piden junto con el framework?

---

## Módulo 7: Eligiendo el stack tecnológico adecuado

### Contenido

- **¿Qué es un stack tecnológico?** Combinación de lenguajes, frameworks, bases de datos y herramientas que se usan juntos para construir una aplicación.
- **Stacks populares:**
  - **LAMP:** Linux + Apache + MySQL + PHP. Clásico de la web. WordPress, Drupal.
  - **MEAN:** MongoDB + Express + Angular + Node.js. Full JavaScript.
  - **MERN:** MongoDB + Express + React + Node.js. Variante con React en vez de Angular.
  - **MEVN:** MongoDB + Express + Vue + Node.js. Variante con Vue.
  - **.NET Stack:** C# + ASP.NET Core + SQL Server/PostgreSQL + Entity Framework. Empresarial.
  - **JAMstack:** JavaScript + APIs + Markup. Sites estáticos modernos (Next.js, Gatsby, Astro).
  - **T3 Stack:** TypeScript + Next.js + tRPC + Tailwind + Prisma. Moderno, tipo-safe.
- **Factores para elegir un stack:**
  - **Tipo de proyecto:** startup rápida (prototipo) vs sistema empresarial a largo plazo.
  - **Equipo:** ¿con qué lenguajes tiene experiencia el equipo? ¿Se puede capacitar?
  - **Rendimiento:** ¿necesita alta concurrencia? ¿Tiempo real? ¿Procesamiento pesado?
  - **Escalabilidad:** ¿crecerá mucho? ¿Microservicios o monolito?
  - **Ecosistema:** ¿hay librerías, documentación, comunidad para resolver problemas?
  - **Demanda laboral:** ¿es fácil encontrar desarrolladores con ese stack?
  - **Costo:** ¿es open source? ¿Requiere licencias?
- **El stack de este training y por qué:**
  - **Backend opción 1 — C# .NET 10:** maduro, alto rendimiento, tipado fuerte, excelente tooling (Visual Studio 2026), muy demandado en el mercado empresarial latinoamericano, soporte de Microsoft, ecosistema completo (EF Core, ASP.NET, Azure).
  - **Backend opción 2 — Node.js + Fastify + TypeScript:** mismo lenguaje en frontend y backend (JavaScript/TypeScript), rendimiento superior a Express, ecosistema npm gigante, ideal para APIs y microservicios, demanda altísima globalmente.
  - **Frontend — React + TypeScript + MUI + RTK Query + React Router DOM:** React es el framework frontend más demandado, TypeScript aporta seguridad de tipos, MUI provee componentes profesionales, RTK Query simplifica el consumo de APIs, React Router DOM maneja la navegación.
  - **Base de datos — PostgreSQL:** open source, robusto, soporte de tipos avanzados (JSON, arrays), rendimiento, escalabilidad, estándar de la industria.
  - **IDEs — Visual Studio 2026 + VS Code:** VS 2026 para C# (debugging, tooling avanzado), VS Code para todo lo demás (Node.js, React, TypeScript, extensiones).

### Actividad del módulo

1. Para cada uno de los 3 escenarios siguientes, proponer un **stack tecnológico completo** (frontend, backend, base de datos, herramientas) y justificar cada elección en al menos 2 líneas:
   - **Escenario A:** una startup que necesita lanzar un MVP (producto mínimo viable) de una app de delivery de comida en 3 meses.
   - **Escenario B:** un banco que necesita migrar su sistema core de COBOL a tecnología moderna, con requisitos estrictos de seguridad y rendimiento.
   - **Escenario C:** un emprendedor individual que quiere crear un blog personal con capacidad de vender productos digitales.
2. Elaborar un **mapa conceptual** del stack de este training que muestre cómo se conectan todas las piezas: C# .NET 10, Node.js + Fastify, React, TypeScript, PostgreSQL, VS 2026, VS Code, Git/GitHub.

---

## Actividad final del Curso 3

**"Investigación a fondo de un lenguaje de programación"**

Desde la rama `curso-3/actividad-final`:

Elegir **un lenguaje de programación** (que no sea C# ni JavaScript/TypeScript, ya que esos se cubrirán en profundidad más adelante) y elaborar una investigación completa que incluya:

1. **Historia y origen:** quién lo creó, cuándo, en qué contexto, qué problema buscaba resolver.
2. **Evolución:** versiones clave, cambios importantes, estado actual.
3. **Paradigma(s):** qué paradigmas soporta y cómo.
4. **Sintaxis:** Hola Mundo + un ejemplo básico que muestre las características del lenguaje (variables, condicional, bucle, función).
5. **Frameworks principales:** listar al menos 3 frameworks con su nicho de uso.
6. **Nicho de aplicación:** en qué tipo de proyectos se usa, por qué se elige para esos proyectos.
7. **Empresas que lo usan:** al menos 5 empresas con una línea sobre cómo lo usan.
8. **Comunidad y ecosistema:** tamaño de la comunidad, gestor de paquetes, documentación, conferencias.
9. **Ventajas y desventajas:** al menos 4 de cada una.
10. **Comparación con un lenguaje similar:** elegir un competidor directo y comparar en al menos 5 aspectos (sintaxis, rendimiento, ecosistema, curva de aprendizaje, demanda laboral).

**Entregable:** Informe en Markdown (4-5 páginas) dentro del repositorio. Debe incluir fuentes de información. Commit con mensajes siguiendo convención y PR hacia develop.

**Criterios de evaluación:**
- Profundidad y precisión de la investigación.
- Cobertura de todos los puntos solicitados.
- Calidad de la comparación con el lenguaje competidor.
- Estructura, redacción y formato del documento.
- Correcto uso de Markdown y Git.
