# Diagnóstico de agilidad organizativa
## Transformación digital del reclutamiento de Hapag-Lloyd Chile — base para el *Recruitment Agility Pilot*

**Estado:** borrador para revisión del equipo (paso 4 de la sección 11 de `CLAUDE.md`). No incluye storyboard ni diseño de diapositivas.

**Convención de etiquetas**

- **[Hecho]**: dato o situación documentada en el repositorio (se indica la fuente).
- **[Propuesta]**: recomendación del equipo consultor.
- **[Supuesto / por validar]**: inferencia razonable que debe confirmarse con Hapag-Lloyd Chile antes de presentarla como hecho.

**Abreviaturas de fuentes**

| Código | Documento |
|---|---|
| TFM | *Segunda Entrega TD del Reclutamiento en Hapag Lloyd Chile _v2.docx* (proyecto final del Máster) |
| TFM-A1 / A4 | Anexo 1 (cuestionario a RR. HH.) / Anexo 4 (tabla AS-IS y observaciones del levantamiento) del TFM |
| BPMN | *Flujo Reclutamiento.pdf* (diagrama BPMN del proceso) |
| S4 / S5 | *EADA_ Sesión 4 Agilidad Organizativa* / *Sesión 5* (diapositivas del curso) |
| McK | De Smet (2018), *The agile manager*, McKinsey (lectura 75924) |
| PS | Le-Brun (2020), *Creating Psychological Safety*, AWS (lectura 75981) |
| HRA-R | HR Agile (2020), *Perfil de comportamiento frente a la agilidad* — Rogers (lectura 76620) |
| HRA-C | HR Agile (2020), *Conversaciones significativas con managers* (lectura 76622) |
| REP | Repenning, Kieffer y Repenning, *Un nuevo enfoque en el diseño de los procesos de trabajo*, HDBR (lectura 78841) |
| WD | Workday (2021), *Agilidad organizacional: roadmap para la aceleración digital* (lectura 78850) |
| ETBO | Nota técnica ETBO® (86403) |
| MM | *Moving Motivators*, Management 3.0 (75930) |

---

## 1. Síntesis ejecutiva

1. **La brecha principal no es tecnológica.** Hapag-Lloyd Chile ya tiene MyPort como núcleo del proceso: registra el 100 % de los procesos internos y entre el 70 % y el 80 % de los externos. Desde octubre de 2025 MyPort permite además que el líder revise candidatos [Hecho, TFM-A4 obs. 7 y 16]. Aun así, los CV y las entrevistas siguen viajando por correo, la reportería se alimenta a mano y la reclutadora ejecuta pasos que corresponden al líder [Hecho, TFM-A4 obs. 7, 10 y 13]. Esto coincide con la lectura de Workday: el 56 % de las empresas dice que su tecnología está alineada con la transformación, pero solo el 16 % dice lo mismo de su cultura [WD].

2. **El principal freno del tiempo de cobertura está fuera de RR. HH.** Según RR. HH., la principal causa de demora es la agenda del líder solicitante y el tiempo que tarda en decidir [Hecho, TFM-A1; TFM §6.1]. No se puede bajar de 38 a 28 días optimizando solo el trabajo de selección. Hay que cambiar las responsabilidades, la visibilidad y los acuerdos de decisión.

3. **El trabajo es invisible.** No hay indicadores consolidados de extremo a extremo ni tiempos por etapa [Hecho, TFM Tabla 16]. El seguimiento se hace "con correos y llamadas" [Hecho, BPMN] y "la encargada de reclutamiento realiza todo ese trabajo" [Hecho, TFM-A1]. Sin visibilidad del flujo no se puede saber dónde se pierden los días.

4. **Hay un cuello de botella estructural en las personas.** La operación depende de una sola reclutadora, con apoyo de una psicóloga interna [Hecho, TFM §6.1; TFM-A4 obs. 3], en un proceso que atraviesa 11 carriles de actores [Hecho, BPMN]. Por eso el piloto debe **liberar capacidad antes de exigirla** [coincide con TFM §2.4 "reto de capacidad"].

5. **Punto de partida: características de una etapa inicial de adopción ágil.** En este proceso todavía no se trabaja con prácticas ágiles (visualización del flujo, ciclos cortos de mejora, retrospectivas). Un piloto de 8 a 12 semanas permitirá desarrollar capacidades iniciales de foco, trabajo en equipo, visibilidad y aprendizaje. No debe aspirar a transformar la estructura organizativa [Propuesta]. El *Agile Fluency Model* (S4) se usa solo como referencia secundaria, sin clasificar formalmente el proceso en una de sus zonas.

6. **Recomendación central [Propuesta].** Lanzar un *Recruitment Agility Pilot* acotado a una familia de cargos, con:
   - un equipo multidisciplinario con dueño de extremo a extremo;
   - Kanban para hacer visible el flujo y Scrumban para mejorarlo en ciclos de dos semanas;
   - ADKAR aplicado a los líderes solicitantes;
   - un acuerdo explícito de tiempos de decisión entre líderes y RR. HH.
   
   Se escala solo lo que demuestre resultados.

---

## 2. Lectura del sistema actual (evidencia del flujo)

### 2.1 Qué muestra el proceso real

