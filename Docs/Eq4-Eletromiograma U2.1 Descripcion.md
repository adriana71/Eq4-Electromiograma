Materias: Taller de Desarrollo de Tecnologías de la Automatización (TDTA) y Programación Avanzada

Docente(s) responsable(s):
- Marcos Romo Avilés

- Adriana Rojas Molina

Integrantes del equipo:
1. Ian Carlo Aguilar Vázquez 343509
2. Victor Ortigosa Coral 343540
3. Ezequiel Gil Guerrero Patiño 343563
4. Carlos Gabriel López Rangel 343532

Carrera: Ingeniería en Automatización
Campus: Centro Universitario

# 🦾 MyoTrack AI
**Sistema Inteligente de Adquisición de Señales Biomecánicas (EMG) y Evaluación del Ejercicio Mediante Asistente de Inteligencia Artificial**

---

## 1. RESUMEN EJECUTIVO
El presente documento describe la propuesta de desarrollo de MyoTrack AI, un sistema integral que combina electrónica de instrumentación biomédica, automatización y desarrollo de software con inteligencia artificial, orientado a la adquisición, procesamiento e interpretación de señales electromiográficas (EMG) de superficie en tiempo real.

El problema que se busca resolver es la falta de herramientas accesibles, portátiles que permitan a pacientes en proceso de rehabilitación y a practicantes de actividad física evaluar de forma cuantitativa la activación muscular, la fatiga y la calidad técnica de sus movimientos, sin depender exclusivamente de la supervisión presencial de un especialista.

La solución propuesta consiste en un módulo de hardware basado en electrodos de superficie y un microcontrolador que digitaliza y transmite las señales EMG hacia una aplicación de software móvil. Dicha aplicación integrará un agente de inteligencia artificial, capaz de interpretar los datos y generar retroalimentación personalizada en tres posibles frentes: rehabilitación física, evaluación de rendimiento deportivo y corrección postural.

**Impacto tecnológico esperado:** Generar un prototipo funcional con aplicabilidad real en los sectores de salud, deporte y tecnología "wearable".

---

## 2. PLANTEAMIENTO DEL PROBLEMA Y JUSTIFICACIÓN

### 2.1 Descripción del problema
La evaluación de la actividad muscular durante procesos de rehabilitación física o entrenamiento deportivo suele depender de la observación de un terapeuta, entrenador o del propio usuario. Esta aproximación presenta falta de datos cuantitativos, dificultad para detectar fatiga muscular incipiente y alto riesgo de lesiones derivadas de una ejecución postural incorrecta que no es detectada a tiempo

Los equipos de electromiografía disponibles comercialmente para uso clínico son, en su mayoría, costosos, de uso exclusivo institucional y no ofrecen integración con sistemas de inteligencia artificial orientados a la generación de retroalimentación automática y personalizada para el usuario final.

### 2.2 Justificación
Vemos necesario el desarrollo de un sistema propio, académico y de bajo costo, que integre electrónica de adquisición de señales biomédicas con software inteligente, dado que:
- Atiende una necesidad real y vigente tanto en el ámbito clínico como en el deportivo.
- Sienta las bases para el desarrollo de dispositivos wearable de bajo costo con capacidades de análisis inteligente, un área en creciente expansión dentro de la ingeniería biomédica y la salud digital.

### 2.3 Recuperación de la oportunidad seleccionada (Unidad 1) y beneficiarios
- **Oportunidad seleccionada:** Desarrollo de un sistema accesible y portátil para la medición cuantitativa de la actividad y fatiga muscular mediante electromiografía de superficie (sEMG) fuera de entornos clínicos especializados.
- **Posibles beneficiarios y actores involucrados:**
  - **Usuarios directos:** Personas en procesos de rehabilitación física y practicantes de entrenamiento de fuerza o acondicionamiento físico en gimnasio.
  - **Especialistas de apoyo:** Fisioterapeutas, rehabilitadores y entrenadores deportivos que requieren métricas objetivas para evaluar el progreso y prevenir lesiones en sus pacientes o usuarios.
  - **Sector académico:** Estudiantes y docentes de ingeniería interesados en bioinstrumentación, procesamiento de señales y sistemas embebidos.

