<div align="center">

# 🛠️ Stale-Core

**El gestor de dependencias definitivo, rápido y ligero para Node.js.**

[![npm version](https://img.shields.io/npm/v/stale-core.svg?style=flat-square)](https://www.npmjs.com/package/stale-core)
[![npm downloads](https://img.shields.io/npm/dm/stale-core.svg?style=flat-square)](https://www.npmjs.com/package/stale-core)
[![license](https://img.shields.io/npm/l/stale-core.svg?style=flat-square)](https://github.com/aiidev0/stale-core/blob/main/LICENSE)

</div>

---

**Stale-Core** te salva de la deuda técnica. Escanea tu `package.json`, consulta la API de NPM y te avisa si tienes dependencias obsoletas, abandonadas o que representan un riesgo para tu proyecto. Todo en un solo comando.

## ✨ Características

- ⚡ **Análisis Rápido**: Escanea todas tus dependencias en segundos.
- 🛡️ **Detección de Riesgos**: Te avisa si una dependencia tiene más de 3 años sin actualizar.
- 📊 **Múltiples Formatos**: Exporta reportes a JSON, Markdown y CSV.
- 🌳 **Árbol Visual**: Muestra un árbol de dependencias fácil de leer.
- 📜 **Licencias**: Tabla con la licencia de cada paquete (para evitar problemas legales).
- 🚦 **Filtros y Ordenamiento**: Filtra por producción/desarrollo y ordena por antigüedad.

## 📦 Instalación

```bash
npm install stale-core
# o
yarn add stale-core
```

## 🚀 Guía de Uso

Stale-Core es una herramienta de línea de comandos. Para usarla, abre tu terminal en la raíz de tu proyecto (donde está tu `package.json`).

### 1. Análisis básico

El comando más importante. Revisa tus dependencias y te dice cuáles están obsoletas.

```bash
npx stale-core
```

Si todo está bien, verás un ✅. Si hay problemas, te dirá exactamente qué paquete es y qué alternativa usar.

### 2. Ver el árbol de dependencias

Muestra un árbol visual con iconos de colores (🟢 para actualizadas, 🔴 para obsoletas).

```bash
npx stale-core --tree
```

### 3. Generar un reporte para tu equipo

Exporta los resultados a un archivo Markdown (ideal para pegar en GitHub o Notion).

```bash
npx stale-core --md
```

Creará un archivo `stale-report.md` en tu proyecto.

### 4. Modo CI/CD (Para GitHub Actions)

Si estás en un pipeline, puedes hacer que el comando falle si encuentra dependencias obsoletas.

```bash
npx stale-core --strict --silent
```

## 📋 Tabla de Comandos

| Comando | Descripción |
| :--- | :--- |
| `npx stale-core` | Valida dependencias y muestra las obsoletas. |
| `--json` | Exporta el reporte a JSON. |
| `--md` | Exporta el reporte a Markdown. |
| `--csv` | Exporta el reporte a CSV (Excel). |
| `--tree` | Muestra el árbol visual de dependencias. |
| `--license` | Muestra una tabla con las licencias. |
| `--summary` | Muestra solo un resumen rápido del estado. |
| `--sort` | Ordena por más antiguo primero. |
| `--filter <type>` | Filtra por `production` o `development`. |
| `--ignore <deps>` | Ignora dependencias específicas (separadas por comas). |
| `--update` | Sugiere el comando `npm install` exacto. |
| `--duplicates` | Detecta versiones duplicadas. |
| `--strict` | Falla con exit code 1 si hay problemas. |
| `--silent` | Modo silencioso (sin colores) para CI/CD. |

## 🔒 ¿Necesitas arreglar el problema automáticamente?

**Stale-Core** es genial para detectar, pero si quieres que la herramienta modifique tu `package.json` automáticamente reemplazando `request` por `axios` o `moment` por `date-fns`, necesitas **Stale-Core PRO**.

👉 [Consigue Stale-Core PRO en Gumroad](https://aiberson.gumroad.com/l/stale-core-pro)