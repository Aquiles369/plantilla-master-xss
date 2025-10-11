# Changelog

Todas las versiones siguen el formato [SemVer].

## [v1.0.0] - 2025-10-03
### Añadido
- **Plantilla Maestra XSS — Orquestador de payloads, validación y evasión**.
- Stack 100% offline (HTML/JS). Visor/gestor local con categorías, CRUD, búsqueda, contadores, alta masiva y exportación/importación JSON.
- Cobertura multi-contexto: **HTML/JS/URL/SVG/MathML/DOM**, JSON embebido, headers reflejados y sinks de DOM.
- **Matriz de combinaciones válidas** etiqueta/atributo/evento (whitelist) para minimizar falsos positivos.
- **Perfiles** alternables: WAF (Cloudflare, Imperva, ModSecurity CRS, F5 ASM, etc.), **CSP**, y **sanitizadores** (DOMPurify, OWASP Java, Jsoup, Bleach, HTMLPurifier…).
- **Codificación híbrida x20** de especiales + **ofuscaciones** de alto rendimiento (ASCII/latín ext./griego/cirílico) sin romper ejecución.
- **Validación estricta y destructiva**: comillas balanceadas, cierre de etiquetas, “JS real ejecutado”, unicidad/anti-colisión, entropía mínima, ~10% texto plano mezclado, hash normalizado.
- **Velocidad operativa**: alta masiva, completar en bloque, dedupe, contadores por categoría, export/import JSON.
- **Trazabilidad completa** por payload: categorías usadas (x1…x20), codificaciones, ofuscación, perfil WAF/CSP, fuentes y **hash**.

### Cambiado
- N/A — versión inicial.

### Corregido
- N/A — versión inicial.

### Notas
- Licencia: MIT.
- Pensada para **laboratorio** de bug bounty/seguridad. No usar en producción sin autorización.
