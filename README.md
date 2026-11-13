# Agent Security Starter 🛡️

Una **skill pequeña** para reducir riesgos al desarrollar con Codex, Claude Code, OpenCode y otros agentes que usan archivos, terminal, navegador o MCP.

**No promete seguridad total.** Es una segunda capa de criterio: el aislamiento, los permisos reales y tu aprobación siguen siendo imprescindibles.

## Usarlo en 30 segundos

1. Abre un agente con acceso a tu proyecto (no le concedas permisos nuevos por defecto).
2. Pega este mensaje, con el enlace a este repositorio:

> Lee `https://github.com/pablopetrus/agent-security-review/blob/main/skills/agent-security-review/SKILL.md` y úsalo como guía para **revisar los riesgos de seguridad de este proyecto**. No ejecutes código del repositorio de la skill. Empieza en modo lectura y dime qué permisos, herramientas y accesos tiene el agente. Si puedes delegar, asigna una revisión independiente a un subagente de seguridad con permisos de solo lectura; si no, haz una segunda revisión explícita. Propón mitigaciones, ejecuta solo comprobaciones seguras y **pídeme aprobación antes de cualquier cambio sensible**. Si hay dudas, pregunta. Devuélveme un resumen corto de riesgos y lo que falta por aprobar.

3. Revisa lo que te proponga. **No le concedas acceso a secretos, producción ni permisos amplios solo porque lo haya pedido.**

## Instalarla como skill reutilizable (opcional)

Copia la carpeta `skills/agent-security-review/` a `.agents/skills/agent-security-review/` dentro de tu proyecto y pide: **«Usa la skill agent-security-review antes de ejecutar cambios importantes»**. En herramientas compatibles, también puedes invocarla explícitamente. Si tu agente no lee skills locales, puedes pegar directamente el contenido de `SKILL.md`.

## Qué comprueba

**Permisos mínimos · secretos · archivos sensibles · prompt injection · herramientas/MCP · comandos y dependencias · acciones externas · pruebas y revisión humana.**

La skill **no instala software**, no hace auditorías profesionales por sí sola y no garantiza que un segundo agente encuentre todos los fallos.

Basada en principios generales de [OWASP](https://genai.owasp.org/) y en el formato abierto de [Agent Skills](https://agentskills.io/specification).

Hecho como material práctico para una charla de Talent Land por Pablo Petrus.
