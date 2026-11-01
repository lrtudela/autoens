# Autoevaluación ENS para pymes (nombre provisional)

Herramienta web de autoevaluación de ciberseguridad para pymes, basada en el ENS (categoría básica). El usuario responde un cuestionario y recibe un informe de brechas y un plan de 90 días. Es una pieza de portfolio de Luis para entrevistas de Solutions Engineer: cualquiera debe poder abrirla y usarla sin cuentas ni instalación.

## Estado

Todavía no hay código. Se están tomando decisiones en conversaciones con Claude (chat), y el resultado vive en `docs/`. No decidas por tu cuenta lo que esté como pendiente en `docs/00 Indice.md`: pregunta.

## Reglas que no hay que deshacer

- Sin IA en ejecución. Ninguna llamada de red a APIs de IA, ni servidor ni claves. Las puntuaciones y el plan salen de reglas fijas y reproducibles; los textos del informe salen de una biblioteca de textos escrita de antemano y revisada por Luis. Los datos del usuario no salen del navegador.
- Un solo banco de preguntas con dos modos (rápido y completo) y un mini-filtro de categorización al empezar.
- El informe es un diagnóstico orientativo y lo dice. No hables de certificación ni de cumplimiento legal.
- Nada normativo se afirma sin contrastarlo con la fuente oficial (ver la nota «Datos normativos por verificar»).
- Estética corporativa sobria. NO retro, aunque Luis suele preferir interfaces retro: en este proyecto no apliques la skill interfaces-retro.
- Interfaz en español; código (variables, funciones) en inglés.
- Stack: por decidir. Antes de elegir, propón a Luis las opciones; la preferencia general es la solución más simple, sin dependencias ni build si basta.

## Cómo trabajar aquí

- Piensa antes de programar. Si dudas, pregunta; si hay dos caminos, enséñalos antes de elegir.
- Mínimo código que resuelva el problema. Sin funciones, configuración ni abstracciones que no se hayan pedido. Si ves una mejora, propónla en una línea y espera.
- Cambios quirúrgicos: toca solo lo necesario y no reformatees ni reorganices lo que funciona.
- Define el criterio de éxito antes de empezar y no des nada por terminado hasta comprobarlo.

## Pendiente y decisiones

Viven en `docs/`, que Luis abre como vault de Obsidian. Antes de trabajar lee `docs/00 Indice.md`. Cada problema, mejora y decisión es una nota con las propiedades `tipo`, `prioridad`, `estado` y `coste`, y con un criterio de éxito comprobable. Al terminar algo, cambia `estado` a `hecho` en su nota; si es un problema, muévela a `docs/problemas/resueltos/` y pasa su enlace a «Resuelto (historial)» en el índice. No la borres. Si creas una nota, enlázala en el índice. No añadas pendientes a este archivo y no edites `docs/Tablero.canvas` ni `docs/.obsidian/`.

`docs/` no se publica: está en `.gitignore`. No lo añadas a ningún commit ni lo saques del `.gitignore`. Al subir cambios, añade solo los archivos que corresponden al código y a la documentación pública.