### 2.4 Distinción entre lo que sabemos y lo que debemos averiguar (U2.1)

| Aspecto | ¿Qué sabemos hasta ahora? | ¿Qué necesitamos investigar, consultar o verificar? |
| :--- | :--- | :--- |
| **Contexto de la situación** | El seguimiento en rehabilitación y gimnasio suele hacerse de forma visual y subjetiva, lo que impide detectar con precisión el inicio de la fatiga muscular. | Qué métricas e indicadores cuantitativos son los más relevantes durante una rutina para prevenir lesiones por sobrecarga o mala técnica. |
| **Personas o actores involucrados** | Los usuarios en entrenamiento y pacientes en rehabilitación no suelen tener acceso cotidiano a equipos de electromiografía por su costo y complejidad. | Qué tan cómoda y práctica resulta la colocación de electrodos de superficie para un usuario durante el ejercicio dinámico. |
| **Forma actual en que se atiende la necesidad** | Mediante supervisión presencial de un fisioterapeuta/entrenador o con dispositivos comerciales que solo miden frecuencia cardíaca y movimiento general. | Qué dispositivos portátiles de EMG existen actualmente en el mercado, cómo procesan la información y qué limitaciones presentan. |
| **Limitaciones o dificultades identificadas** | Las señales EMG de superficie son de muy baja amplitud y susceptibles al ruido eléctrico y artefactos por movimiento. | Qué etapas de filtrado analógico y procesamiento digital son indispensables para limpiar la señal sin perder información útil del músculo. |
| **Información técnica necesaria** | Se requiere acondicionamiento analógico (amplificación y filtrado), digitalización mediante ADC y extracción de características de la señal. | Cómo medir y cuantificar numéricamente la fatiga muscular a partir de la señal EMG (parámetros en el dominio del tiempo y frecuencia) y cómo estructurar esos datos para su análisis. |

### 2.5 Preguntas iniciales para comprender mejor el proyecto (U2.1)
1. **Cuantificación de la fatiga:** ¿Cómo se puede medir numéricamente la fatiga muscular a partir de una señal EMG de superficie y qué indicadores matemáticos (como el valor RMS, la frecuencia media o la frecuencia mediana del espectro) reflejan con mayor fiabilidad que el músculo se está fatigando?
2. **Acondicionamiento y filtrado:** ¿Qué características de filtrado analógico y qué frecuencia de muestreo son necesarias para capturar la señal muscular limpia durante ejercicios en movimiento sin saturación ni interferencia de la red eléctrica?
3. **Transmisión y arquitectura:** ¿Qué volumen de datos genera el muestreo en tiempo real y cuál es la forma más eficiente de empaquetarlos y transmitirlos inalámbricamente hacia la aplicación sin pérdida de información?
4. **Interpretación para el usuario:** ¿Cómo debemos traducir los valores numéricos de activación y fatiga muscular para que el agente de IA genere recomendaciones claras, seguras y fáciles de entender para el usuario final?

---

## 3. OBJETIVOS

### 3.1 Objetivo General
Diseñar, desarrollar e implementar un sistema embebido de adquisición de señales electromiográficas (EMG) integrado con una aplicación de software orientada a objetos y un agente de inteligencia artificial, capaz de apoyar procesos de rehabilitación física, evaluación de rendimiento en el gimnasio y corrección de postura mediante el análisis en tiempo real de la actividad muscular.

### 3.2 Objetivos Específicos

**Automatización y Hardware (TDTA)**
- Seleccionar e integrar un microcontrolador con conversor analógico-digital (ADC) apto para el muestreo de señales biomecánicas en tiempo real.
- Implementar el módulo de comunicación inalámbrica (Bluetooth Low Energy o Wi-Fi) para la transmisión de datos hacia la aplicación cliente.
- Desarrollar el firmware embebido para la sincronización, muestreo y empaquetado de datos provenientes de múltiples canales EMG.
- Validar experimentalmente la fidelidad y el nivel de ruido de la señal adquirida, comparando contra referencias teóricas de electromiografía de superficie.

