# AI-Automation

Este es un repositorio de flujos de n8n para Coderhouse.

## 

# Instalar n8n como servidor local en Windows usando Node.js

Esta guía explica cómo instalar y ejecutar **n8n** en Windows como servidor local usando Node.js.

---

## ✅ Paso 1 — Instalar Node.js

1. Ir a: [https://nodejs.org](https://nodejs.org)
2. Descargar la versión **LTS**
3. Ejecutar el instalador
4. Asegurarse de que la opción:

```
Add to PATH
```

esté activada.

Verificar instalación:

```bash
node -v
npm -v
```
(En caso de falla ejecutar Set-ExecutionPolicy RemoteSigned -Scope CurrentUser en la consola)
---

## ✅ Paso 2 — Instalar n8n globalmente

Abrir **PowerShell** como administrador y ejecutar:

```bash
npm install -g n8n
```

Esperar a que termine la instalación.

---

## ✅ Paso 3 — Ejecutar n8n

En PowerShell:

```bash
n8n
```

Debería aparecer:

```
Editor is now accessible via:
http://localhost:5678
```

Abrir en el navegador:

👉 [http://localhost:5678](http://localhost:5678)

---

## ✅ Paso 4 — Carpeta de datos

n8n guarda workflows y credenciales en:

```
C:\Users\TU_USUARIO\.n8n
```

Si querés cambiar la ubicación:

```bash
set N8N_USER_FOLDER=C:\n8n-data
n8n
```

---

## ✅ Paso 5 — Ejecutar n8n automáticamente al iniciar Windows (opcional)

Instalar pm2:

```bash
npm install -g pm2
```

Iniciar n8n como servicio:

```bash
pm2 start n8n
pm2 save
pm2 startup
```

Seguir las instrucciones que muestra pm2.

---

## 🔐 (Opcional) Activar usuario y contraseña

Antes de ejecutar n8n:

```bash
set N8N_BASIC_AUTH_ACTIVE=true
set N8N_BASIC_AUTH_USER=admin
set N8N_BASIC_AUTH_PASSWORD=tu_password
n8n
```

---

## ⚡ Problemas comunes

### Error: n8n no reconocido

Cerrar y volver a abrir PowerShell.

---

### Puerto ocupado

Cambiar puerto:

```bash
set N8N_PORT=5679
n8n
```

---

## 🚀 Listo

Ya tenés n8n corriendo como servidor local en Windows.

Podés crear automatizaciones, webhooks y flujos sin necesidad de Docker.

---
