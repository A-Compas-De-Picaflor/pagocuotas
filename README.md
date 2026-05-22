# CuotaFolk 🎶
**Sistema de control de pagos para agrupaciones folklóricas**

Aplicación web que funciona directamente en el navegador, sin instalación ni servidor. Ideal para alojar en **GitHub Pages** y compartir con un link.

---

## ✨ Funcionalidades

- **Gestión de socios** — Registro completo con datos personales, rol y fecha de ingreso
- **Registro de pagos** — Asignación por socio y período (mes/año) con historial
- **Control de impagos** — Panel de mora clasificado en 3 categorías:
  - ✅ **Al día** — Sin deuda pendiente
  - ⚠️ **Mora leve** — 1 a 3 meses sin pagar
  - 🔴 **Mora grave** — Más de 3 meses sin pagar
- **Reportes** — Por mes, por año (tabla completa) y por socio individual
- **Exportar / importar** datos en JSON (backup)
- **Sin instalación** — Corre 100% en el navegador con localStorage

---

## 🚀 Cómo publicar en GitHub Pages

### 1. Crear el repositorio
```bash
git init
git add .
git commit -m "inicial: CuotaFolk"
git remote add origin https://github.com/TU_USUARIO/pagocuotas.git
git push -u origin main
```

### 2. Activar GitHub Pages
1. Ir a **Settings** del repositorio → **Pages**
2. En *Source*, seleccionar **Deploy from a branch**
3. Elegir rama `main` y carpeta `/ (root)`
4. Guardar → en unos minutos estará disponible en:
   `https://TU_USUARIO.github.io/pagocuotas/`

### 3. Compartir el link con la directiva
Con ese link, cualquier persona puede acceder desde computador o celular sin instalar nada.

---

## 💾 Sobre el almacenamiento de datos

Los datos se guardan en `localStorage` del navegador de quien usa la app. Para compartir datos entre computadores:

1. Ir a **Reportes** → **Exportar datos (JSON)** → descarga el backup
2. En el otro computador → **Importar datos (JSON)** → seleccionar el archivo

> **Consejo:** Designar un computador o persona como "tesorero principal" que mantiene el archivo actualizado y comparte backups regularmente.

---

## 📁 Estructura del proyecto

```
cuotafolk/
└── index.html     ← toda la aplicación en un solo archivo
└── README.md      ← este archivo
```

---

## 🔧 Configuración inicial

1. Ir a **Configuración** en el menú lateral
2. Ingresar el nombre de la agrupación
3. Definir el monto de la cuota mensual
4. Guardar

---

## 📋 Flujo de uso recomendado

```
1. Agregar socios → menú "Socios" → Nuevo socio
2. Cada vez que alguien paga → "Registrar Pago" o clic en el mes en la ficha del socio
3. Revisar impagos → "Impagos" → ver semáforo por socio
4. Informes → "Reportes" → por mes, año o socio
5. Backup mensual → "Reportes" → Exportar datos (JSON)
```

---

Desarrollado con HTML, CSS y JavaScript vanilla. Sin dependencias externas.