**Software Avanzado e Inteligencia Artificial**
- Diseñar la arquitectura de software de la aplicación móvil, aplicando patrones de diseño adecuados para el manejo de datos en tiempo real.
- Implementar los módulos de recepción, almacenamiento y visualización de señales EMG mediante estructuras de datos eficientes.
- Integrar, mediante API, un agente de inteligencia artificial capaz de procesar los datos biomecánicos y generar retroalimentación contextual para rehabilitación, entrenamiento y postura.
- Desarrollar los módulos funcionales de la aplicación: seguimiento de rehabilitación, evaluación de fatiga/rendimiento en el gimnasio y corrección postural.
- Implementar pruebas unitarias y de integración que garanticen la robustez, escalabilidad y mantenibilidad del software desarrollado.

---

## 4. ALCANCE Y REQUISITOS DEL SISTEMA
Con el fin de delimitar de forma realista el desarrollo dentro del periodo académico establecido, se definen a continuación los elementos incluidos y excluidos del alcance del proyecto.

### Dentro del alcance
| N° | Elemento incluido en el alcance del proyecto |
|:--:|:---|
| 1 | Adquisición de señales EMG de superficie mediante electrodos en al menos dos grupos musculares. |
| 2 | Acondicionamiento analógico de la señal previo a la digitalización. |
| 3 | Transmisión inalámbrica de datos desde el módulo embebido hacia la aplicación cliente. |
| 4 | Aplicación de escritorio y/o móvil para la visualización de señales en tiempo real. |
| 5 | Integración de un agente de IA (mediante API) para el análisis de patrones musculares y generación de retroalimentación. |
| 6 | Módulos funcionales de rehabilitación guiada, evaluación de rendimiento en gimnasio y corrección postural básica. |
| 7 | Almacenamiento histórico de sesiones para seguimiento de progreso del usuario. |

### Fuera del alcance (versión actual)
| N° | Elemento excluido en esta primera versión |
|:--:|:---|
| 1 | Diagnóstico médico certificado; el sistema es una herramienta de apoyo, no un dispositivo médico regulado. |
| 2 | Captura de señales EMG intramuscular (invasiva); el proyecto se limita a electromiografía de superficie. |
| 3 | Corrección postural mediante visión por computadora avanzada (cámaras 3D) en esta primera versión. |
| 4 | Comercialización o fabricación masiva del dispositivo; el alcance es un prototipo funcional académico. |
| 5 | Integración con dispositivos de terceros (wearables comerciales) fuera de los sensores propios del proyecto. |

### 4.1 Requisitos generales del sistema
- Requisito no funcional: la aplicación debe ejecutarse en al menos una plataforma (Windows, Android o multiplataforma) con interfaz de usuario intuitiva.
- Requisito no funcional: el sistema debe permitir la operación continua durante sesiones de al menos 30 minutos sin pérdida significativa de datos.
- Requisito de seguridad: los datos biométricos del usuario deben almacenarse de forma local o cifrada, respetando principios básicos de privacidad de datos de salud.

> **NOTA IMPORTANTE:** MyoTrack Al es una herramienta de apoyo académico y de acondicionamiento físico. No sustituye el diagnóstico, tratamiento o supervisión de un profesional certificado de la salud.

---

## 5. METODOLOGÍA DE DESARROLLO Y CRONOGRAMA

### 5.1 Fases del proyecto
- **Diseño:** análisis de requisitos, investigación de componentes y definición de arquitectura general del sistema.
- **Prototipado:** construcción del circuito de acondicionamiento de señal, integración de electrodos y pruebas iniciales de adquisición.
- **Programación:** desarrollo del firmware embebido y de la aplicación de software, incluyendo la integración del agente de IA.
- **Pruebas y validación:** verificación funcional, pruebas con usuarios piloto, calibración de umbrales y ajuste de algoritmos de evaluación.

### 5.2 Cronograma tentativo