| Observación | Evidencia | Lectura ágil |
|---|---|---|
| 11 carriles de actores: candidato, plataforma de evaluación, psicóloga, HR Chile, HR OD, especialista RR. HH., Compensaciones, coordinación senior RR. HH., colaborador, Area Manager y nivel L1 | [Hecho, BPMN; TFM Anexo 2] | Muchos traspasos y ningún dueño visible de extremo a extremo |
| Un candidato externo puede pasar por hasta cinco instancias de entrevista: especialista, HR Chile o HR OD según ámbito, psicóloga, Area Manager y L1 | [Hecho, BPMN] | Cada instancia añade una espera de agenda. La vigencia del rol L1 está pendiente de confirmar [TFM §6.2] |
| Cuatro registros manuales en base de datos (candidatos, estado de entrevista, estado de oferta, guardado) y carga manual a QlikView | [Hecho, BPMN; TFM-A4 obs. 13] | Trabajo duplicado que no aporta valor al cliente |
| Coordinación de entrevistas por correos sucesivos; CV y entrevistas enviados al líder por correo aunque MyPort ya lo permite | [Hecho, TFM-A4 obs. 7; TFM §6.1] | La funcionalidad existe; lo que falta es adopción |
| Pruebas de Evaluar.com enviadas por correo o **WhatsApp personal**, sin plazo definido y con resultados que no se integran | [Hecho, TFM-A4 P020 y obs. 9; TFM Tabla 36] | Canal fuera del modelo, sin trazabilidad ni protección de datos |
| Ventana de recepción de CV de 1 a 2 semanas (internos) y de 1 a 3 semanas (externos) | [Hecho, TFM-A4 P013–P014] | **Hipótesis [por validar]:** parte relevante de los 38 días podría depender de una *política* y no de la tecnología |
| Candidatos descartados sin aviso hasta el cierre del proceso | [Hecho, TFM-A4 P021, P027 y P033] | Afecta a la experiencia y a la marca empleadora; posible *quick win* |
| Ponderación por Excel solo en procesos internos; sin ponderación en externos | [Hecho, TFM-A4 P007–P008] | El líder decide con información no comparable [TFM §6.1] |
| Ya se capacitó a todos los managers en MyPort; "la siguiente etapa es el acompañamiento" | [Hecho, TFM-A4 obs. 14] | Se trabajó el *Knowledge*, pero falta la *Ability* y el *Reinforcement* (ADKAR) |
| RR. HH. describe el proceso en "tres etapas" y dice "no tener certeza" de que existan tareas repetitivas, pero también identifica como manuales el agendamiento y la selección de CV | [Hecho, TFM-A1] | La percepción del desperdicio es limitada. Antes de pedir *Desire* hay que trabajar el *Awareness* |

### 2.2 Interpretación con Repenning (diseño dinámico del trabajo)

El proceso combina dos tipos de trabajo [REP]:

- **Trabajo de "fábrica"** (bien definido): publicar, registrar, enviar pruebas, comunicar estados. Debería fluir sin coordinación manual.
- **Trabajo de "estudio"** (ambiguo, requiere colaboración): definir el perfil y los criterios, y decidir entre candidatos.

Hoy el trabajo ambiguo se resuelve **en secuencia y por correo**. Repenning llama a esto **iteración inefectiva**: idas y vueltas lentas, porque la ambigüedad se traslada de mano en mano por escrito. El caso *RefineCo* de la lectura es casi idéntico:

- solicitudes incompletas que generaban cadenas de correos;
- un equipo saturado "haciendo de bombero".

RefineCo lo resolvió con tres medidas:

1. una **lista de verificación de entrada** (la solicitud se devuelve si está incompleta);
2. un **desencadenante** que separa los casos rutinarios de los complejos;
3. un **bloque diario de trabajo colaborativo** para los casos complejos.

Esta lógica se puede trasladar directamente a la requisición y a la agenda del líder [Propuesta].

---

## 3. Diagnóstico por dimensión

Las cinco dimensiones siguen el marco de la sesión 4 (Estrategia, Estructura, Personas, Procesos y Tecnología). Cada dimensión cierra con una barrera, un cambio, un concepto, una acción y un indicador principales. Las acciones son habilitadores; los indicadores miden el cambio observable.

### 3.1 Estrategia — propósito, outcomes y alineamiento con valor

