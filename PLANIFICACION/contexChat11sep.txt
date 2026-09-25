# RESUMEN Y CONTEXTO CONSOLIDADO DE LA SESIÓN DE TRABAJO
**Fecha de Ejecución:** 11 de Septiembre de 2026  
**Proyecto de Titulación:** Desarrollo de un sistema informático de gestión clínica optométrica utilizando la metodología ágil Scrum, garantizando la seguridad de los datos de salud visual (SGO)  
**Institución Académica:** Escuela Superior Politécnica de Chimborazo (ESPOCH) — Facultad de Informática y Electrónica — Carrera de Software  
**Autores / Investigadores:** Omar Santiago Figueroa Díaz & Alexander Rafael Villalva Dumancela  
**Director / Scrum Master:** Ing. Jorge Ariel Menéndez Verdecia  
**Revisión Técnica / Asesoría:** Ing. Julio Roberto Santillán Castillo  
**Entorno de Aplicación:** Óptica de estudio (Riobamba, Provincia de Chimborazo, Ecuador)  
**Ubicación del Archivo:** `DESARROLLO_SGO/PLANIFICACION/contexChat11sep.txt` (y `contexChat11sep.md`)  

---

## 1. PROPÓSITO GENERAL DE LA SESIÓN

Durante la presente sesión de trabajo se ejecutó de forma secuencial, rigurosa y metodológica la ingeniería de requisitos del sistema SGO, articulando la investigación de campo, la auditoría forense del software legado en uso, los requerimientos de la ESPOCH y los estándares internacionales de calidad y modelado (**IEEE Std 830-1998**, **ISO/IEC 25010:2023**, **UML 2.5** y **Secure Scrum**).

Se transitó de manera continua desde la teoría de Casos de Uso, pasando por la planificación metodológica del proceso de requisitos, la ejecución de la Fase 1 (Elicitación), la definición formal del Alcance bajo la metodología de 5 pasos, la ejecución de la Fase 2 (Análisis y Negociación), hasta culminar en la ejecución de la Fase 3 (Especificación Formal y Modelado de Casos de Uso).

---

## 2. EVOLUCIÓN CRONOLÓGICA DE SOLICITUDES Y ENTREGABLES

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        FLUJO DE TRABAJO EJECUTADO EN LA SESIÓN                         │
└────────────────────────────────────────────────────────────────────────────────────────┘
                                           │
  ┌────────────────────────────────────────┼────────────────────────────────────────┐
  ▼                                        ▼                                        ▼
[SOLICITUD 1]                            [SOLICITUD 2]                            [SOLICITUD 3]
Teoría Casos de Uso                      Plan de Requisitos                       Ejecución Fase 1
(Unidad II_Rq_2)                         (IEEE 830 + Scrum)                       (Elicitación)
      │                                        │                                        │
      ▼                                        ▼                                        ▼
CasosUsoTeoria.txt                       plaDesarrolloRequisitos.txt              informeFase1.txt
                                                                                        │
  ┌─────────────────────────────────────────────────────────────────────────────────────┘
  ▼
[SOLICITUD 4]                            [SOLICITUD 5]                            [SOLICITUD 6]
Construir Alcance                        Ejecución Fase 2                         Ejecución Fase 3
(ALCANCE PDF + instruccion)              (Análisis y Negociación)                 (Especificación y CUS)
      │                                        │                                        │
      ▼                                        ▼                                        ▼
