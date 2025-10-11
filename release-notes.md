# Release Notes — v1.0.0 (2025-10-03)

## Resumen
Lanzamiento inicial de **Plantilla Maestra XSS — Orquestador de payloads, validación y evasión**: un “hub” 100% offline (HTML/JS) que **genera, cataloga y valida** payloads XSS por contexto, con reglas estrictas, perfiles de WAF/CSP/sanitizadores y trazabilidad técnica (fuentes, codificaciones, hash).

## Problema que resuelve
La investigación XSS suele estar dispersa: cheatsheets, blogs, PoCs viejos, listas WAF y notas sueltas. Resultado:
- Lento encontrar **payloads que ejecuten** en el **contexto exacto** (atributo con/sin comillas, href/src, innerHTML, SVG/MathML, JSON-in-HTML…).
- Difícil **versionar** ofuscaciones/codificaciones y **probar evasiones** (CSP/WAF/sanitizadores).
- Duplicación y poca validación (comillas desbalanceadas, etiquetas inválidas).

**La plantilla** unifica todo en un **orquestador offline** con motores/categorías curadas, combinaciones válidas, codificación híbrida x20, perfiles WAF/CSP/sanitizadores, **validación destructiva** y export/import JSON.

## Qué aporta
- 🧭 **Cobertura por contexto** (atributo, HTML plano, JS inline, URLs, SVG/MathML, DOM sinks, JSON embebido, headers/templating).
- ✅ **Matriz whitelist** de etiqueta/atributo/evento (payloads que sí parsean).
- 🧪 **Validación estricta** (JS real ejecutado, comillas/etiquetas correctas, unicidad/hash).
- 🧩 **Perfiles conmutables**: WAF/CSP/sanitizadores para probar bypasses realistas.
- 🧠 **Trazabilidad**: guarda categorías (x1–x20), codificaciones, ofuscación, perfil y fuentes.
- ⚡ **Operativa rápida**: alta/edición masiva, dedupe, contadores, export/import JSON.

## Características destacadas
- **x1–x20** categorías mejoradas (motores, métodos HTTP, caracteres disponibles, contextos, etiquetas, eventos, atributos, combinaciones válidas, técnicas XSS, polimórficos, frameworks, sanitizadores, WAF, backends/ORM, servidor, CSP bypass, ofuscaciones, codificaciones, **x20 híbrida** de especiales, y **#aa fusión total**).
- **Reglas técnicas**: #a (combinar), #aa (fusión total), #* (reutilizar), #** (ofuscar char a char), #0/#00 (omitir/IA libre), **#526+** (mínimo de combinaciones).
- **Validación destructiva** configurable (modo_validación: estricto/flexible/off).
- **Persistencia local** mediante JSON (y localStorage opcional si aplicas parche).

## Uso rápido
1. Abre la herramienta (HTML/JS) en tu navegador (offline).
2. Carga o define tus categorías (x1–x20), activa perfiles WAF/CSP/sanitizador.
3. Elige **modo**:
   - **Automático** (payload_input ≠ "2"): aplica todas las categorías activas y genera `payload_count`.
   - **Manual** (payload_input = "2"): vos indicás cada valor; la plantilla obedece sin añadir ni quitar.
4. Exportá tu catálogo/resultado en JSON; compartí paquetes con tu equipo/lab.

## Handshake (opcional en tu flujo de IA)
Incluye bloque **LLAVE MAESTRA** (“aquilestop”) y reglas de obediencia para sesiones con IA. *Para uso en laboratorio; no afecta la versión HTML/JS base.*

## Roadmap futuro
- Métricas por contexto y por WAF/CSP.
- Generador asistido por IA con vistas comparativas (antes/después de sanitización).
- Reportes de cobertura y diversidad de combinaciones.

## Licencia
MIT — uso responsable y legal únicamente.

---

*"Plantilla Maestra XSS — tu fábrica offline de payloads que sí ejecutan, con rastro completo de su construcción y validación."*