| Elemento | Contenido |
|---|---|
| **Situación actual** | Hay una estrategia digital corporativa explícita (*Strategy 2030*), y el pilar *Undisputed Number One for Quality* se gestiona con compromisos verificables (*Quality Promises*) [Hecho, TFM §1.5]. El proyecto de reclutamiento tiene objetivos claros: pasar de 38 a 28 días y registrar el 100 % de los procesos de extremo a extremo [Hecho, TFM §6.1]. Sin embargo, la única métrica que hoy usa RR. HH. es el Coeficiente de Adecuación al Puesto (CAP), una medida de ajuste del candidato y no del flujo [Hecho, TFM-A1], y "no existe un indicador establecido sobre la búsqueda del candidato" [Hecho, TFM-A4 obs. 6]. El foco inicial del proyecto era "IA para evaluar redes sociales", algo que hoy está excluido [Hecho, TFM-A1 §3]. El patrocinio corporativo existe, pero no consta un sponsor ejecutivo nominal: solo que "el presupuesto provendría de RR. HH." [Hecho, TFM-A1 §2]. |
| **Barrera** | El objetivo se vive como **proyecto tecnológico de RR. HH.**, aunque el resultado (los 28 días) depende de los líderes solicitantes. No hay línea base por etapa que permita formular hipótesis. Existe el riesgo de medir el éxito por *outputs* (herramienta implantada, capacitación realizada) en lugar de *outcomes*. |
| **Cambio requerido** | **De** "implantar tecnología en reclutamiento" **a** "un servicio de reclutamiento compartido entre RR. HH. y líderes, con outcomes comunes y verificables". |
| **Concepto del curso** | Principio n.º 1 de los *10 principles of workforce transformation*: **centrarse en los outcomes** [S4]. *Performance management* basado en outcomes [S4, Procesos]. Kotter: visión compartida y sentido de urgencia [S4]. Planificación continua y métricas ágiles [WD]. |
| **Acción concreta** [Propuesta] | Taller de alineamiento de medio día con el sponsor, el *Product Owner* y dos líderes *early adopters* para acordar: (a) el propósito del piloto; (b) tres o cuatro outcomes con línea base; (c) los criterios para continuar, ajustar o detener. Puede anclarse en la cultura de *Quality Promises* que ya existe, como una "promesa de servicio" del reclutamiento. Esta es una adaptación local, no la copia de un modelo externo. |
| **Indicador** | **Tiempo total de cobertura** de los procesos del piloto frente a la línea base de 38 días. Como indicador de proceso, el porcentaje de outcomes del piloto que tienen línea base medida al cierre del primer ciclo. |

**Urgencia legítima disponible (Kotter) [Hecho, TFM]:**

- la integración de ZIM, en la que el talento es un activo declarado de la operación;
- la vigencia de la Ley 21.719 prevista para el 1 de diciembre de 2026 (el TFM pide verificar la fecha al implementar);
- la presión sobre costos laborales.

### 3.2 Estructura — equipo, responsabilidades y toma de decisiones

| Elemento | Contenido |
|---|---|
| **Situación actual** | La estructura es matricial. El Área Chile y la Oficina Regional LATAM conviven, y hay directores que reportan funcionalmente a la casa matriz [Hecho, TFM §1.4]. RR. HH. replica esa lógica dual (unidad regional OD y Compensaciones, más un área Chile reducida) [Hecho, TFM §1.4]. El reclutamiento recae en **una sola persona** [Hecho, TFM-A4 obs. 3]. La reclutadora ejecuta pasos del líder [Hecho, TFM-A4 obs. 10]. Las decisiones sobre plataformas e IA corresponden a la casa matriz [Hecho, TFM §1.4 y §1.5]. Los traspasos a Compensaciones e IT se hacen por Outlook [Hecho, TFM-A4 P032, obs. 12]. |
| **Barrera** | **Nadie es dueño del proceso de extremo a extremo** y los **derechos de decisión son implícitos**: no está acordado quién decide qué ni en qué plazo. Sin acuerdo de plazos, la demora del líder es invisible y no se puede gestionar. RR. HH. compensa absorbiendo tareas ajenas, lo que McKinsey describe como crear "funciones sombra" [McK]. |
| **Cambio requerido** | **De** una cadena de traspasos entre áreas **a** un equipo multidisciplinario con un dueño de extremo a extremo (*Product Owner*) y acuerdos explícitos de decisión. RR. HH. pasa a ser asesor y facilitador; el líder pasa a ser dueño de su decisión. |
| **Concepto del curso** | Estructura según la sesión 4: roles y responsabilidades, gobernanza y toma de decisiones, simplificar y aplanar [S4]. **Responsabilidad end to end** y equipos pequeños multidisciplinarios [McK]. Toma de decisiones **justificada y delegada** [WD]. **Cadena de ayuda**: saber a quién llamar cuando hay un problema [REP]. *Nota:* no se propone adoptar tribus ni *chapters*. De McKinsey se toma solo el principio de responsabilidad de extremo a extremo y el de liderar sin microgestionar (regla de `CLAUDE.md`). |
| **Acción concreta** [Propuesta] | Definir para el piloto: (a) los roles (sponsor, PO, facilitador y equipo); (b) una **matriz de decisiones** con tres niveles: lo que decide el equipo, lo que se consulta y lo que se escala a casa matriz; (c) un **acuerdo de servicio entre el líder y RR. HH.** con plazos para revisar candidatos y para decidir (*meta por acordar*); (d) un mapa de la cadena de ayuda para desbloquear procesos. |
| **Indicador** | **Tiempo de decisión del líder por etapa** (línea base por medir). Como complemento, el número de tareas del líder ejecutadas por RR. HH. en cada proceso (cumplimiento de responsabilidades por rol). |

### 3.3 Personas — competencias, empoderamiento, colaboración y seguridad psicológica