| Fase | Actividades Principales | Semanas | Entregable |
|:---|:---|:---:|:---|
| 1. Diseño y Análisis | Levantamiento de requisitos, investigación de sensores EMG, definición de arquitectura HW/SW y selección de componentes. | 1-3 | Documento de especificación técnica |
| 2. Prototipado de Hardware | Diseño del circuito de acondicionamiento de señal (amplificación, filtrado), integración de electrodos y microcontrolador, pruebas de adquisición. | 3-6 | Prototipo funcional de adquisición EMG |
| 3. Desarrollo de Software Base | Implementación del firmware, protocolo de comunicación, y estructura de la aplicación cliente. | 6-9 | Firmware y esqueleto de aplicación |
| 4. Integración de IA | Preprocesamiento de señales, extracción de características, conexión con API del agente de IA y lógica de evaluación de ejercicio. | 9-10 | Módulo de IA integrado y funcional |
| 5. Pruebas y Validación | Pruebas unitarias | 10-11 | Reporte de pruebas y validación |
| 6. Documentación y Cierre | Elaboración de manuales de usuario y técnico, preparación de presentación final y defensa del proyecto. | 11-12 | Documento final y presentación |

---

## 6. CONCLUSIONES / IMPACTO ESPERADO

### 6.1 Beneficios académicos
- Aplicación integral de conocimientos de instrumentación electrónica, procesamiento digital de señales y sistemas embebidos.
- Fortalecimiento de competencias en arquitectura de software, patrones de diseño e inteligencia artificial mediante API.
- Desarrollo de habilidades de trabajo interdisciplinario entre hardware y software, replicando condiciones reales de la industria biomédica y tecnológica.

### 6.2 Beneficios prácticos y sociales
- Aporte de una herramienta accesible y de bajo costo para el monitoreo objetivo de procesos de rehabilitación física.
- Apoyo a la prevención de lesiones deportivas mediante la detección temprana de fatiga muscular y desviaciones posturales.
- Sentado de las bases técnicas para futuras versiones del sistema con mayor número de canales, algoritmos de IA más sofisticados y validación clínica formal.

---

## 7. ORGANIZACIÓN Y ACUERDOS DEL EQUIPO (U2.2)

### 7.1 Participación inicial de cada integrante

| Integrante | Me interesa participar en... | Inicialmente puedo colaborar en... | Me gustaría aprender o desarrollar... |
| :--- | :--- | :--- | :--- |
| **Gil Ezequiel Guerrero Patino** | **La creacion del prototipo y programar** | **El armado del prototipo inicial y que pueda funcionar de forma muy basica** | **Programar, hacer modelos mas complejos con los PCB** |
| **Ian Carlo Aguilar Vazquez** | | | |
| **Carlos Gabriel Lopez Rangel** | **El diseño de la arquitectura de la aplicación, el procesamiento de la señal EMG y, de ser necesario, la etapa de filtrado analógico.** | **La estructuración y redacción de la documentación técnica del proyecto.** | **La integración de la API de Inteligencia Artificial y la implementación de la comunicación inalámbrica.** |
| **Victor Ortigoza Coral** | | | |

### 7.2 Necesidades de aprendizaje y apoyo del equipo

