# codex-skills-library

Biblioteca reutilizable de Skills de Codex para convertir procedimientos de ingeniería en instrucciones que puedan copiarse entre proyectos, mantenerse juntas y versionarse más adelante.

Cada skill se centra en una actividad concreta y puede combinarse con otras cuando la tarea lo requiere. Las reglas propias de cada proyecto —stack, arquitectura, comandos y convenciones— permanecen en su `AGENTS.md`.

## Estado actual

- Disponibles: `debugging`, `planning`, `feature-design`, `architecture-review`, `backend-development`, `frontend-development`, `database-engineering`, `security-review`, `testing`, `code-review`, `refactoring` y `pre-commit-review`.
- Los tres archivos de `debugging` conservan exactamente el contenido desarrollado en la conversación «Aprender skills Codex», sin reescrituras ni adaptaciones.
- Esta entrega es una carpeta local lista para seguir creciendo. Todavía no se inicializó Git, no hay commits ni conexión con GitHub.
- Las skills actuales contienen únicamente instrucciones y referencias; no requieren scripts ni dependencias adicionales.

## Estructura

```text
codex-skills-library/
├── README.md
└── .agents/
    └── skills/
        ├── debugging/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── report-template.md
        ├── planning/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── plan-template.md
        ├── feature-design/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── feature-template.md
        ├── architecture-review/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── review-template.md
        ├── backend-development/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── report-template.md
        ├── frontend-development/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── report-template.md
        ├── database-engineering/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── report-template.md
        ├── security-review/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── report-template.md
        ├── testing/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── report-template.md
        ├── code-review/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── report-template.md
        ├── refactoring/
        │   ├── SKILL.md
        │   └── references/
        │       ├── methodology.md
        │       └── report-template.md
        └── pre-commit-review/
            ├── SKILL.md
            └── references/
                ├── methodology.md
                └── report-template.md
```

### Archivos de debugging

- [SKILL.md](.agents/skills/debugging/SKILL.md): identificación, criterios de uso, investigación basada en evidencia, corrección mínima, validación y condiciones de cierre.
- [methodology.md](.agents/skills/debugging/references/methodology.md): metodología detallada para causas poco evidentes, hipótesis alternativas y fallos entre componentes.
- [report-template.md](.agents/skills/debugging/references/report-template.md): formato de informe con síntoma, reproducción, causa, evidencia, corrección, regresión, validación y riesgos.

### Archivos de planning

- [SKILL.md](.agents/skills/planning/SKILL.md): planificación basada en el proyecto real, alcance, supuestos, dependencias, riesgos y criterios de cierre.
- [methodology.md](.agents/skills/planning/references/methodology.md): investigación acotada, secuenciación entre componentes, compatibilidad y validaciones observables.
- [plan-template.md](.agents/skills/planning/references/plan-template.md): guía adaptable para entregar un plan ejecutable sin secciones innecesarias.

`planning` ayuda a ordenar cambios antes de implementarlos. Si pedís solamente un plan, entrega el plan; si también autorizás la implementación, continúa con el trabajo autorizado. Las preguntas se reservan para decisiones relevantes que no puedan resolverse con el contexto disponible.

### Archivos de feature-design

- [SKILL.md](.agents/skills/feature-design/SKILL.md): definición de alcance, reglas de negocio, flujos, estados relevantes y criterios de aceptación verificables.
- [methodology.md](.agents/skills/feature-design/references/methodology.md): decisiones de producto, actores y permisos, transiciones, operaciones concurrentes y efectos externos cuando correspondan.
- [feature-template.md](.agents/skills/feature-design/references/feature-template.md): guía adaptable para entregar una especificación funcional con evidencia, supuestos y decisiones pendientes.

`feature-design` define qué debe hacer una funcionalidad; `planning` ordena cómo implementarla. Se pueden usar juntas, pero cada una funciona de manera independiente. Las reglas de negocio no definidas se señalan como decisiones pendientes.

### Archivos de architecture-review