| Elemento | Contenido |
|---|---|
| **Situación actual** | Los managers perciben MyPort como complejo y poco intuitivo. Ya recibieron capacitación y "la siguiente etapa es el acompañamiento" [Hecho, TFM-A4 obs. 8 y 14]. Los líderes tardan en decidir y en gestionar su agenda de entrevistas [Hecho, TFM-A1]. El conocimiento del estado de cada proceso "reside más en las personas que en el sistema" [Hecho, TFM §6.1]. La jornada laboral se reduce a 42 horas, con menos holgura justo durante la implementación [Hecho, TFM DAFO A4]. Los valores corporativos son *We Care, We Move, We Deliver* [Hecho, TFM §1.4]. No hay evidencia documentada sobre el clima ni sobre la seguridad psicológica del equipo [Por validar]. |
| **Barrera** | La **adopción individual está incompleta**: hubo *Knowledge* (capacitación), pero falta *Ability* (uso real) y *Reinforcement* (nadie mide ni reconoce el cambio). Hacer visibles las demoras del líder puede **vivirse como exposición o culpa** si no existe seguridad psicológica. En ese caso, los líderes ocultarán bloqueos en lugar de mostrarlos [PS]. Los managers pueden percibir el autoservicio como trabajo extra y pérdida de estatus [HRA-C]. |
| **Cambio requerido** | **De** "RR. HH. lo hace por el líder" **a** "un líder autónomo acompañado por RR. HH.". **De** ocultar retrasos **a** mostrar bloqueos sin buscar culpables, tratándolos como problemas del sistema. |
| **Concepto del curso** | **ADKAR** por perfil [S4]. **Seguridad psicológica**: definición y 12 preguntas [S5], y los tres supuestos del líder que la erosionan [PS]. **Liderazgo ágil**: el líder dedica tiempo a quitar impedimentos, no a la operativa [S5]. **Conversaciones significativas** con managers: indagación apreciativa y escucha empática [HRA-C]. **Rogers** para elegir a los primeros participantes [S4, HRA-R]. *Moving Motivators* [MM] y roles **ETBO** [ETBO] para entender motivaciones y equilibrar el equipo. |
| **Acción concreta** [Propuesta] | (a) Diagnóstico ADKAR rápido por perfil (ver §5.4). (b) **Acompañamiento 1:1 en el puesto** a los líderes del piloto durante su primer proceso en MyPort: la "siguiente etapa" que RR. HH. ya había identificado. (c) **Acuerdos de equipo** de seguridad psicológica: un bloqueo informado es información, no falta; el error honesto se analiza en la retrospectiva sin sanción. (d) Una conversación significativa con cada líder participante antes del inicio, para entender qué gana y qué teme perder. |
| **Indicador** | **Uso efectivo de MyPort por los líderes del piloto:** porcentaje de acciones del líder (revisión de candidatos, *feedback* de entrevista y decisión) hechas por él en MyPort, sin intervención de RR. HH. Como complemento, un **pulso de seguridad psicológica** quincenal con un subconjunto de las 12 preguntas de la S5. |

### 3.4 Procesos — flujo, experimentación, mejora continua y eliminación de bloqueos

| Elemento | Contenido |
|---|---|
| **Situación actual** | El flujo es secuencial y con muchos traspasos (ver §2.1). La coordinación se hace por correo y el seguimiento con correos y llamadas [Hecho, BPMN]. No hay plazo para Evaluar.com [Hecho, TFM-A4 obs. 9]. No hay tiempos por etapa ni indicadores de extremo a extremo [Hecho, TFM Tabla 16]. Los descartados no reciben aviso hasta el cierre [Hecho, TFM-A4]. El TFM ya propone validar con pilotos acotados y decidir si continuar, ajustar o detener [Hecho, TFM §6.4.2], pero no define cómo organizar ese aprendizaje. |
| **Barrera** | El **trabajo invisible** impide ver dónde se detiene un proceso. No hay **políticas explícitas** de entrada y salida por etapa (cuándo está lista una requisición o una terna). El trabajo ambiguo se resuelve por correo: es la **iteración inefectiva** de Repenning [REP]. Las mejoras no tienen un ciclo propio y se mezclan con la operación diaria. |
| **Cambio requerido** | **De** un flujo secuencial e invisible **a** un flujo visualizado, con políticas explícitas, **desencadenantes** que activan la colaboración cuando algo se bloquea y un ciclo de mejora continua (PDCA). |
| **Concepto del curso** | **Los cuatro principios del diseño dinámico del trabajo** [REP]: distinguir lo bien definido de lo ambiguo; trabajar en unidades pequeñas verificadas con frecuencia; identificar la cadena de ayuda; introducir desencadenantes y verificaciones. **Kanban**: visualizar, limitar el WIP, explicitar políticas y medir el *lead time* (módulo "Agilidad técnica: Kanban & Scrumban") [S5]. **Ciclo de Deming (PDCA)** [S4]. "Foco en el trabajo que aporte valor" [S4, Procesos]. |
| **Acción concreta** [Propuesta] | (a) **Tablero Kanban** del flujo de la familia piloto, con una tarjeta por vacante y columnas por etapa real. (b) **Lista de verificación de requisición lista**, al estilo RefineCo: perfil, criterios ponderados y disponibilidad de agenda del líder antes de publicar. (c) **Desencadenante**: si una tarjeta supera el plazo acordado en una etapa, se marca como bloqueada y se trata en la siguiente reunión de flujo. (d) **Bloque fijo semanal de entrevistas** en la agenda del líder, que pasa a "modo estudio". (e) Reunión breve de flujo dos o tres veces por semana. |
| **Indicador** | ***Lead time*** **por vacante** y **tiempo por etapa**. Como complemento: el **tiempo bloqueado** y sus principales causas, y el porcentaje de candidatos comunicados en el momento de la decisión. |

### 3.5 Tecnología — habilita, pero no sustituye el cambio organizativo

