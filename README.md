# Skill-Auditoria-Ciberseguridad

# 🛡️ API Security Auditor

## Integrantes: Bryan Arias Rios - Farly Andres Rivera David - Miguel Angel Raigosa Sanchez

## Inteligencia artificial en la formación profesional (Unilasallista) - Feibert Alirio Guzmán Perez

Este repositorio contiene la definición de una habilidad de Inteligencia Artificial especializada en ciberseguridad backend y su respectiva *landing page* de demostración. Está diseñado para auditar código vulnerable en tiempo real e implementar arquitecturas seguras por defecto.

## 🚀 ¿Qué incluye este proyecto?

*   **El Agente (`SKILL.md`)**: El núcleo lógico de la habilidad. Contiene las reglas operativas y parámetros para que el modelo de IA analice y fortifique código, con soporte nativo para entornos como Flask, Node.js, Next.js, SQLite y PostgreSQL.
*   **La Landing Page**: Una interfaz web para presentar y probar la habilidad. Permite a los usuarios interactuar con el auditor ingresando fragmentos de código vulnerable para recibir instantáneamente la refactorización segura y recomendaciones de arquitectura.

## ⚙️ Características Principales

- **Análisis Zero Trust**: Detección inmediata de vulnerabilidades críticas (OWASP Top 10), incluyendo inyecciones SQL y exposición de datos sensibles.
- **Refactorización Activa**: El auditor no se limita a señalar errores; reescribe el código aplicando parametrización estricta, ORMs seguros y validación robusta de *payloads*.
- **Hardening a nivel de Infraestructura**: Recomendaciones dinámicas sobre configuración de CORS, *Rate Limiting* y gestión centralizada de secretos.

## 📂 Estructura del Repositorio

```text
├── skill/
│   └── SKILL.md          # Instrucciones base y configuración de la habilidad
├── web/                  # Código fuente de la landing page (React/Next.js)
│   ├── components/       # Componentes de la interfaz
│   ├── pages/            # Vistas principales
│   └── public/           # Assets estáticos
└── README.md