- [SKILL.md](.agents/skills/architecture-review/SKILL.md): revisión de responsabilidades, dependencias, acoplamiento, propiedad de datos y contratos con hallazgos basados en evidencia.
- [methodology.md](.agents/skills/architecture-review/references/methodology.md): análisis de límites, consistencia, despliegue y alternativas según las necesidades reales del proyecto.
- [review-template.md](.agents/skills/architecture-review/references/review-template.md): informe adaptable con evidencia, impacto, recomendaciones, alternativas y limitaciones.

`architecture-review` evalúa si la estructura sirve al comportamiento requerido. Puede revisar una arquitectura existente, un diseño propuesto o un cambio entre componentes. Cada hallazgo debe explicar una consecuencia concreta; conservar la arquitectura actual también es una conclusión válida.

### Archivos de backend-development

- [SKILL.md](.agents/skills/backend-development/SKILL.md): implementación de APIs, servicios, trabajos en segundo plano e integraciones con contratos, validación, permisos y verificación.
- [methodology.md](.agents/skills/backend-development/references/methodology.md): persistencia, concurrencia, efectos externos, entrega de eventos, pruebas y orientación específica para proyectos Node.js/Express.
- [report-template.md](.agents/skills/backend-development/references/report-template.md): informe adaptable del comportamiento entregado, cambios de contrato, validaciones y limitaciones.

`backend-development` implementa el comportamiento requerido en el stack existente. Revisa las reglas y los permisos en el servidor, conserva contratos y verifica los efectos sobre datos e integraciones cuando correspondan. No exige una arquitectura ni un framework particular.

### Archivos de frontend-development

- [SKILL.md](.agents/skills/frontend-development/SKILL.md): implementación de interfaces, componentes, formularios y navegación con estado, accesibilidad, diseño responsive e integración de APIs.
- [methodology.md](.agents/skills/frontend-development/references/methodology.md): propiedad del estado, datos asíncronos, recuperación de formularios, orientación para React y verificación en navegador.
- [report-template.md](.agents/skills/frontend-development/references/report-template.md): informe adaptable del comportamiento visible, cambios intencionales, validaciones y limitaciones.

`frontend-development` sigue el stack y el sistema visual del proyecto. Verifica lo que el usuario puede ver y hacer, distingue datos simulados de integración real y contempla errores, carga y recuperación cuando afectan el flujo. No exige React ni una librería de componentes particular.

### Archivos de database-engineering

- [SKILL.md](.agents/skills/database-engineering/SKILL.md): diseño, implementación y revisión de modelos, restricciones, consultas, índices, migraciones y transformaciones de datos.
- [methodology.md](.agents/skills/database-engineering/references/methodology.md): integridad, concurrencia, compatibilidad, backfills, rendimiento medido y permisos, con orientación para PostgreSQL, MySQL y Supabase cuando corresponda.
- [report-template.md](.agents/skills/database-engineering/references/report-template.md): informe adaptable de cambios, evidencia, validaciones, estado de aplicación y recuperación.

`database-engineering` sigue el motor y las herramientas reales del proyecto. Distingue cambios preparados de cambios aplicados, verifica datos existentes y conserva las reglas de integridad y acceso. Una mejora de rendimiento necesita evidencia; escribir una migración no autoriza ejecutarla en una base de producción.

### Archivos de security-review

- [SKILL.md](.agents/skills/security-review/SKILL.md): revisión de seguridad con alcance definido, trazabilidad de fallos, evidencia, impacto y recomendaciones concretas.
- [methodology.md](.agents/skills/security-review/references/methodology.md): permisos, sesiones, entradas no confiables, navegador, archivos, secretos, dependencias y calibración de severidad según la superficie revisada.
- [report-template.md](.agents/skills/security-review/references/report-template.md): informe adaptable con hallazgos priorizados, confianza, verificaciones, estado de corrección y limitaciones.

`security-review` distingue defectos demostrados, riesgos condicionados y mejoras opcionales. Prioriza el impacto real y evita exponer secretos o ampliar pruebas fuera del alcance autorizado. Una revisión sin hallazgos se limita a lo inspeccionado; no certifica la seguridad de todo el sistema.

### Archivos de testing