| Elemento | Contenido |
|---|---|
| **Situación actual** | Oracle Recruiting/MyPort es el núcleo transaccional, con aprovechamiento parcial [Hecho, TFM Tabla 36]. La función de revisión del líder está disponible desde octubre de 2025, pero se usa poco [Hecho, TFM-A4 obs. 7]. QlikView se alimenta a mano y no cubre el 100 % de los procesos [Hecho, TFM-A4 obs. 13]. Conviven Evaluar.com aislado, planillas Excel y bases paralelas, y WhatsApp personal [Hecho, TFM Tabla 36]. No se usa IA por lineamientos corporativos de protección de datos [Hecho, TFM §1.5.3]. Existe capacidad corporativa de Data & AI en otros dominios [Hecho, TFM §1.5.2]. |
| **Barrera** | La tecnología existe, pero **no se adopta** y **los datos no fluyen**. Hay riesgo de "transformación por herramienta": esperar que la IA o un tablero resuelvan un problema de comportamiento. La restricción a la IA es de gobierno, no de capacidad, y no se controla localmente [TFM DAFO D5]. |
| **Cambio requerido** | **De** desplegar funcionalidades **a** entregar incrementos pequeños que el usuario valida en ciclos cortos y que se priorizan por su impacto en el flujo. IA solo en casos de bajo riesgo, con supervisión humana y aprobación corporativa. |
| **Concepto del curso** | Tecnología según la sesión 4: "herramientas que apoyen la agilidad, **foco en la entrega temprana** de automatizaciones, equipo de IT" [S4]. "Cambiar las herramientas es más fácil que cambiar la mentalidad" y el valor de los datos accesibles [WD]. Unidades pequeñas verificadas con frecuencia [REP]. |
| **Acción concreta** [Propuesta] | Un **backlog técnico priorizado por outcomes**, que entregue en este orden: (1) **usar lo que ya existe**: CV y *feedback* del líder dentro de MyPort, sin correo, en la familia piloto; (2) un tablero mínimo de *lead time* y bloqueos alimentado desde MyPort; (3) solo con aprobación de casa matriz, **un** caso de IA de bajo riesgo (detección de expedientes incompletos o borradores de comunicaciones), sin descartes ni decisiones automatizadas. Cada incremento se muestra en la revisión quincenal. |
| **Indicador** | **Porcentaje de procesos del piloto registrados de extremo a extremo en MyPort** (hoy: 100 % de los internos y 70–80 % de los externos). Como complemento: el número de cargas o registros manuales por proceso y de envíos por canales fuera del modelo (correo con CV, WhatsApp). |

### 3.6 Mapa de calor del diagnóstico [Propuesta, valoración cualitativa del equipo]

| Dimensión | Madurez actual | Peso en la brecha 38→28 | Control local | Prioridad en el piloto |
|---|---|---|---|---|
| Estrategia | Media (objetivo claro, outcomes sin línea base) | Media | Alto | Alta: es la condición de partida |
| Estructura | Baja (sin dueño E2E ni decisiones explícitas) | **Alta** (tiempo del líder) | Medio | **Muy alta** |
| Personas | Baja-media (capacitación hecha, adopción no lograda) | **Alta** | Medio | **Muy alta** |
| Procesos | Baja (flujo invisible, sin políticas) | **Alta** | Alto | **Muy alta** |
| Tecnología | Media (plataforma existe, poco usada; IA restringida) | Media | Bajo en IA, alto en adopción | Media: habilitador |

*La valoración es cualitativa y se basa en la evidencia citada; debe contrastarse con RR. HH.*

---

## 4. Diferenciación: agilidad técnica, de equipo, organizativa y gestión del cambio

En el curso, **"agilidad técnica" se refiere a los marcos y prácticas** (Kanban, Scrum y Scrumban, según la hoja de ruta de la S5), **no a la tecnología** (MyPort, Analytics, IA). Conviene dejarlo claro en la exposición para evitar confusiones.

| Nivel | Qué es | En el caso Hapag-Lloyd Chile | Qué incluye el piloto [Propuesta] | Riesgo si se confunde |
|---|---|---|---|---|
| **Agilidad técnica** | Prácticas y marcos para gestionar el trabajo: Kanban, Scrum y Scrumban | No existe hoy en el proceso | Kanban del flujo de reclutamiento; Scrumban en ciclos de dos semanas para las mejoras; políticas explícitas; métricas de flujo | Presentar Scrum o Kanban como fin y no como mecanismo de aprendizaje |
| **Agilidad de equipo** | Cómo colabora un equipo: roles, autoorganización, seguridad psicológica, *feedback* y complementariedad | El trabajo se hace en solitario (una reclutadora) y por traspasos | Equipo multidisciplinario con PO y facilitador; acuerdos de equipo; retrospectivas; equilibrio de roles (ETBO) | Creer que juntar personas en reuniones ya es un equipo |
| **Agilidad organizativa** | Cómo se alinean estrategia, estructura, personas, procesos y tecnología para responder con rapidez y aportar valor | Matriz local, regional y casa matriz; decisiones implícitas y limitada delegación documentada | Derechos de decisión explícitos; acuerdo de servicio líder–RR. HH.; liderazgo de servicio; escalamiento basado en evidencia | Querer reorganizar la empresa (tribus, SAFe o Nexus) en lugar de experimentar en un ámbito acotado |
| **Gestión del cambio** | Cómo pasan las personas del estado actual al deseado y reducen su resistencia | Capacitación hecha, adopción no lograda | ADKAR por perfil; elementos de Kotter; Rogers para elegir participantes; PDCA; comunicación de *quick wins* | Reducir el cambio a "capacitar y comunicar" |

