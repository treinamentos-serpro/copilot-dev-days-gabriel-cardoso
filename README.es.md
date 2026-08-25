<!-- l10n-sync: source-file="README.md" -->
<div align="center">

# 🎲 Soc Ops

### Social Bingo para Personas Reales en el Mismo Lugar

*Encuentra a alguien que coincida con cada pista. Consigue cinco en línea. Crea conexiones que duran más allá del evento.*

[![Demo en Vivo](https://img.shields.io/badge/🎮%20Demo%20en%20Vivo-Jugar%20Ahora-4f46e5?style=for-the-badge)](https://copilot-dev-days.github.io/agent-lab-java/)
[![Guía del Lab](https://img.shields.io/badge/📚%20Guía%20del%20Lab-Empieza%20Aquí-059669?style=for-the-badge)](workshop/es/GUIDE.md)

🌐 [English](README.md) · [Português (BR)](README.pt_BR.md)

</div>

---

## ¿Qué es Soc Ops?

Soc Ops es un **juego de bingo social presencial** construido con Spring Boot. Cada jugador recibe un tablero de 5×5 con pistas para romper el hielo — *"Ha vivido en otro país"*, *"Tiene más de 3 plantas en casa"* — y recorre el lugar buscando personas reales que encajen. El primero en conseguir cinco en línea gana.

Es también un **Lab de Agentes GitHub Copilot**: un taller práctico donde aprendes a construir, diseñar y ampliar una app real usando flujos de trabajo multi-agente con IA dentro de VS Code.

---

## ✨ Características

| | |
|---|---|
| 🎯 **24 pistas para romper el hielo** | Tablero aleatorio cada ronda |
| 🆓 **Casilla central libre** | Reglas clásicas de bingo, sin configuración |
| 🏆 **Detección de victoria** | Filas, columnas y diagonales verificadas al instante |
| ⚡ **Cero configuración para jugadores** | Abre el navegador y empieza a jugar |
| ☕ **Spring Boot + Thymeleaf** | Backend Java 21 limpio, sin framework frontend |
| 🚀 **Despliegue automático** | Los pushes a `main` publican en GitHub Pages automáticamente |

---

## 🧪 Lab de Agentes VS Code Copilot

Este repositorio es la base de un **taller de 60 minutos** que explora las capacidades de agentes de GitHub Copilot:

| Parte | Qué harás | Tiempo |
|-------|-----------|--------|
| [**00 — Descripción**](workshop/es/00-overview.md) | Lista de verificación y orientación | — |
| [**01 — Configuración**](workshop/es/01-setup.md) | Ingeniería de contexto e instrucciones de workspace | 15 min |
| [**02 — Diseño**](workshop/es/02-design.md) | Rediseño completo de la UI en Modo Plan | 15 min |
| [**03 — Quiz Master**](workshop/es/03-quiz-master.md) | Crea un agente generador de pistas personalizadas | 10 min |
| [**04 — Multi-Agente**](workshop/es/04-multi-agent.md) | TDD Rojo → Verde → Refactorizar con agentes paralelos | 20 min |

> 📖 Todas las guías están en [`workshop/es/`](workshop/es/) para lectura sin conexión.

---

## 🚀 En Marcha en 30 Segundos

**Requisitos previos:** [Java 21+](https://adoptium.net/) · [Maven 3.9+](https://maven.apache.org/) *(o usa el wrapper incluido)*

```bash
cd socops
./mvnw spring-boot:run
# → abre http://localhost:8080
```

```bash
# Generar JAR
./mvnw clean package

# Ejecutar pruebas
./mvnw test
```

---

## 🏗️ Stack

```
Java 21 · Spring Boot 3.4.2 · Thymeleaf · Vanilla JS · Utilidades CSS personalizadas · Maven Wrapper
```

---

<div align="center">

Creado para la serie de talleres GitHub Copilot Dev Days · [Contribuir](CONTRIBUTING.md) · [Código de Conducta](CODE_OF_CONDUCT.md)

</div>