| Necesidad identificada | ¿Qué sabemos actualmente? | ¿Qué necesitamos hacer para atenderla? |
| :--- | :--- | :--- |
| **Adquisición y acondicionamiento de señales EMG de superficie** | Conocemos las bases de electrónica analógica y que se requieren etapas de amplificación y filtrado para limpiar la señal muscular antes de digitalizarla. | Investigar documentación técnica sobre sensores/electrodos EMG de superficie, diseñar el circuito de acondicionamiento y consultar a los docentes para validar la reducción de ruido. |
| **Muestreo en tiempo real y comunicación inalámbrica (BLE / Wi-Fi)** | Tenemos nociones de programación básica de microcontroladores y lectura de entradas analógicas (ADC). | Aprender a configurar la frecuencia de muestreo adecuada en el ADC y el protocolo de transmisión inalámbrica (Bluetooth Low Energy o Wi-Fi) para enviar paquetes sin pérdida de datos. |
| **Arquitectura de software y visualización en tiempo real** | Contamos con fundamentos de programación orientada a objetos (POO) y estructuras de datos básicas. | Aprender a utilizar un framework para el desarrollo de la interfaz (móvil o de escritorio), aplicar patrones de diseño para graficar señales en tiempo real y gestionar el almacenamiento local de sesiones. |
| **Integración del agente de Inteligencia Artificial mediante API** | Sabemos qué tipo de retroalimentación buscamos generar (rehabilitación, fatiga en gimnasio y postura) a partir de las señales adquiridas. | Aprender a consumir una API de IA desde nuestra aplicación, estructurar los datos biomecánicos preprocesados (extracción de características) y definir los prompts o parámetros de evaluación. |
| **Parámetros biomecánicos de fatiga y activación muscular** | Identificamos el problema de la falta de métricas cuantitativas al realizar ejercicios de rehabilitación o entrenamiento de fuerza. | Investigar referencias teóricas sobre electromiografía de superficie y consultar a especialistas o bibliografía en fisioterapia/deporte para calibrar los umbrales de activación y fatiga. |

### 7.3 Distribución inicial de responsabilidades de organización

| Responsabilidad | Integrante(s) | ¿Qué deberá cuidar o verificar? |
| :--- | :--- | :--- |
| **Coordinación** | *Por asignar entre integrantes* | Dar seguimiento a los acuerdos del equipo, ayudar a organizar las actividades semanales y cuidar que se cumplan los tiempos de entrega. |
| **Documentación** | **Carlos Gabriel López Rangel** | Verificar que la información técnica y los documentos generados en el repositorio se encuentren bien estructurados, organizados y actualizados conforme a los requisitos de cada unidad. |
| **Seguimiento en GitHub** | *Por asignar entre integrantes* | Verificar que las tarjetas (Issues y Sub-issues), estados del tablero, enlaces, commits y evidencias de participación del proyecto se mantengan actualizados. |

### 7.4 Acuerdos de trabajo del equipo

- **¿Cómo nos comunicaremos?** Utilizaremos nuestro grupo de WhatsApp para hablar, coordinarnos diariamente y tomar decisiones rápidas, manteniendo disponibilidad habitual entre semana en un horario de 8:00 a.m. a 10:00 p.m., además de platicar en persona durante los horarios de clase en el campus.
- **¿Cómo organizaremos y distribuiremos las actividades?** Cada tarjeta de unidad en GitHub se dividirá en tareas específicas (*Sub-issues*) de acuerdo con los intereses y disponibilidad de cada integrante, registrando al responsable directamente en la plataforma.
- **¿Cómo acordaremos fechas y daremos seguimiento a pendientes?** Definiremos fechas meta internas previas a la entrega oficial de cada unidad y daremos seguimiento a los avances a través del grupo de WhatsApp y el tablero de GitHub.
- **¿Qué haremos cuando un integrante tenga dificultades para cumplir una actividad?** Cuando alguien se atore o no encuentre solución a un problema técnico o de documentación, pedirá apoyo directamente en el grupo para que cualquiera de los compañeros de equipo lo oriente, proponga nuevas ideas o colabore para destrabar la tarea a tiempo.
- **¿Cómo resolveremos diferencias o desacuerdos?** Escuchando las propuestas de cada integrante, evaluando qué opción es más viable técnicamente para el proyecto y, en caso de duda, consultando la opinión de los profesores responsables.
- **¿Cómo revisaremos un trabajo antes de considerarlo terminado?** Antes de cerrar un *Issue* o mover una tarjeta a la columna *Por revisar*, compartiremos el avance con el resto del equipo para verificar conjuntamente que cumple con todos los puntos del *checklist* de la actividad.
- **¿Cómo aseguraremos que todos conozcan las decisiones tomadas?** Todos los acuerdos y cambios importantes se comentarán tanto en el grupo de WhatsApp como en los comentarios de la tarjeta correspondiente en GitHub antes de actualizar el documento principal.