Las cuatro capas se necesitan entre sí:

- La agilidad técnica sin seguridad psicológica produce tableros que esconden bloqueos.
- La agilidad organizativa sin gestión del cambio produce acuerdos que nadie cumple.
- La gestión del cambio sin práctica técnica no deja evidencia que medir.

---

## 5. Recomendaciones para el piloto

### 5.1 Alcance del piloto [Propuesta]

**Criterios de selección** (de `CLAUDE.md`, aplicados al caso):

| Criterio | Aplicación |
|---|---|
| Volumen suficiente | Elegir una familia con procesos recurrentes dentro de los ~615 anuales. El volumen por familia **no está documentado** [por validar con RR. HH.]. |
| Líderes dispuestos | Uno o dos líderes *innovators* o *early adopters* (Rogers). |
| Complejidad manejable | **Excluir** los perfiles que el TFM identifica como de mayor dificultad de cobertura (auditoría, impuestos, asuntos legales, operadores de naves) y las posiciones regionales con intervención directa de casa matriz [Hecho, TFM §1.4]. |
| Recorrido de extremo a extremo | Priorizar **movilidad interna**, porque concentra cerca del 90 % del volumen y el 100 % ya se registra en MyPort. Incluir, cuando se produzca, el **reemplazo externo encadenado** (proceso "en escalera"), ya que el externo suele ser junior tras cubrir la posición senior internamente [Hecho, TFM-A4 obs. 17–18]. Así el piloto recorre ambos modelos sin abrir perfiles complejos. |
| Bajo riesgo | Sin IA en el primer ciclo; IA de bajo riesgo solo con aprobación corporativa. |

**Duración:** propuesta de **8 a 12 semanas** (4 a 6 ciclos de dos semanas). Es una propuesta del equipo, no un plazo validado. Según la duración real de los procesos, puede que pocos procesos se cierren completos dentro del piloto; en ese caso los indicadores de etapa (tiempo de decisión, tiempo bloqueado) serán la evidencia principal, más que el tiempo total de cobertura [Supuesto].

### 5.2 Equipo piloto [Propuesta]

| Rol | Perfil (sin nombres) | Dedicación y observaciones |
|---|---|---|
| Sponsor | Responsable ejecutivo de RR. HH. | Revisión quincenal; elimina obstáculos y negocia con casa matriz. **Hoy no está nombrado** [Hecho, TFM-A1] |
| *Product Owner* | Responsable de Talent Acquisition / Recruitment | Prioriza el backlog por outcomes. Si es la misma reclutadora, el piloto debe **liberar parte de su carga** primero |
| Facilitador ágil | Perfil interno de RR. HH. u OD, o el equipo consultor en el arranque | **No debería ser la reclutadora**, por capacidad. Facilita el flujo, las ceremonias y la eliminación de impedimentos |
| Equipo multidisciplinario | Reclutadora, **psicóloga interna** (actor documentado y clave en la evaluación), IT, Data/Analytics, Legal/Data Privacy, Compensaciones, 1–2 líderes solicitantes; soporte corporativo de Oracle cuando corresponda | Dedicación parcial y por demanda, salvo el núcleo (PO, reclutadora, psicóloga y facilitador) |
| Usuarios piloto | Candidatos internos y externos de la familia piloto; líderes *early adopters* | Dan *feedback* en las revisiones y en encuestas breves |

La **composición del equipo** puede revisarse con ETBO (equilibrio entre roles de impulso, cohesión, método, análisis y conexión) y *Moving Motivators* (qué motiva a cada participante) [ETBO, MM]. Así se evita un equipo homogéneo, sin perfiles de conexión con los líderes ni de análisis de datos.

### 5.3 Marco de trabajo [Propuesta]

| Componente | Para qué | Práctica |
|---|---|---|
| **Kanban del flujo de reclutamiento** | Ver dónde se detiene cada vacante | Tablero por etapa; políticas de entrada y salida; límite de WIP donde tenga sentido (por ejemplo, entrevistas abiertas por líder); edad de las tarjetas; bloqueos marcados |
| **Scrumban para mejorar el modelo** | Experimentar y aprender en ciclos cortos | Backlog de experimentos priorizado por outcomes; ciclos de dos semanas; revisión con stakeholders; retrospectiva |
| **Desencadenantes y verificaciones (Repenning)** | Pasar a colaborar cuando algo falla | Requisición incompleta, devuelta. Plazo de etapa superado: se trata en la reunión de flujo. Bloque fijo de entrevistas como verificación planificada |
| **Cadencias** | Ritmo de aprendizaje | Priorización semanal; reunión de flujo de 15 minutos, 2–3 veces por semana; revisión quincenal con el sponsor; retrospectiva quincenal; revisión mensual de outcomes con decisión de continuar, ajustar o detener |
| **Su-Ha-Ri** | Adaptar las prácticas | Primero se siguen las prácticas tal cual y luego se adaptan con evidencia [S4, *key learnings*] |

Cada experimento del backlog debe registrar:

