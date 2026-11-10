# MALEJA-Analisis-FinancieroProyecto de analítica financiera | IX Concurso ITM 2026 |
Plantilla de trabajo para estudiantes. Crea una copia de este archivo en el repositorio de tu equipo y reemplaza los textos entre corchetes. Conserva las preguntas como apoyo durante la investigación. No publiques claves de acceso ni información privada.

Curso: Lenguajes de Programación · Ingeniería Financiera
Concurso: 12 de noviembre de 2026
Simulacro: 10 de noviembre de 2026
Tecnología: Python + Streamlit

1. Identificación del proyecto
Nombre de la aplicación: App financiera MALEJA
Equipo e integrantes: Equipo MALEJA. Mariana Guisao Gomez - Maria Alejandra Guisao Gomez
Enlace a la aplicación: Pendiente de publicación.
Repositorio del proyecto: Pendiente de creación o confirmación.
Última actualización: 2026-11-05
2. ¿Qué queremos investigar? · S25
Investiga: ¿qué significa analizar el comportamiento histórico de un activo financiero? ¿Qué preguntas pueden responderse con datos de mercado y cuáles no?

Situación o fenómeno de interés: Analizar el comportamiento histórico de los precios de tres materias primas negociadas en los mercados internacionales: oro, petróleo WTI y café. Se busca observar sus tendencias, variaciones y niveles de volatilidad durante un período de cinco años.
Pregunta principal: ¿Cómo se ha comportado históricamente el precio del oro, el petróleo WTI y el café entre noviembre de 2021 y noviembre de 2026, y qué diferencias presentan en términos de rendimiento y volatilidad?
Objetivo del análisis: Desarrollar una aplicación financiera en Python que permita consultar, visualizar y comparar los precios históricos del oro, el petróleo WTI y el café, y calcular indicadores que describan su rendimiento y volatilidad.
Importancia financiera: El estudio de las materias primas permite observar cómo cambian sus precios en los mercados, comparar su comportamiento histórico e identificar períodos de mayor variación. Esta información contribuye a comprender características históricas de estos mercados, sin garantizar ni predecir resultados futuros.
Preguntas complementarias: ¿Cuál de los tres commodities presentó mayor volatilidad? ¿Cuál registró el mayor rendimiento acumulado durante el período? ¿En qué fechas se presentaron las variaciones más importantes? ¿Cómo se comparan sus tendencias de precios?
Comprueba: ¿tu pregunta identifica activos, variables y un período de estudio? ¿Es posible responderla con datos disponibles?

3. Activos, datos y alcance · S25
Investiga: ¿qué activos se ajustan a tu pregunta? ¿qué datos históricos existen? ¿qué frecuencia, período y fuente utilizarás?

Activo	Símbolo o ticker	Tipo	Razón para incluirlo
Oro	GC=F	Commodity – metal precioso (futuro)	Se incluye como materia prima de referencia para estudiar la evolución de los metales preciosos.
Petróleo WTI	CL=F	Commodity – energético (futuro)	Se incluye por su importancia en el mercado energético y para comparar su variación con otros commodities.
Café	KC=F	Commodity – agrícola (futuro)	Se incluye para representar el mercado de materias primas agrícolas y contrastar su comportamiento con los metales y la energía.
Fuente de datos: Yahoo Finance, consultada desde Python mediante la biblioteca yfinance. Documentación: https://ranaroussi.github.io/yfinance/.
Período: Del 2021-11-05 al 2026-11-05. La fecha final debe tratarse como límite de consulta; en yfinance, el parámetro end es exclusivo, por lo que se configurará de acuerdo con esa regla para incluir los últimos datos disponibles hasta la fecha de corte.
Frecuencia: Diaria, correspondiente a los días de negociación disponibles para cada contrato.
Variables disponibles: Fecha, apertura (Open), máximo (High), mínimo (Low), cierre (Close) y volumen (Volume), según los campos que entregue la fuente para cada símbolo.
Limitaciones de los datos: Los mercados no necesariamente negocian todos los días y los activos pueden tener calendarios diferentes. Los símbolos corresponden a contratos de futuros; sus series históricas pueden verse afectadas por vencimientos y cambios entre contratos. La disponibilidad, continuidad y calidad de cada serie deben verificarse antes del análisis. yfinance utiliza datos disponibles públicamente en Yahoo Finance y su documentación advierte que la herramienta no está afiliada ni respaldada por Yahoo.
Primera prueba: Pendiente. Se debe ejecutar una descarga de prueba para GC=F, CL=F y KC=F, comprobar que cada serie contiene datos dentro del período y registrar las fechas inicial y final efectivamente recibidas.

