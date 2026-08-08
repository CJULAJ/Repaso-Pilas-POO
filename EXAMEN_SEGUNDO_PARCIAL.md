# Examen parcial 2 — Programación 1 (Java)

**Nombre:**
**Carnet:**
**Unicamente para Serie 2**
**Carnet que finaliza en numero par, realizar ejercicios pares** 
**Carnet que finaliza en numero impar, realizar ejercicios impares** 

**Alcance:** contenido de Clase 7 y 8 (POO: clases, objetos, encapsulamiento, getters/setters), Clase 9 y 10 (herencia, `super`, sobreescritura) e introducción a **polimorfismo** (referencia de supertipo, enlace dinámico, uso puntual de `instanceof`).

**Nivel:** equivalente al primer parcial en exigencia (programación estructurada previa se asume dominada).

---

## Estructura del proyecto

Proyecto **Java estándar** (sin Maven ni Gradle): solo código fuente bajo `src/` respetando la jerarquía de paquetes.

| Ruta | Descripción |
|------|-------------|
| `src/edu/umg/programacion1/examen2/seriea/` | **Serie A** — diez archivos de preguntas teórico-prácticas. |
| `src/edu/umg/programacion1/examen2/serieb/` | **Serie B** — cuatro clases con `main` (un problema por archivo). |

Los estudiantes pueden trabajar en **IntelliJ**, **Eclipse**, **VS Code** (extensión Java) o editor + terminal; el paquete y los nombres de clase deben mantenerse para facilitar la calificación.

### Compilación y ejecución (terminal)

Desde la carpeta raíz del proyecto (`examen-segundo-parcial-java`), con **JDK 11 o superior** instalado:

```bash
mkdir -p bin
javac -encoding UTF-8 -d bin $(find src -name "*.java")
```

Ejecutar un `main` de la Serie B (ejemplo problema 1):

```bash
java -cp bin edu.umg.programacion1.examen2.serieb.Problema01ProductoMain
```

Sustituya el nombre completo de la clase según el problema (`Problema02HerenciaMain`, etc.).

En **Windows (PowerShell)** puede usar:

```powershell
mkdir bin -ea 0; javac -encoding UTF-8 -d bin (Get-ChildItem -Path src -Filter *.java -Recurse).FullName
java -cp bin edu.umg.programacion1.examen2.serieb.Problema01ProductoMain
```

La carpeta `bin/` (o `out/`) contiene los `.class` generados; suele añadirse al `.gitignore` si usa control de versiones.

---

## Serie A (10 puntos) — Teórico-práctico

**Formato:** en cada archivo `Pregunta0X....java` el estudiante **completa fragmentos de código** indicados con `TODO` y escribe una **explicación breve** en el bloque `CONCEPTO` (comentarios multilínea al final de la clase), salvo donde el enunciado en el propio archivo indique otro criterio.

**Criterio sugerido de calificación:** 0.5 punto por pregunta (total **5 puntos**), valorando:

- Corrección del código completado.
- Claridad y precisión del comentario conceptual (no se exige extensión; sí que demuestre comprensión).

| # | Archivo | Contenido principal |
|---|---------|------------------------|
| 1 | `Pregunta01Encapsulamiento.java` | `private`, validación en setter |
| 2 | `Pregunta02Constructores.java` | Constructores, `this(...)` |
| 3 | `Pregunta03GettersSetters.java` | Validación en setters |
| 4 | `Pregunta04HerenciaSuper.java` | `extends`, `super(...)` en constructor |
| 5 | `Pregunta05Override.java` | Sobreescritura y `@Override` |
| 6 | `Pregunta06Protected.java` | Acceso `protected` desde subclase |
| 7 | `Pregunta07Polimorfismo.java` | Referencia `Figura`, objeto `Rectangulo`; uso de `area()` |
| 8 | `Pregunta08SuperMetodo.java` | `super.metodo()` dentro de método sobreescrito |
| 9 | `Pregunta09Instanceof.java` | `instanceof` y conversión segura |
| 10 | `Pregunta10HerenciaSubclase.java` | Subclase, `super` en constructor, método con datos heredados |

**Nota para el docente:** En la pregunta 4 el constructor de `Vendedor` incluye valores de relleno (`"PENDIENTE"`, etc.) para que el proyecto compile antes del examen; el estudiante debe **reemplazarlos** por la lógica correcta según el enunciado en el Javadoc de la clase.

---

## Serie B (10 puntos) — Práctica

**Formato:** cada problema está descrito en el **Javadoc** de una clase con método `main`. El estudiante **implementa** la lógica (creando las clases auxiliares que necesite, normalmente en el mismo paquete `serieb`).

**Distribución sugerida:** **2,5 puntos** por problema × 4 = **10 puntos**.

| Problema | Clase principal | Ideas evaluadas |
|----------|-----------------|-----------------|
| 1 | `Problema01ProductoMain` | Encapsulamiento, `vender`, validaciones |
| 2 | `Problema02HerenciaMain` | `Empleado` / `Vendedor`, `super`, `resumen()` |
| 3 | `Problema03CuentaMain` | `Cuenta` / `CuentaAhorro`, `@Override`, reglas distintas |
| 4 | `Problema04PolimorfismoMain` | Jerarquía de figuras, arreglo/lista, recorrido polimórfico **sin** `instanceof` |

**Criterio sugerido:** diseño razonable de clases, compilación, demostración en `main` coherente con el enunciado, manejo de casos límite (stock insuficiente, montos inválidos, etc., según cada problema).

---

## Puntuación total sugerida

| Sección | Puntos |
|---------|--------|
| Serie A | 10 |
| Serie B | 10 |
| **Total** | **20** |

Si su reglamento académico usa otra escala (por ejemplo 15 puntos como el parcial 1), puede ponderar proporcionalmente (por ejemplo Serie A = 50 % y Serie B = 50 % del valor del parcial).

---

## Alineación con las clases

- **Clase 7–8:** preguntas 1–3 y problema B1; parte de validaciones y diseño de métodos en B2–B3.
- **Clase 9–10:** preguntas 4–6, 8, 10 y problemas B2–B3.
- **Polimorfismo (tema complementario):** preguntas 7 y 9; problema B4 (y reforzado en B3 si se enfatiza enlace dinámico).

---

## Entrega sugerida

- Carpeta del proyecto con el árbol `src/edu/...` (código fuente `.java` únicamente; opcionalmente excluir `bin/`).
- Breve **nota de prueba** opcional: cómo ejecutar cada `main` de la Serie B con `java -cp bin ...`.

---

*Documento generado como guía del examen; el docente puede ajustar plazos, ponderaciones y criterios de rubrica.*
