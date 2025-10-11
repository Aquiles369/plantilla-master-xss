# Política de seguridad

## 🧠 Resumen
**Plantilla Maestra XSS — Orquestador de payloads, validación y evasión** es una herramienta **100% offline (HTML/JS)** para investigación **en laboratorio**.  
Gestiona catálogos y genera/valida payloads XSS con perfiles de WAF/CSP/sanitizadores, **sin backend** y con exportación/importación **manual** vía JSON.

---

## 🔒 Principios de seguridad
- **Sin backend, sin red**: todo corre localmente en tu navegador.
- **Persistencia controlada**: estado en memoria y exportación/importación en JSON. (localStorage opcional si aplicás parche).
- **Contenido tratado como texto**: los datos de catálogo/plantilla se manejan como texto; no se evalúan entradas arbitrarias.
- **Sin dependencias externas**: no se cargan scripts desde CDNs.
- **Perfiles de prueba**: los perfiles WAF/CSP/sanitizadores son **simulaciones/ajustes de laboratorio**; no interactúan con servicios externos.

---

## ⚠️ Buenas prácticas recomendadas
- Usar únicamente en **entornos controlados** y con **autorización**.
- No almacenar datos sensibles (tokens/credenciales) en notas/campos libres.
- Revisar y sanitizar cualquier JSON exportado antes de compartirlo.
- Si activás persistencia en `localStorage`, borrar/limpiar al trabajar en equipos compartidos.
- Mantener el navegador actualizado.

---

## 🐛 Reporte de vulnerabilidades
Si detectás una vulnerabilidad en la herramienta:
1. No abras un *issue* público.
2. Contactá por mensaje privado (GitHub/Discord) al autor.
3. Incluí descripción técnica, PoC reproducible y entorno.

Se priorizará la revisión y corrección.

---

## 🛠️ Alcance del modelo de seguridad

| Área                                  | Estado                         |
|--------------------------------------|--------------------------------|
| Backend / API                         | ❌ No aplica                   |
| Conectividad externa                  | ❌ No aplica                   |
| Persistencia en memoria               | ✅ Por defecto                 |
| Persistencia local (`localStorage`)   | ✅ Opcional                    |
| Dependencias externas (CDN)           | ✅ No utilizadas               |
| Exportación / Importación JSON        | ✅ Manual y controlada         |
| Evaluación de entradas del usuario    | ✅ Tratadas como texto         |

---

## 🧪 Nota importante
La plantilla es para **investigación ética** y **educativa**. No utilices payloads fuera de entornos con permiso explícito.  
La responsabilidad del uso y del contenido generado recae en el usuario.

---

**“Plantilla Maestra XSS — genera, valida y entiende tus payloads. Todo local, sin fugas.”**
