Materias: Taller de Desarrollo de Tecnologías de la Automatización (TDTA) y Programación Avanzada
Docente(s) responsable(s):
• Marcos Romo Avilés
• Adriana Rojas Molina
Integrantes del equipo:
1. Ian Carlo Aguilar Vázquez
2. Victor Ortigosa Coral
3. Ezequiel Gil Guerrero Patiño
4. Carlos Gabriel López Rangel
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
* Atiende una necesidad real y vigente tanto en el ámbito clínico como en el deportivo.
* Sienta las bases para el desarrollo de dispositivos wearable de bajo costo con capacidades de análisis inteligente, un área en creciente expansión dentro de la ingeniería biomédica y la salud digital.

---

## 3. OBJETIVOS

### 3.1 Objetivo General
Diseñar, desarrollar e implementar un sistema embebido de adquisición de señales electromiográficas (EMG) integrado con una aplicación de software orientada a objetos y un agente de inteligencia artificial, capaz de apoyar procesos de rehabilitación física, evaluación de rendimiento en el gimnasio y corrección de postura mediante el análisis en tiempo real de la actividad muscular.

### 3.2 Objetivos Específicos

**Automatización y Hardware (TDTA)**
* Seleccionar e integrar un microcontrolador con conversor analógico-digital (ADC) apto para el muestreo de señales biomecánicas en tiempo real.
* Implementar el módulo de comunicación inalámbrica (Bluetooth Low Energy o Wi-Fi) para la transmisión de datos hacia la aplicación cliente.
* Desarrollar el firmware embebido para la sincronización, muestreo y empaquetado de datos provenientes de múltiples canales EMG.
* Validar experimentalmente la fidelidad y el nivel de ruido de la señal adquirida, comparando contra referencias teóricas de electromiografía de superficie.

**Software Avanzado e Inteligencia Artificial**
* Diseñar la arquitectura de software de la aplicación móvil, aplicando patrones de diseño adecuados para el manejo de datos en tiempo real.
* Implementar los módulos de recepción, almacenamiento y visualización de señales EMG mediante estructuras de datos eficientes.
* Integrar, mediante API, un agente de inteligencia artificial capaz de procesar los datos biomecánicos y generar retroalimentación contextual para rehabilitación, entrenamiento y postura.
* Desarrollar los módulos funcionales de la aplicación: seguimiento de rehabilitación, evaluación de fatiga/rendimiento en el gimnasio y corrección postural.
* Implementar pruebas unitarias y de integración que garanticen la robustez, escalabilidad y mantenibilidad del software desarrollado.

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
* Requisito no funcional: la aplicación debe ejecutarse en al menos una plataforma (Windows, Android o multiplataforma) con interfaz de usuario intuitiva.
* Requisito no funcional: el sistema debe permitir la operación continua durante sesiones de al menos 30 minutos sin pérdida significativa de datos.
* Requisito de seguridad: los datos biométricos del usuario deben almacenarse de forma local o cifrada, respetando principios básicos de privacidad de datos de salud.

> **NOTA IMPORTANTE:** MyoTrack Al es una herramienta de apoyo académico y de acondicionamiento físico. No sustituye el diagnóstico, tratamiento o supervisión de un profesional certificado de la salud.

---

## 5. METODOLOGÍA DE DESARROLLO Y CRONOGRAMA

### 5.1 Fases del proyecto
* **Diseño:** análisis de requisitos, investigación de componentes y definición de arquitectura general del sistema.
* **Prototipado:** construcción del circuito de acondicionamiento de señal, integración de electrodos y pruebas iniciales de adquisición.
* **Programación:** desarrollo del firmware embebido y de la aplicación de software, incluyendo la integración del agente de IA.
* **Pruebas y validación:** verificación funcional, pruebas con usuarios piloto, calibración de umbrales y ajuste de algoritmos de evaluación.

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
* Aplicación integral de conocimientos de instrumentación electrónica, procesamiento digital de señales y sistemas embebidos.
* Fortalecimiento de competencias en arquitectura de software, patrones de diseño e inteligencia artificial mediante API.
* Desarrollo de habilidades de trabajo interdisciplinario entre hardware y software, replicando condiciones reales de la industria biomédica y tecnológica.

### 6.2 Beneficios prácticos y sociales
* Aporte de una herramienta accesible y de bajo costo para el monitoreo objetivo de procesos de rehabilitación física.
* Apoyo a la prevención de lesiones deportivas mediante la detección temprana de fatiga muscular y desviaciones posturales.
* Sentado de las bases técnicas para futuras versiones del sistema con mayor número de canales, algoritmos de IA más sofisticados y validación clínica formal.

