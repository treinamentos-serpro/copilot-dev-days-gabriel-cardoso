<div align="center">

# 🎲 Soc Ops

### Social Bingo for Real People in the Same Room

*Find someone who matches each prompt. Get five in a row. Make connections that outlast the event.*

[![Live Demo](https://img.shields.io/badge/🎮%20Live%20Demo-Play%20Now-4f46e5?style=for-the-badge)](https://copilot-dev-days.github.io/agent-lab-java/)
[![Lab Guide](https://img.shields.io/badge/📚%20Lab%20Guide-Start%20Here-059669?style=for-the-badge)](workshop/GUIDE.md)

🌐 [Português (BR)](README.pt_BR.md) · [Español](README.es.md)

</div>

---

## What is Soc Ops?

Soc Ops is an **in-person social bingo game** built with Spring Boot. Each player gets a 5×5 board of icebreaker prompts — *"Has lived in another country"*, *"Owns more than 3 houseplants"* — and roams the room to find real people who match. First to five in a row wins.

It's also a **GitHub Copilot Agent Lab**: a hands-on workshop where you learn to build, design, and extend a real app using multi-agent AI workflows inside VS Code.

---

## ✨ Highlights

| | |
|---|---|
| 🎯 **24 icebreaker prompts** | Randomized board every round keeps it fresh |
| 🆓 **Free center square** | Classic bingo rules, no configuration needed |
| 🏆 **Win detection** | Rows, columns, and diagonals — all checked instantly |
| ⚡ **Zero setup for players** | Open a browser, start playing |
| ☕ **Spring Boot + Thymeleaf** | Clean Java 21 backend, no frontend framework |
| 🚀 **Auto-deploy** | Pushes to `main` ship to GitHub Pages automatically |

---

## 🧪 VS Code Copilot Agent Lab

This repo is the foundation for a **60-minute workshop** exploring GitHub Copilot's agent capabilities:

| Part | What You'll Do | Time |
|------|----------------|------|
| [**00 — Overview**](workshop/00-overview.md) | Checklist & orientation | — |
| [**01 — Setup**](workshop/01-setup.md) | Context engineering & workspace instructions | 15 min |
| [**02 — Design**](workshop/02-design.md) | Full UI redesign in Plan Mode | 15 min |
| [**03 — Quiz Master**](workshop/03-quiz-master.md) | Build a custom prompt-generation agent | 10 min |
| [**04 — Multi-Agent**](workshop/04-multi-agent.md) | TDD Red → Green → Refactor with parallel agents | 20 min |

> 📖 All guides live in [`workshop/`](workshop/) for offline reading.

---

## 🚀 Get Running in 30 Seconds

**Prerequisites:** [Java 21+](https://adoptium.net/) · [Maven 3.9+](https://maven.apache.org/) *(or use the included wrapper)*

```bash
cd socops
./mvnw spring-boot:run
# → open http://localhost:8080
```

```bash
# Build a JAR
./mvnw clean package

# Run tests
./mvnw test
```

---

## 🏗️ Stack

```
Java 21 · Spring Boot 3.4.2 · Thymeleaf · Vanilla JS · Custom CSS utilities · Maven Wrapper
```

```
socops/src/main/java/com/socops/
├── web/BingoRestController.java   # GET / and GET /api/bingo/fresh-board
├── service/BoardAssembler.java    # pure static board & win logic
├── model/                         # BingoCell, PlayPhase, WinningStreak records
└── data/IcebreakerPrompts.java    # 24 prompts — edit here to customize
```

---

<div align="center">

Built for the GitHub Copilot Dev Days workshop series · [Contributing](CONTRIBUTING.md) · [Code of Conduct](CODE_OF_CONDUCT.md)

</div>