- [SKILL.md](.agents/skills/testing/SKILL.md): diseño, implementación y ejecución de pruebas enfocadas en criterios de aceptación, invariantes y regresiones.
- [methodology.md](.agents/skills/testing/references/methodology.md): selección de niveles, mocks, fixtures, regresiones, asincronía, pruebas intermitentes y evidencia de cobertura.
- [report-template.md](.agents/skills/testing/references/report-template.md): informe adaptable de comportamientos cubiertos, cambios, ejecución real, resultados y limitaciones.

`testing` elige el nivel de prueba según el fallo que debe detectar. Evita simular la interacción que necesita verificar, distingue pruebas escritas de pruebas ejecutadas y comprueba que la selección realmente haya corrido. Un reintento exitoso no oculta un fallo anterior ni demuestra estabilidad.

### Archivos de code-review

- [SKILL.md](.agents/skills/code-review/SKILL.md): revisión de cambios con foco en bugs, seguridad, regresiones y compatibilidad de contratos.
- [methodology.md](.agents/skills/code-review/references/methodology.md): alcance del diff, trazabilidad de fallos, atribución de regresiones, evidencia y priorización de hallazgos.
- [report-template.md](.agents/skills/code-review/references/report-template.md): informe adaptable con hallazgos accionables, ubicaciones verificadas, preguntas abiertas y validaciones ejecutadas.

`code-review` sigue el cambio hasta sus consumidores y distingue problemas nuevos de contexto preexistente. Cada hallazgo necesita una condición alcanzable y una consecuencia concreta. Evita preferencias de estilo sin impacto y conserva la implementación cuando el pedido es solamente revisar.

### Archivos de refactoring

- [SKILL.md](.agents/skills/refactoring/SKILL.md): mejoras de estructura con alcance definido, contratos explícitos y transformaciones pequeñas verificables.
- [methodology.md](.agents/skills/refactoring/references/methodology.md): caracterización del comportamiento, extracción, consolidación, cambios compartidos y preservación de efectos, orden y estado.
- [report-template.md](.agents/skills/refactoring/references/report-template.md): informe adaptable de la mejora, cambios intencionales, contratos preservados, validaciones y limitaciones.

`refactoring` busca una mejora estructural concreta y protege el comportamiento relevante antes y después del cambio. Distingue reorganización de correcciones funcionales, conserva el trabajo existente y evita abstraer o rediseñar áreas ajenas al pedido.

### Archivos de pre-commit-review

- [SKILL.md](.agents/skills/pre-commit-review/SKILL.md): revisión del contenido propuesto para un commit, alcance, archivos accidentales y validaciones pertinentes.
- [methodology.md](.agents/skills/pre-commit-review/references/methodology.md): diferencias entre el índice y los archivos locales, preparación parcial, evidencia de ejecución y vigencia de los resultados.
- [report-template.md](.agents/skills/pre-commit-review/references/report-template.md): informe adaptable con candidato revisado, bloqueos, validaciones, limitaciones y siguiente acción.

`pre-commit-review` distingue lo preparado para commit de los cambios locales que quedan fuera. No confunde pruebas sobre archivos locales con pruebas del candidato exacto, y una revisión favorable no autoriza preparar archivos, crear commits ni publicar cambios.

## Convenciones de la biblioteca

1. Guardar cada skill en `.agents/skills/<nombre>/`, con nombres en minúsculas y guiones, como `security-review`.
2. Incluir un `SKILL.md` con frontmatter YAML que defina `name` y `description`. El nombre debe coincidir con la carpeta; la descripción explica qué hace y cuándo corresponde usarla.
3. Mantener las instrucciones principales en `SKILL.md` y el material detallado en `references/`. Indicar cuándo consultar cada referencia.
4. Agregar `scripts/` o `assets/` solo si la skill realmente los necesita. No crear carpetas vacías para las skills previstas.
5. Mantener las skills independientes de rutas locales, credenciales y reglas particulares de un proyecto.
6. Al incorporar o modificar una skill, revisar sus referencias, probarla en una tarea representativa y actualizar su estado en este README.
7. Copiar siempre la carpeta completa de una skill para conservar sus referencias y recursos.

Estas convenciones se aplican a las próximas incorporaciones. La versión inicial de `debugging` se conserva tal como fue redactada en la conversación de origen.

## Instalar una skill en un proyecto