Alcance.txt                              informeFase2.txt                         informeFase3.txt
```

### Solicitud 1: Extracción de Teoría de Casos de Uso
- **Petición del Usuario:** Revisar el directorio `CASOS DE USO`, extraer del documento `Unidad II_Rq_2_CASOS_USO.pdf` la teoría pertinente para la elaboración de Casos de Uso respecto al Anteproyecto de Titulación, y almacenar `CasosUsoTeoria.txt` en el mismo directorio.
- **Acciones Realizadas:**
  * Análisis de las 43 diapositivas del PDF: distinción Casos de Uso del Negocio (CUN) vs. Casos de Uso del Sistema (CUS), concepto de "Caja Negra", resultado observable de valor, métodos de identificación (por actores y por eventos), relaciones UML (`<<include>>`, `<<extend>>`, generalización), descomposición en paquetes/subsistemas y plantillas de especificación textual.
  * Contextualización directa con el proyecto SGO de Óptica de estudio, los 5 módulos MVP y las subcaracterísticas de seguridad ISO/IEC 25010:2023.
- **Entregable Generado:** `DESARROLLO_SGO/CASOS DE USO/CasosUsoTeoria.txt` (31,230 bytes).

---

### Solicitud 2: Plan por Fases para el Desarrollo de Requisitos
- **Petición del Usuario:** Teniendo en cuenta `informeEntrevistasConsolidado.txt`, `Especificacion de Requisitos_01.txt`, el Anteproyecto y `Orden_Metodologico_Implementacion_Sistema.txt`, generar un plan por fases para el desarrollo de requisitos y almacenarlo como `plaDesarrolloRequisitos.txt` en `REQUERIMENTACION`.
- **Acciones Realizadas:**
  * Estructuración del ciclo de ingeniería de requisitos conforme a IEEE Std 830-1998, ISO/IEC/IEEE 29148:2018 y Secure Scrum (Pohl y Hof, 2015).
  * Formulación de 5 fases secuenciales e iterativas:
    1. Fase 1: Elicitación y Levantamiento de Requisitos.
    2. Fase 2: Análisis, Refinamiento y Negociación de Alcance.
    3. Fase 3: Especificación y Modelado Formal de Requisitos.
    4. Fase 4: Verificación, Validación y Gestión de Calidad.
    5. Fase 5: Gestión del Cambio y Transición al Product Backlog de Scrum.
  * Definición de Matriz RACI, cronograma sugerido y articulación con las etapas posteriores (MER, Arquitectura, Sprints).
- **Entregable Generado:** `DESARROLLO_SGO/REQUERIMENTACION/plaDesarrolloRequisitos.txt` (28,889 bytes).

---

### Solicitud 3: Ejecución de la Fase 1 (Elicitación y Levantamiento)
- **Petición del Usuario:** Ejecutar la Fase 1, generar `informeFase1.txt`, almacenarlo en el directorio `fase1`, validar la completitud de la información para la fase siguiente o solicitar mayor contexto.
- **Acciones Realizadas:**
  * Análisis cruzado de las 3 entrevistas técnicas de relevamiento (Entrevista 1 exploratoria, Entrevista demostrativa del sistema legado, Entrevista 2 estructurada con el Product Owner y asesores de la ESPOCH).
  * Diagnóstico forense del sistema legado: interfaz MDI obsoleta, sobreescritura destructiva de refracciones históricas (`UPDATE` ciego), ausencia total de pistas de auditoría (no repudio nulo) y dependencia bloqueante de servicios web externos.
  * Modelado de 5 flujos de negocio AS-IS (Recepción/filiación, Consulta/refracción OD-OS, Pedidos a talleres de Quito/Guayaquil, Cobros/anticipos y Cierre diario de caja).
  * Catálogo de 28 Requisitos Funcionales brutos, requisitos de seguridad ISO/IEC 25010 y catálogo inicial de S-Tags ([`S-TAG-AUTH`], [`S-TAG-INT`], [`S-TAG-RES`]).
  * Evaluación de completitud: Diagnóstico de suficiencia técnica positivo (100% de criterios de entrada cumplidos) y planteamiento de 3 puntos de afinamiento (umbral dióptrico $\ge 1.50$ D, permisos de papelera lógica y formato de recibo térmico de 80 mm).
- **Entregable Generado:** `DESARROLLO_SGO/REQUERIMENTACION/fase1/informeFase1.txt` (34,645 bytes) y espejo en `DESARROLLO_SGO/fase1/informeFase1.txt`.

---

### Solicitud 4: Construcción del Alcance del Proyecto (Paso Previo a Fase 2)
- **Petición del Usuario:** Antes de ejecutar la Fase 2, desarrollar lo solicitado en `REQUERIMENTACION/fase2/instruccion.txt`, basándose en el documento `ALCANCE DE UN PROYECTO.pdf`, y almacenar `Alcance.txt` en el directorio `fase2`.
- **Acciones Realizadas:**
  * Implementación del marco teórico de 5 pasos de `ALCANCE DE UN PROYECTO.pdf`:
    1. *Definir las necesidades:* Justificación del problema clínico, resultados entregables (PWA, PostgreSQL, Audit Log) y marco normativo (LOPDP y Acuerdo MSP 30-2020).
    2. *Proyectar objetivos S.M.A.R.T.:* Formulación estratégica basada en el Anteproyecto con metas medibles (100% de 23 RF, 0 sobreescrituras, < 1.5s de respuesta).
    3. *Describir actividades:* Desglose funcional en tareas y acciones para los 5 módulos del MVP y tareas transversales de seguridad.
    4. *Analizar capacidades:* Evaluación de competencias de Omar Figueroa (Backend/PostgreSQL/Seguridad), Alexander Villalva (Frontend/React/UX), tutores y viabilidad de autofinanciamiento Open Source.
    5. *Entender limitaciones y riesgos:* Plazo rígido de 16 semanas, exclusión justificada de factores externos (SRI y WhatsApp) y matriz de mitigación de riesgos.
  * Enunciado canónico del alcance formal delimitando lo que está DENTRO (*In-Scope*) vs. FUERA (*Out-of-Scope*).
- **Entregable Generado:** `DESARROLLO_SGO/REQUERIMENTACION/fase2/Alcance.txt` (28,164 bytes) y espejo en `DESARROLLO_SGO/fase2/Alcance.txt`.

---

### Solicitud 5: Ejecución de la Fase 2 (Análisis, Refinamiento y Negociación)
- **Petición del Usuario:** Ejecutar la Fase 2, generar `informeFase2.txt` y almacenarlo en el directorio `fase2`.
- **Acciones Realizadas:**
  * Análisis de los 17 procesos del negocio optométrico y filtrado sistemático hacia los **5 Módulos Nucleares del MVP** (M1: Usuarios, M2: Pacientes, M3: Historia Clínica, M4: Pedidos a Taller, M5: Ventas/Cobros).
  * Exclusión técnica justificada y catalogación formal de requerimientos futuros:
    - `RF-FUT-01`: Facturación Electrónica WebService SRI (riesgo burocrático y caídas de servicio).
    - `RF-FUT-02`: Notificaciones automáticas por WhatsApp API (costo Meta en dólares y riesgo de bloqueo).
    - `RF-FUT-03`: Migración masiva ETL de la base de datos legada corrupta (riesgo de contaminar PostgreSQL; se adopta migración manual bajo demanda).
    - `RF-FUT-04`: Módulo de agenda y citas web interactivas.
    - `RF-FUT-05`: Pasarelas de pago web en línea (Stripe/Datafast).
  * Formalización y normalización de Reglas de Negocio:
    - *Clínicas (`RN-CLI`):* Adición siempre (+); notación cilíndrica negativa obligatoria $[-0.25, -10.00]$ D; pasos de $0.25$ D; eje angular $[0^\circ, 180^\circ]$; escala Snellen en pies; alerta de salto dióptrico atípico ante variaciones $\ge 1.50$ D.
    - *Operativas (`RN-OPE`):* Flexibilidad pediátrica; inventario de armazones por lotes de precio uniforme; y aislamiento de privacidad en órdenes de taller (LOPDP).
    - *Seguridad (`RN-SEG`):* Prohibición de sobreescritura de graduaciones; borrado lógico (*Soft Delete*); pistas inmutables de auditoría (*Audit Log*); y control RBAC.
  * Resolución formal de las 3 consultas de la Fase 1 (alerta fijada en $1.50$ D; papelera exclusiva de Administrador; impresión en ticket térmico de 80 mm y PDF).
  * Priorización MoSCoW: 19 *Must Have* (82.6%), 3 *Should Have* (13.0%), 1 *Could Have* (4.4%) y 5 *Won't Have*.
- **Entregable Generado:** `DESARROLLO_SGO/REQUERIMENTACION/fase2/informeFase2.txt` (31,253 bytes) y espejo en `DESARROLLO_SGO/fase2/informeFase2.txt`.

---

### Solicitud 6: Ejecución de la Fase 3 (Especificación y Modelado Formal de Casos de Uso)
- **Petición del Usuario:** En base a los documentos generados y la documentación pertinente, ejecutar la Fase 3, generar `informeFase3.txt` y almacenarlo en el directorio `fase3`.
- **Acciones Realizadas:**
  * Especificación técnica exhaustiva bajo IEEE Std 830-1998 de los **23 Requisitos Funcionales Nucleares (`RF-01` a `RF-23`)** con códigos, prioridades MoSCoW, precondiciones, entradas, reglas detalladas de procesamiento, salidas, postcondiciones y S-Tags asociados.
  * Especificación formal de Requisitos No Funcionales bajo **ISO/IEC 25010:2023**:
    - *Autenticidad (`RNF-SEG-01`):* Hashing bcrypt (costo $\ge 12$), tokens JWT firmados y expiración tras 20 min de inactividad.
    - *Integridad (`RNF-SEG-02`):* Validación dual cliente/servidor, restricciones `CHECK` en PostgreSQL y transaccionalidad ACID.
    - *Responsabilidad (`RNF-SEG-03`):* Bitácora inmutable `audit_logs` que captura timestamp UTC, usuario, IP, tipo de evento y diferencias de datos en formato JSONB.
    - *Rendimiento y Disponibilidad (`RNF-REN-01`, `RNF-DIS-01`):* Respuesta $< 1.5$ s y disponibilidad 99.5% autónoma en red local LAN.
    - *Usabilidad y Cumplimiento (`RNF-USA-01`, `RNF-LEG-01`):* PWA reactiva sin ventanas flotantes MDI y apego irrestricto a la LOPDP.
  * Modelado formal de Casos de Uso en UML:
    - Definición de los 5 Actores (`ACT-01: Admin`, `ACT-02: Optometrista`, `ACT-03: Asistente`, `ACT-EXT-01: Taller Externo`, `ACT-NEG-01: Paciente`).
    - Estructuración en 5 Subsistemas/Paquetes (`<<subsystem>>`).
    - Diagramas conceptuales de arquitectura de casos de uso en texto estructurado.
    - Modelado de relaciones de inclusión (`<<include>>`: Validar Rangos Dióptricos, Validar Cédula, Registrar Log de Auditoría).
    - Modelado de relaciones de extensión (`<<extend>>`: Alerta de Salto Atípico $\ge 1.50$ D, Medidas Progresivos, Rectificación por Garantía, Cobro de Anticipos y Anulación Justificada).
  * Fichas textuales paso a paso de interacción actor $\leftrightarrow$ sistema para los casos nucleares `CUS-01`, `CUS-05`, `CUS-10`, `CUS-15` y `CUS-19`.
  * Matriz de Trazabilidad Integral Bidireccional vinculando los 23 RF con sus Casos de Uso, S-Tags y subcaracterísticas ISO 25010.
- **Entregable Generado:** `DESARROLLO_SGO/REQUERIMENTACION/fase3/informeFase3.txt` (53,268 bytes) y espejo en `DESARROLLO_SGO/fase3/informeFase3.txt`.

---

## 3. INVENTARIO COMPLETO DE ARTEFACTOS GENERADOS

| # | ARTEFACTO / ARCHIVO | DIRECTORIO DE ALMACENAMIENTO | TAMAÑO | PROPÓSITO / DESCRIPCIÓN TÉCNICA |
|---|---------------------|------------------------------|--------|----------------------------------|
| 1 | `CasosUsoTeoria.txt` | `DESARROLLO_SGO/CASOS DE USO/` | 31.2 KB | Guía metodológica y base teórica de Casos de Uso UML adaptada al SGO. |
| 2 | `plaDesarrolloRequisitos.txt` | `DESARROLLO_SGO/REQUERIMENTACION/` | 28.9 KB | Plan maestro de 5 fases para el desarrollo de requisitos (IEEE 830 / Scrum). |
| 3 | `informeFase1.txt` | `DESARROLLO_SGO/REQUERIMENTACION/fase1/`<br>*(Espejo: `DESARROLLO_SGO/fase1/`)* | 34.6 KB | Informe de Elicitación: auditoría forense del sistema legado, flujos AS-IS y RF brutos. |
| 4 | `Alcance.txt` | `DESARROLLO_SGO/REQUERIMENTACION/fase2/`<br>*(Espejo: `DESARROLLO_SGO/fase2/`)* | 28.2 KB | Documento formal de Alcance basado en los 5 pasos de `ALCANCE DE UN PROYECTO.pdf`. |
| 5 | `informeFase2.txt` | `DESARROLLO_SGO/REQUERIMENTACION/fase2/`<br>*(Espejo: `DESARROLLO_SGO/fase2/`)* | 31.3 KB | Informe de Análisis y Negociación: filtrado a 5 módulos MVP, exclusión SRI y reglas de negocio. |
| 6 | `informeFase3.txt` | `DESARROLLO_SGO/REQUERIMENTACION/fase3/`<br>*(Espejo: `DESARROLLO_SGO/fase3/`)* | 53.3 KB | Informe de Especificación Formal: 23 RF detallados, RNF ISO 25010, Casos de Uso UML y S-Tags. |
| 7 | `contexChat11sep.txt`<br>`contexChat11sep.md` | `DESARROLLO_SGO/PLANIFICACION/` | ~15 KB | Resumen y memoria técnica consolidada de la sesión de trabajo del 11/09/2026. |

---

## 4. DECISIONES CLAVE Y ACUERDOS TÉCNICOS CONSOLIDADOS

1. **Stack Tecnológico Definitivo:**
   - *Backend:* PHP 8.2+ con Laravel 10/11 (Arquitectura modular en capas, robustez y madurez).
   - *Frontend:* React 18+ con Vite y TailwindCSS (SPA / PWA reactiva, ergonómica y rápida).
   - *Base de Datos:* PostgreSQL 15+ (Garantía de integridad referencial, transaccionalidad ACID y soporte JSONB para auditoría).
   - *Despliegue:* Operación autónoma en red local (LAN/WLAN) de la óptica y entorno de pruebas en Google Cloud Platform (GCP).

2. **Alcance del MVP (5 Módulos Nucleares):**
   - M1: Autenticación y Gestión de Usuarios (RBAC: Admin, Optometrista, Asistente; JWT; sesiones acotadas).
   - M2: Gestión de Pacientes (Registro demográfico, validación módulo 10 de cédula, flexibilidad pediátrica y adjuntos).
   - M3: Historia Clínica y Graduación (Refracción OD/OS, dioptrías validadas, adición siempre positiva, Snellen en pies, CIE-10, inmutabilidad y Soft Delete).
   - M4: Pedidos al Laboratorio Óptico (Órdenes técnicas aisladas sin exponer diagnósticos personales LOPDP, máquina de estados y rectificaciones).
   - M5: Ventas y Cobros (Lotes de armazones sin serial único, pagos mixtos efectivo/transferencia, anticipos/saldos, recibos térmicos de 80 mm y cuadre diario de caja).

3. **Exclusiones Conscientes de Riesgo:**
   - La facturación electrónica SRI (`RF-FUT-01`), WhatsApp API (`RF-FUT-02`) y la migración masiva de la BD legada (`RF-FUT-03`) quedan formalmente excluidas del MVP para asegurar la continuidad de los Sprints y evitar parálisis operativas.

4. **Pilares de Seguridad y Calidad (ISO/IEC 25010:2023):**
   - *Autenticidad ([S-TAG-AUTH]):* Verificación estricta de identidad y roles en cada endpoint.
   - *Integridad ([S-TAG-INT]):* Eliminación total de la sobreescritura destructiva de refracciones; validaciones matemáticas duales en dioptrías.
   - *Responsabilidad ([S-TAG-RES]):* Registro inmutable de auditoría forense (*Audit Log*) para no repudio legal.

---

## 5. ESTADO ACTUAL Y PRÓXIMOS PASOS METODOLÓGICOS

### Estado Actual:
Las **Fases 1, 2 y 3** de la Ingeniería de Requisitos se encuentran **100% concluidas, aprobadas y documentadas**.

### Próximos Pasos (Conforme a `plaDesarrolloRequisitos.txt` y `Orden_Metodologico_Implementacion_Sistema.txt`):
1. **Ejecución de la Fase 4: Verificación, Validación y Gestión de Calidad de Requisitos**:
   - Conducción de las Revisiones Técnicas Formales (FBR) con el Director de Titulación (Ing. Jorge Menéndez) y Asesor Metodológico (Ing. Julio Santillán).
   - Sesión de validación final (walkthrough) y firma de actas de aprobación con el Product Owner / Propietario de Óptica de estudio.
2. **Ejecución de la Fase 5: Transición Metodológica al Entorno Scrum**:
   - Transformación de los 23 Requisitos Funcionales en Historias de Usuario con sintaxis formal (*Como / Quiero / Para*).
   - Formulación de Criterios de Aceptación bajo el estándar Gherkin (*Dado que / Cuando / Entonces*).
   - Construcción del **Product Backlog Inicial** y **Security Backlog** priorizado.
   - Formalización de la **Security Definition of Done (DoD)**.
3. **Inicio de las Fases Subsiguientes del Orden Metodológico de Implementación**:
   - Modelado del **Modelo Entidad-Relación (MER)** y esquema de base de datos relacional en PostgreSQL.
   - Diseño del **Diagrama de Arquitectura de Software** en capas y APIs.
   - Elaboración del **Esquema de Navegación del Sistema** y prototipado UI.
   - Planificación de los Sprints en el Cronograma de Titulación.

---
*Memoria técnica registrada y consolidada para el expediente académico del Trabajo de Titulación — ESPOCH 2026.*
