# EstéticIA

Aprendizaje, simulación clínica y evaluación adaptativa en Medicina Estética. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/esteticia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24175185.svg)](https://doi.org/10.5281/zenodo.24175185)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Entorno de estudio para el **Máster de Formación Permanente en Medicina Estética Integral y Antienvejecimiento** (UMH). Recorre sus 11 asignaturas (60 ECTS) con estos módulos:

- **Asignaturas y objetivos**: las 11 asignaturas con sus créditos, cuatro ideas clave por asignatura y los 13 objetivos específicos de la ficha del máster. Mapa de 17 competencias en 6 dimensiones, enlazadas con los resultados COM1–COM8 de la ficha.
- **Laboratorio de fisiología cutánea**: modelo cualitativo y determinista del envejecimiento de la piel (edad, radiación ultravioleta, fotoprotección, tabaco, estrógenos, retinoide) con corte de piel ilustrado; modos aprendizaje, experimentación, desafío de predicción y evaluación.
- **Laboratorio de diagnóstico**: atlas de 9 zonas de riesgo facial sobre un esquema propio clicable (reto y exploración), dermatoscopia con la regla ABCD de Stolz sobre lesiones generadas por semilla, escalas clínicas (Fitzpatrick, Glogau, celulitis, lista de tres puntos) y esquemas de ecografía facial (ácido hialurónico, hidroxiapatita, silicona, vasos con Doppler, hilos, hueso).
- **7 calculadoras clínicas** con la fórmula paso a paso: reconstitución de toxina botulínica, dosis máxima de anestésico local, fluencia láser y orientación por fototipo, fuerza centrífuga relativa y factor de concentración del plasma rico en plaquetas, diluciones, regla ABCD e índices corporales.
- **Problemas con solución calculada** (7 tipos): cada variante sale de una semilla; si la respuesta no coincide, el código la recalcula con los errores típicos y dice cuál se ha cometido.
- **9 pacientes virtuales de 10 estados** (presentación, anamnesis, exploración, pruebas, interpretación, diferencial, diagnóstico, conducta, evolución, razonamiento): la paciente evoluciona según la decisión y un **error crítico no se compensa** (el caso no pasa de 40 %).
- **Seguridad y prácticas**: 6 simulacros de complicaciones con decisiones encadenadas (oclusión vascular, pérdida de visión, anafilaxia, ptosis, síncope, quemadura); tabla comparativa de rellenos y bioestimuladores; **pasaporte de prácticas** con las 7 prácticas en clínica y los 6 talleres de la ficha, lista de preparación y reflexión posterior.
- **6 estaciones ECOE** escritas con lista ponderada y errores críticos; modos libre, cronometrado y simulacro; autoevaluación, evaluación docente o comentario de la IA con cita comprobada.
- **Simulacro tipo test**: 55 preguntas (5 por asignatura) con explicación inmediata, por bloque o asignatura, y repaso de falladas.
- **Tutor de IA** con contexto docente (competencia de trabajo, errores recurrentes), seis modos.
- **Mi progreso**: perfil de competencias, recomendaciones explicadas y repaso espaciado; informe en Word, copia JSON y exportación seudonimizada para el profesorado.
- **Panel del profesorado**: importa los JSON del alumnado, analiza competencias e ítems, configura ECOE y registra qué contenidos ha validado.

Funciona sin clave y sin conexión salvo el tutor y los comentarios de IA.

## Estado del contenido

La ficha pública del máster indica asignaturas, créditos, objetivos, competencias y prácticas, pero **no el temario de cada asignatura ni su evaluación**. Todo el contenido clínico (ideas clave, preguntas, casos, estaciones, complicaciones, modelo de piel, esquemas) lo ha redactado el equipo autor. Los dibujos son esquemas docentes propios, no imágenes de pacientes.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. No hace falta servidor. La IA no calcula ni puntúa: el código comprueba que cada cita que atribuye al estudiante aparece literalmente en su texto, descarta elementos inventados, marca cifras y referencias no comprobadas y retira cualquier nota. La IA nunca cambia el perfil de competencias.

## Privacidad

El progreso, las respuestas, la clave y las notas del pasaporte se guardan solo en este navegador. Solo si se piden comentarios a la IA sale hacia el proveedor el caso y el texto escrito, con correos, DNI y teléfonos enmascarados; antes del primer envío se muestra la muestra. La exportación para el profesorado lleva seudónimo y evidencias numéricas, sin textos libres, sin notas del pasaporte y sin clave. Para investigar con esos datos hacen falta comité de ética (OEP en la UMH) y consentimiento informado.

## Límites

Material de estudio para médicos en formación. No sustituye a las clases, a las fichas técnicas, a los protocolos escritos de cada consulta ni al juicio clínico. Las calculadoras no deben usarse para decidir sobre pacientes reales; las dosis de anestésico son orientativas y las unidades de toxina no son intercambiables entre productos. El simulacro no reproduce ningún examen oficial. El modelo de piel es cualitativo: direcciones de cambio, no medidas.

## Accesibilidad y pruebas

Sin infracciones WCAG 2.2 AA (axe-core) en las 13 pantallas y los tres idiomas; navegable con teclado; primera pantalla útil en menos de 3 s con la CPU ralentizada ×4 en móvil. Pruebas: `node tests/test_logica.js`, `node tests/test_competencias.js`, `python3 tests/smoke.py`, `python3 tests/a11y.py`.

## Adaptación a otro máster

El currículo es datos: `src/datos.js` (asignaturas, ideas clave, objetivos), `src/preguntas.js`, `src/casos.js`, `src/ecoe.js` y `src/seg.js`. Cambiando esos ficheros y ejecutando `python3 build.py` se obtiene otra app con el mismo motor.

## Autoría

Roles (CRediT): Fernando Borrás Rocher — conceptualización, software, redacción del contenido; Elena Caride Miana — conceptualización, recursos, validación del contenido clínico.


Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Elena Caride Miana (Dra. Caride Medicina Estética & Antiaging).

Construida a partir de la ficha pública del Máster de Formación Permanente en Medicina Estética Integral y Antienvejecimiento (UMH), del que Elena Caride Miana es codirectora.

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Elena Caride Miana [0000-0002-7620-4857](https://orcid.org/0000-0002-7620-4857)

## Cómo citar

Borrás Rocher, F. y Caride Miana, E. (2026). *EstéticIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.24175185](https://doi.org/10.5281/zenodo.24175185)

## Licencia

MIT. El motor adaptativo, de casos, ECOE, tutor y panel está adaptado de NefrIA (Borrás Rocher y Gómez Pérez, MIT). MIT es una licencia de software; para los contenidos docentes lo habitual sería CC BY 4.0, a decidir por los autores. Véase [LICENSE](LICENSE).