- hipótesis;
- usuario;
- cambio probado;
- indicador;
- criterio para continuar, ajustar o detener;
- riesgo y control.

**Candidatos a primeros experimentos y *quick wins*** [Propuesta; factibilidad por validar]:

1. CV y *feedback* del líder solo por MyPort en la familia piloto. La funcionalidad ya existe.
2. Bloque fijo semanal de entrevistas en la agenda del líder.
3. Lista de verificación de "requisición lista".
4. Comunicar al candidato descartado en el momento de la decisión y no al cierre.
5. Probar una ventana de recepción de CV más corta en procesos internos, si la política lo permite.
6. Plazo explícito para completar las pruebas de Evaluar.com y enviarlas por canal corporativo, eliminando WhatsApp.

### 5.4 Enfoque de gestión del cambio [Propuesta]

**ADKAR por perfil** (hipótesis de partida, a validar con entrevistas breves):

| Perfil | Awareness | Desire | Knowledge | Ability | Reinforcement | Intervención prioritaria |
|---|---|---|---|---|---|---|
| Líderes solicitantes | Parcial: ¿conocen el efecto de su demora? | Por validar | **Sí** (capacitación hecha) | **Brecha** (MyPort no intuitivo) | **Ausente** | Acompañamiento 1:1 y visibilidad de su tiempo de decisión con reconocimiento, no con sanción |
| Reclutadora | Alta sobre la carga | Por validar | Alta | Alta, pero sin capacidad | Ausente | Liberar capacidad; acuerdo para dejar de absorber tareas del líder |
| Psicóloga | Por validar | Por validar | Media sobre el nuevo flujo | Media | Ausente | Integrar los resultados de Evaluar.com en el expediente; plazos explícitos |
| Compensaciones e IT | Baja sobre su papel en el flujo | Por validar | Media | Media | Ausente | Ver su etapa en el tablero; traspaso desde el registro y no por Outlook |
| RR. HH. en general | **Limitada sobre el desperdicio** ("sin certeza de tareas repetitivas") | Alta respecto a la IA | Media | Media | Ausente | Mostrar datos del flujo propio antes de proponer soluciones |

**Kotter (solo los pasos que resuelven una barrera concreta):**

- **Sentido de urgencia:** ZIM, Ley 21.719, costos laborales y 38 días.
- **Coalición ligera:** sponsor, PO, facilitador y dos líderes.
- **Visión** del piloto en una frase.
- **Eliminar obstáculos:** acuerdos de decisión y canales paralelos.
- ***Quick wins*** visibles en cada revisión quincenal.
- **Anclar y escalar** solo con evidencia.

**Rogers:**

- Empezar con *innovators* y *early adopters*: los líderes con vacantes recurrentes y apertura a probar.
- No incluir *laggards* en el piloto. Esto aplica el principio n.º 9 de la S4: "incluye a todos menos los que no están dispuestos".
- La mayoría temprana se suma por **prueba social** con los resultados del piloto [HRA-R; PS].

**PDCA:** cada ciclo de dos semanas es un Plan–Do–Check–Act, y la revisión mensual de outcomes es el *Act* de mayor nivel.

**Lecciones del caso real de la sesión 4** que se aplican directamente:

1. Lograr primero el compromiso del management.
2. Elegir equipos piloto con objetivos claros y motivados.
3. Visualizar los *quick wins*.
4. Trabajar la seguridad psicológica.
5. Crear un equipo del cambio.
6. Escalar solo cuando haya progreso.
7. Comunicar con transparencia.

[S4]

### 5.5 Métricas principales [Propuesta]

| Tipo | Métrica | Línea base | Meta |
|---|---|---|---|
| **Outcome** | Tiempo total de cobertura | **38 días** [Hecho] | **28 días** [Hecho, objetivo del modelo] |
| Outcome | Procesos registrados de extremo a extremo | **100 % internos; 70–80 % externos** [Hecho] | **100 %** [Hecho, meta propuesta en el TFM] |
| Outcome | Tiempo de decisión del líder por etapa | Por medir | Por acordar |
| Outcome | Cargas o registros manuales por proceso | Por medir | Por acordar |
| Outcome | Candidatos comunicados oportunamente | Por medir (hoy, aviso solo al cierre) | Por acordar |
| Outcome | Satisfacción de candidatos y líderes | Por medir | Por acordar |
| **Flujo** | *Lead time*, *cycle time* por etapa, WIP, *throughput*, edad de tarjetas, tiempo bloqueado y causas | Por medir (se construye en el primer ciclo) | Por acordar |
| **Adopción** | Uso efectivo de MyPort por los líderes del piloto | Por medir | Por acordar |
| Adopción | Envíos por canales fuera del modelo (correo con CV, WhatsApp) | Por medir | Por acordar |
| **Equipo y cambio** | Pulso de seguridad psicológica; experimentos completados; mejoras adoptadas; participación en revisiones y retrospectivas | Por medir | Por acordar |

No se agregan metas numéricas que no estén documentadas.

---

## 6. Supuestos, vacíos de información y puntos a validar

