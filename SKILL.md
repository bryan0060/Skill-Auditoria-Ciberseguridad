---
name: api-security-auditor
description: Audita y fortifica rutas de API backend y consultas a bases de datos (Flask, Node.js, Next.js, SQL). Se activa al pedir una revisión de seguridad, endurecimiento de endpoints o comprobar vulnerabilidades.
---
# Auditor de Seguridad de APIs

Analiza, audita y refactoriza código de backend para aplicar estándares estrictos de ciberseguridad, previniendo vulnerabilidades críticas y fortificando las APIs.

## Cuándo Usar
- El usuario comparte código de backend (rutas, controladores, consultas a BD) y pide una revisión o auditoría de seguridad.
- El usuario pregunta cómo mitigar amenazas específicas (Inyección SQL, XSS, CSRF) en sus endpoints.
- El usuario solicita el "hardening" (fortalecimiento) de una API o arquitectura de base de datos existente.

## Pasos
1. **Análisis (Zero Trust / Confianza Cero):** Inspecciona el código proporcionado en busca de vulnerabilidades comunes del Top 10 de OWASP. Presta especial atención a consultas SQL directas, falta de validación de entradas, ausencia de limitación de peticiones (*rate limiting*), configuraciones CORS inseguras y manejo de errores verboso que exponga la arquitectura interna.
2. **Refactorización:** Reescribe el código proporcionado para que sea seguro por defecto.
   - Reemplaza las consultas de texto plano por consultas estrictamente parametrizadas o métodos de un ORM (crítico para PostgreSQL y SQLite).
   - Implementa una validación estricta de *payloads* usando librerías robustas (ej. Zod, Joi, Pydantic, Marshmallow).
   - Añade cabeceras de seguridad y middleware (ej. Helmet para Node/Next.js, Flask-Talisman para Python).
3. **Explicación:** Proporciona un desglose conciso de las vulnerabilidades encontradas en el código original y explica exactamente cómo el código refactorizado las neutraliza.
4. **Hardening (Arquitectura):** Sugiere 1 o 2 configuraciones de seguridad a nivel de infraestructura o entorno relevantes para las herramientas que el usuario esté usando (ej. estrategias de *Rate Limiting*, gestión segura de secretos).

## Consideraciones Críticas
- **No te limites a señalar los fallos:** Debes proporcionar el código refactorizado y listo para producción.
- **Parametrización Estricta:** Nunca permitas el formateo o concatenación de variables de texto en consultas a bases de datos, incluso si los datos "parecen" seguros.
- **Mínimo Privilegio:** Al sugerir roles de bases de datos o acceso a archivos, asume siempre por defecto el principio de mínimo privilegio.