Copiá `.agents/skills/debugging/` de esta biblioteca dentro de `.agents/skills/` en la raíz del proyecto de destino.

El resultado debe quedar así:

```text
mi-proyecto/
├── AGENTS.md
└── .agents/
    └── skills/
        └── debugging/
            ├── SKILL.md
            └── references/
                ├── methodology.md
                └── report-template.md
```

### Ejemplo con PowerShell

Ejecutá este ejemplo desde la raíz de `codex-skills-library`, reemplazando la ruta del proyecto:

```powershell
$projectPath = 'C:\ruta\a\mi-proyecto'
$skillsPath = Join-Path $projectPath '.agents\skills'
$destinationPath = Join-Path $skillsPath 'debugging'

if (Test-Path -LiteralPath $destinationPath) {
    throw 'Ya existe debugging en el proyecto. Revisá esa versión antes de reemplazarla.'
}

New-Item -ItemType Directory -Path $skillsPath -Force | Out-Null
Copy-Item -LiteralPath '.agents\skills\debugging' -Destination $skillsPath -Recurse
```

Para instalar otra skill, sustituí `debugging` por su nombre y copiá también todos sus recursos. Las copias son independientes: los cambios en esta biblioteca no actualizan automáticamente los proyectos.

### Usarla en Codex

Abrí el proyecto de destino en Codex. Podés invocarla explícitamente:

```text
$debugging
Investiga y corrige este error. Reproduce el fallo, identifica la causa y valida la solución.
[Agrega aquí el síntoma, el error o los pasos para reproducirlo.]
```

Codex también puede seleccionarla cuando la tarea coincide con su descripción. Si la skill recién copiada no aparece, reiniciá Codex.

Después de copiar también `planning` al proyecto, podés pedir un plan:

```text
$planning
Prepara un plan para agregar exportación CSV al listado de ventas.
Revisa el proyecto e identifica alcance, dependencias, riesgos y validaciones.
Por ahora entrega solamente el plan.
```

Para planificar e implementar en la misma tarea, indicá ambas acciones en el pedido.

Después de copiar también `feature-design` al proyecto, podés definir una funcionalidad:

```text
$feature-design
Define la funcionalidad para cancelar reservas en este proyecto.
Revisa el comportamiento actual y especifica actores, reglas, estados y criterios de aceptación.
Señala las decisiones de negocio que falten. Por ahora entrega solamente el diseño funcional.
```

Después de copiar también `architecture-review` al proyecto, podés revisar una decisión estructural:

```text
$architecture-review
Revisa la arquitectura del flujo de reservas y sus límites entre interfaz, reglas de negocio y persistencia.
Prioriza problemas con evidencia e impacto concreto y compara alternativas cuando corresponda.
Por ahora entrega solamente la revisión, sin modificar la implementación.
```

Después de copiar también `backend-development` al proyecto, podés implementar una funcionalidad de servidor:

```text
$backend-development
Implementa el endpoint de cancelación de reservas según la especificación del proyecto.
Revisa contratos, permisos, reglas de negocio y persistencia antes de modificar código.
Agrega o actualiza las pruebas pertinentes y reporta las validaciones ejecutadas y sus resultados.
```

Después de copiar también `frontend-development` al proyecto, podés implementar una interacción de interfaz:

```text
$frontend-development
Implementa la cancelación de reservas en la interfaz según la especificación y el contrato de API existentes.
Reutiliza los componentes del proyecto y contempla carga, errores, feedback y accesibilidad.
Verifica las interacciones y el comportamiento responsive disponibles y reporta qué quedó sin comprobar.
```

Después de copiar también `database-engineering` al proyecto, podés trabajar sobre una restricción de datos:

```text
$database-engineering
Implementa la regla de unicidad definida en la especificación para los identificadores externos de reservas.
Revisa el esquema, las migraciones, los datos disponibles y los consumidores afectados.
Prepara los cambios y verifícalos en un entorno de pruebas autorizado; reporta conflictos y comprobaciones pendientes.
No ejecutes cambios en producción.
```

Después de copiar también `security-review` al proyecto, podés revisar un flujo sensible:

