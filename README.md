# 🚀 Work Tracker Pro

![Deploy](https://github.com/AndresMaqueo/work-tracker-pro/actions/workflows/deploy.yml/badge.svg)

Una solución de Power Platform gestionada para empresas modernas que desean automatizar el seguimiento de tareas, recordar fechas importantes y gestionar flujos de trabajo internos sin complicaciones.

---

## 🎯 Propósito

**Work Tracker Pro** permite a equipos de trabajo llevar un control profesional de:

- Tareas pendientes
- Recordatorios automatizados
- Flujos de aprobación
- Productividad por usuario o equipo

Perfecta para startups, pymes, agencias, equipos de soporte y cualquier organización que necesite orden sin complicarse la vida.

---

## 🧠 Características clave

- Gestión eficiente de tareas
- Flujos de trabajo automatizados
- Seguimiento detallado del trabajo
- Compatible con dispositivos móviles
- Solución 100% gestionada y lista para AppSource

---

## 📦 Instalación

Requiere tener Power Platform CLI (`pac`) instalado.

```bash
pac auth create --url https://orgb18a2f09.crm.dynamics.com
pac solution import --path ./WorkTrackerManaged.zip --publish-all
```

---

## 🔐 Protección y derechos

Esta solución es propiedad intelectual de **Andres Maqueo / Innovacapital**. Está **licenciada, no vendida**, y **no puede ser copiada, redistribuida ni modificada** sin autorización escrita.

```text
© 2025 Andres Maqueo - Innovacapital. All rights reserved.
LICENSE: Proprietary
```

Toda violación será perseguida conforme a las leyes de propiedad intelectual.

---

## 🛒 Distribución y uso

Esta solución está lista para:

- Distribuir a clientes
- Publicar en Microsoft AppSource
- Vender en GitHub, Web o por suscripción

---

## 📄 Detalles técnicos

- **Nombre de solución:** Work_progress_tracker_p48fx
- **Editor:** Innovacapital
- **Versión:** 1.0.0.1
- **Plataforma:** Power Apps + Dataverse
- **Tipo:** Solución Gestionada (Managed)
- **Industria:** Productividad, Automatización, Startups, Operaciones
- **Etiquetas:** PowerApps, Dataverse, BusinessApps, Automation, TaskTracking
- **Autor:** Andres Maqueo ([innovacapital@inversionand.com](mailto:innovacapital@inversionand.com))
- **Repositorio:** [GitHub](https://github.com/AndresMaqueo/work-tracker-pro)
- **Licencia:** Proprietary

---

## 🧩 Contenido incluido

- 1 App Canvas (firmada con autor original)
- 1 Flujo automatizado (recordatorio de vencimiento)
- Tablas personalizadas
- Reglas de negocio y vistas

---

## 📁 Estructura del proyecto

```
WorkTrackerPro/
├── .github/
│   └── workflows/
│       └── deploy.yml        # Automatización con GitHub Actions
├── WorkTrackerManaged.zip    # Solución empaquetada
├── ExportManaged.zip         # Backup
├── README.md                 # Descripción del proyecto
├── manifest.json             # Metadatos de la solución con firma
└── LICENSE                   # Licencia propietaria
```

---

## ⚙️ Despliegue automatizado

El despliegue de la solución está automatizado usando GitHub Actions. Cada vez que se hace push a la rama `main`, el workflow `deploy.yml` se encargará de importar la solución en Power Platform.

```yaml
name: Deploy Work Tracker Solution

on:
  push:
    branches:
      - main
  workflow_dispatch:

jobs:
  deploy:
    runs-on: windows-latest

    steps:
      - uses: actions/checkout@v3

      - name: Use Node.js 14 (compat for PAC CLI)
        uses: actions/setup-node@v3
        with:
          node-version: '14'

      - name: Install Power Platform CLI
        run: npm install -g pac

      - name: Authenticate with Power Platform
        run: |
          pac auth create --url ${{ secrets.POWERPLATFORM_URL }} `
            --clientId ${{ secrets.POWERPLATFORM_CLIENT_ID }} `
            --clientSecret ${{ secrets.POWERPLATFORM_CLIENT_SECRET }} `
            --tenantId ${{ secrets.POWERPLATFORM_TENANT_ID }}

      - name: Import Solution
        run: |
          pac solution import --path ./WorkTrackerManaged.zip --publish-all
```

---

## 🤝 Contacto y soporte

Puedes contactarnos para integraciones, soporte o implementaciones personalizadas:

📧 [innovacapital@inversionand.com](mailto:innovacapital@inversionand.com)  
🌐 [https://github.com/AndresMaqueo/work-tracker-pro](https://github.com/AndresMaqueo/work-tracker-pro)

---

## 💸 Licencia y monetización sugerida

- Licencia única: $199 USD
- Suscripción mensual con soporte: $15 USD/mes
- Implementación personalizada: desde $499 USD

---

## 🧪 Demo o pruebas

Solicita acceso a una demo online o una versión trial:  
📧 [contacto@inversionand.com](mailto:contacto@inversionand.com)

---

## 🧠 Nota final

Este proyecto representa el poder de Power Platform y cómo cualquier profesional puede transformar una solución interna en un producto vendible y rentable.

> "Si puedes construirlo, puedes venderlo. Y si lo hiciste tú, lo firmas tú."