| # | Tema | Situación | Acción sugerida |
|---|---|---|---|
| 1 | Sponsor ejecutivo | No hay sponsor nominal documentado ("presupuesto de RR. HH.") | Confirmarlo con Hapag-Lloyd Chile |
| 2 | Familia de cargos piloto | El volumen por familia no está documentado | Pedir a RR. HH. los procesos de los últimos 12 meses por familia |
| 3 | Distribución de los 38 días por etapa | Desconocida | Medirla en el primer ciclo; es la primera tarea del Kanban |
| 4 | Peso de la ventana de recepción de CV (1–3 semanas) | Hipótesis del equipo | Validar si es una política modificable |
| 5 | Rol del nivel L1 | Vigencia y responsabilidad pendientes [TFM §6.2] | Confirmar antes de dibujar el flujo del piloto |
| 6 | Capacidad del equipo | Una reclutadora; jornada de 42 h | Acordar una dedicación realista y qué se deja de hacer |
| 7 | Clima y seguridad psicológica | Sin evidencia documentada | Medir un pulso en la semana 1 |
| 8 | IA de bajo riesgo | Requiere aprobación de casa matriz | Dejarla fuera del primer ciclo y preparar el expediente de controles en paralelo |
| 9 | Inconsistencias del levantamiento | RR. HH. describe "3 etapas" frente a un BPMN con muchos más pasos; dice "sin certeza de tareas repetitivas" pero menciona tareas manuales | Usarlo como evidencia de *Awareness* limitado, sin contradecir a la fuente |
| 10 | Material del curso no disponible en el repositorio | La "Guía Kanban & Scrum" (*pre-work*), el caso ING y la teoría detallada de ADKAR y Kotter no están en el repositorio; solo se mencionan en las diapositivas | Fundamentar Kanban, Scrumban y los modelos de cambio a nivel de diapositiva, o subir esos materiales si se quiere citarlos con más detalle |
| 11 | Ley 21.719 | Fecha de vigencia según el TFM (1-dic-2026) | El TFM indica verificarla al implementar |

---

## 7. Inventario de documentos revisados

| Documento | Tipo | Uso en el diagnóstico |
|---|---|---|
| `CLAUDE.md` | Instrucciones del proyecto | Consigna, marco, reglas y datos validados |
| `Segunda Entrega TD ... _v2.docx` | Caso (proyecto final del Máster) | Contexto, organización, DAFO, línea base, expectativas, AS-IS, ecosistema tecnológico, IA y experimentación |
| `Flujo Reclutamiento.pdf` | Caso (BPMN, solo imagen) | Actores, traspasos, entrevistas y registros manuales |
| `EADA_ Sesión 4 Agilidad Organizativ.pdf` | Curso | Cinco dimensiones, *Agile Fluency*, 10 principios, fases de transformación, ADKAR, Kotter, Rogers, PDCA y *key learnings* |
| `Sesion 5.pdf` | Curso | Liderazgo ágil, seguridad psicológica (12 preguntas) y 9 principios del liderazgo ágil |
| `75924.pdf` | Lectura (McKinsey) | Responsabilidad de extremo a extremo y rol del manager ágil |
| `75981.pdf` | Lectura (AWS) | Seguridad psicológica y supuestos del líder |
| `76620 - Perfil de comportamiento...pdf` | Lectura (HR Agile) | Curva de Rogers aplicada a RR. HH. |
| `76622.pdf` | Lectura (HR Agile) | Resistencias de managers y conversaciones significativas |
| `78841 - Un nuevo enfoque en el diseño...pdf` | Lectura (HDBR / MIT) | Diseño dinámico del trabajo, iteración inefectiva y caso RefineCo |
| `78850 - workday-OrganizationalAgility_r.pdf` | Lectura (Workday) | Tecnología frente a cultura, datos accesibles, decisión delegada y métricas ágiles |
| `86403.pdf` | Lectura (ETBO) | Roles de equipo y complementariedad |
| `75930.pdf` | Herramienta (Management 3.0) | *Moving Motivators* |

---

## 8. Próximo paso propuesto

Tras la revisión del equipo, el siguiente paso según `CLAUDE.md` §11 es **proponer el storyboard de la presentación** (máximo nueve diapositivas). Antes conviene cerrar al menos los puntos 1, 2 y 5 de la sección 6, porque determinan el alcance y el equipo del piloto.

---

## 9. Estado y ajustes acordados en la revisión

El diagnóstico queda **aprobado como documento de soporte**, con estos ajustes:

1. El proceso no se clasifica formalmente como *Pre-agile*: presenta características de una etapa inicial de adopción ágil.
2. No se afirma que el piloto alcance una zona del *Agile Fluency Model*. Solo se dice que desarrollará capacidades iniciales de foco, trabajo en equipo, visibilidad y aprendizaje.
3. "Liderazgo de control" se sustituye por "decisiones implícitas y limitada delegación documentada".
4. **Para la presentación:**
   - Marcos principales: Kanban, Scrumban, ADKAR, Rogers, seguridad psicológica, y sponsor, coalición y *quick wins* de Kotter.
   - Sustento secundario en notas: Repenning, PDCA, ETBO, *Moving Motivators*, Su-Ha-Ri y *Agile Fluency*.
   - La IA solo aparece como experimento posterior de bajo riesgo y condicionado.
   - Solo cinco métricas visibles.
   - Narrativa: problema → hipótesis → experimento → evidencia → decisión.

Las acciones y métricas adicionales de este documento (por ejemplo, el caso de IA de la §3.5) se mantienen como sustento, no como contenido de las diapositivas.