```text
$security-review
Revisa la autorización y la exposición de datos del flujo de reservas y de los cambios recientes.
Prioriza hallazgos con evidencia, impacto y condiciones de explotación, y propone correcciones y pruebas de regresión.
Por ahora revisa el código y las pruebas locales pertinentes, sin modificar la implementación ni probar servicios en producción.
```

Después de copiar también `testing` al proyecto, podés proteger un comportamiento con pruebas:

```text
$testing
Agrega o actualiza las pruebas de cancelación de reservas según las reglas y permisos definidos en el proyecto.
Elige los niveles necesarios para verificar resultados y efectos sobre los datos, sin simular la restricción que se quiere comprobar.
Ejecuta las pruebas pertinentes en el entorno de pruebas autorizado y reporta resultados, casos omitidos y limitaciones.
```

Después de copiar también `code-review` al proyecto, podés revisar cambios locales:

```text
$code-review
Revisa los cambios locales de cancelación de reservas, tanto staged como unstaged, y los archivos nuevos pertinentes.
Prioriza bugs, seguridad, regresiones y contratos; comprueba el contexto y los consumidores afectados.
Entrega hallazgos con evidencia, impacto y ubicaciones verificadas. Por ahora no modifiques la implementación.
```

Después de copiar también `refactoring` al proyecto, podés reorganizar una responsabilidad concreta:

```text
$refactoring
Extrae la regla de elegibilidad para cancelar reservas del controlador hacia el componente de dominio que corresponda al proyecto.
Conserva contratos, permisos, resultados y errores existentes, y revisa los consumidores afectados.
Protege el comportamiento con las pruebas pertinentes y avanza en pasos pequeños, sin incluir correcciones funcionales ajenas al pedido.
```

Después de copiar también `pre-commit-review` al proyecto, podés revisar un commit propuesto:

```text
$pre-commit-review
Revisa lo preparado para el próximo commit del flujo de cancelación de reservas.
Distingue los cambios staged de los unstaged y los archivos nuevos que no estén incluidos.
Comprueba alcance, archivos accidentales y validaciones pertinentes, indicando qué contenido verificó cada comprobación.
Entrega bloqueos y limitaciones; no modifiques archivos, no prepares cambios ni crees el commit.
```

Referencia oficial sobre estructura, descubrimiento e invocación: [Build skills — OpenAI](https://learn.chatgpt.com/docs/build-skills).

## Roadmap

El conjunto inicial está redactado: `debugging` y las once skills del roadmap. La estructura y las referencias locales están comprobadas; queda evaluar su comportamiento en tareas representativas de proyectos reales antes de considerarlas probadas en uso.

| Skill | Propósito | Estado |
| --- | --- | --- |
| `planning` | Convertir tareas grandes en planes con alcance, dependencias, riesgos y validaciones. | Disponible |
| `feature-design` | Definir requisitos, reglas de negocio, casos de uso y criterios de aceptación. | Disponible |
| `architecture-review` | Revisar responsabilidades, dependencias, acoplamiento y límites de dominio. | Disponible |
| `backend-development` | Implementar servicios y APIs con contratos, validaciones y manejo de errores. | Disponible |
| `frontend-development` | Implementar interfaces, componentes, estado, accesibilidad y comportamiento responsive. | Disponible |
| `database-engineering` | Diseñar y revisar modelos, consultas, restricciones, índices y migraciones. | Disponible |
| `security-review` | Revisar vulnerabilidades y controles de seguridad con evidencia y severidad. | Disponible |
| `testing` | Definir y ejecutar pruebas unitarias, de integración, E2E y de regresión. | Disponible |
| `code-review` | Revisar cambios priorizando bugs, seguridad, regresiones y contratos. | Disponible |
| `refactoring` | Mejorar estructura interna preservando el comportamiento observable. | Disponible |
| `pre-commit-review` | Revisar validaciones, alcance y cambios antes de un commit autorizado. | Disponible |

## Versionado posterior

Cuando decidamos versionar la biblioteca, la raíz de Git será esta carpeta `codex-skills-library/`. Se incluirán `README.md` y `.agents/skills/`, conservando las referencias junto a cada skill.

La publicación en GitHub y la instalación en proyectos concretos se realizarán en una etapa posterior.