4. Metodología de análisis · S25–S26
Investiga: ¿qué indicadores permiten responder la pregunta principal? ¿cómo se calculan? ¿qué interpretación y limitaciones tienen?

Indicador / técnica	¿Qué mide?	¿Por qué lo necesitamos?	Implementación
[Indicador 1]	[Concepto y fórmula, si aplica]	[Relación con la pregunta]	[Archivo o celda]
[Indicador 2]	[Concepto y fórmula, si aplica]	[Justificación]	[Pendiente / enlace]
No es necesario utilizar todos los indicadores estudiados en clase. Selecciona y justifica únicamente los pertinentes.

Visualizaciones previstas
Gráfico	Pregunta que ayuda a responder	Variables	Interpretación esperada
[Gráfico 1]	[Pregunta]	[Variables]	[Qué se podrá observar]
[Gráfico 2]	[Pregunta]	[Variables]	[Qué se podrá comparar]
Primer resultado verificable: [Enlace a un cálculo o gráfico realizado con datos reales y una interpretación breve]

5. Diseño de la aplicación · S25
Investiga: ¿cómo se construyen controles, gráficos y métricas con la herramienta elegida? ¿qué sucede cuando el usuario modifica una selección?

Usuarios previstos: [Quién podría consultar la aplicación]
Entradas y filtros: [Activos, fechas, parámetros...]
Secciones de la interfaz: [Pantalla principal, comparación, riesgo, etc.]
Resultados visibles: [Gráficos, tablas, indicadores y explicaciones]
Interacción principal: [Describe qué cambia cuando el usuario modifica un control]
Flujo previsto:
Selección de activos y parámetros → Obtención de datos → Preparación y cálculos → Visualización → Interpretación.

Boceto o esquema: [Inserta una imagen o enlace al diseño, por ejemplo docs/boceto.png]

Decisión técnica: [¿Por qué usarás Python o R y qué biblioteca de aplicación elegiste?]

6. Construcción y pruebas · S26 (5 de noviembre)
Actualiza esta sección durante el laboratorio de desarrollo.

Componentes implementados: [Qué funciona realmente]
Cómo ejecutar la aplicación: [Comandos, dependencias y pasos]
Dependencias: [Archivo requirements.txt, renv.lock u otro]
Pruebas realizadas: [Caso probado, resultado esperado y resultado obtenido]
Errores conocidos y cómo se resolvieron: [Explicación]
Pendientes antes del simulacro: [Tareas concretas]
No afirmes que una función está implementada si aún no ha sido probada.

7. Hallazgos e interpretación · S26–S28
Para cada hallazgo importante, registra:

Evidencia: [Gráfico, tabla o indicador con enlace]
Qué muestra: [Describe el comportamiento observado]
Interpretación financiera: [Explica su significado en relación con la pregunta]
Limitaciones: [Qué no puedes concluir de los datos]
Conclusión provisional o final: [Respuesta sustentada a la pregunta principal]

Los resultados históricos no garantizan rendimientos futuros.

8. Simulacro · S27 (10 de noviembre)
Guion de sustentación (3–5 minutos):

Problema financiero y activos.
Datos y metodología.
Demostración de interactividad.
Hallazgos e interpretación.
Conclusión y limitaciones.
Retroalimentación recibida: [Observaciones del docente o compañeros]

Ajuste necesario	Responsable	Estado
[Ajuste]	[Integrante]	[Pendiente / en proceso / resuelto]
9. Presentación final · S28 (12 de noviembre)
Enlace funcional de la aplicación: [URL]
Versión final / commit: [Enlace]
Evidencia de presentación: [Enlace autorizado]
Conclusiones finales: [Síntesis]
Limitaciones y posibles mejoras: [Descripción]
10. Bitácora de trabajo y aportes
Fecha	Integrante(s)	Investigación o decisión	Avance técnico / evidencia	Próximo paso
2026-11-03	[Nombre]	[Qué investigamos]	[Enlace a código o documento]	[Acción]
2026-11-05	[Nombre]	[Decisiones]	[Evidencia]	[Acción]
2026-11-10	[Nombre]	[Retroalimentación]	[Cambio]	[Acción]
Recursos de consulta
Libro de programación y analítica financiera del curso
Documentación de yfinance
Documentación de pandas
Documentación de Streamlit
Documentación de Shiny para R
Uso del documento: En S25 desarrolla especialmente las secciones 2 a 5 y registra tu primera prueba; en S26, S27 y S28 actualiza el mismo README. No dupliques información en entregas separadas.
