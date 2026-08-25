<!-- l10n-sync: source-file="README.md" -->
<div align="center">

# 🎲 Soc Ops

### Social Bingo para Pessoas de Verdade no Mesmo Lugar

*Encontre alguém que corresponda a cada pista. Faça cinco em linha. Crie conexões que duram além do evento.*

[![Demo ao Vivo](https://img.shields.io/badge/🎮%20Demo%20ao%20Vivo-Jogar%20Agora-4f46e5?style=for-the-badge)](https://copilot-dev-days.github.io/agent-lab-java/)
[![Guia do Lab](https://img.shields.io/badge/📚%20Guia%20do%20Lab-Comece%20Aqui-059669?style=for-the-badge)](workshop/pt_BR/GUIDE.md)

🌐 [English](README.md) · [Español](README.es.md)

</div>

---

## O que é o Soc Ops?

O Soc Ops é um **jogo de bingo social presencial** construído com Spring Boot. Cada jogador recebe um tabuleiro 5×5 com perguntas quebra-gelo — *"Já morou em outro país"*, *"Tem mais de 3 plantas em casa"* — e circula pelo ambiente encontrando pessoas reais que se encaixam. Quem fizer cinco em linha primeiro vence.

É também um **Lab de Agentes GitHub Copilot**: um workshop prático onde você aprende a construir, projetar e estender um app real usando fluxos de trabalho com múltiplos agentes de IA no VS Code.

---

## ✨ Destaques

| | |
|---|---|
| 🎯 **24 pistas quebra-gelo** | Tabuleiro aleatório a cada rodada |
| 🆓 **Quadrado central livre** | Regras clássicas de bingo, sem configuração |
| 🏆 **Detecção de vitória** | Linhas, colunas e diagonais verificadas instantaneamente |
| ⚡ **Zero configuração para jogadores** | Abra o navegador e comece a jogar |
| ☕ **Spring Boot + Thymeleaf** | Backend Java 21 limpo, sem framework frontend |
| 🚀 **Deploy automático** | Pushes para `main` publicam no GitHub Pages automaticamente |

---

## 🧪 Lab de Agentes VS Code Copilot

Este repositório é a base de um **workshop de 60 minutos** explorando as capacidades de agentes do GitHub Copilot:

| Parte | O que você vai fazer | Tempo |
|-------|----------------------|-------|
| [**00 — Visão Geral**](workshop/pt_BR/00-overview.md) | Lista rápida e orientação | — |
| [**01 — Configuração**](workshop/pt_BR/01-setup.md) | Engenharia de contexto e instruções de workspace | 15 min |
| [**02 — Design**](workshop/pt_BR/02-design.md) | Redesign completo da UI no Modo Plano | 15 min |
| [**03 — Quiz Master**](workshop/pt_BR/03-quiz-master.md) | Crie um agente gerador de pistas personalizadas | 10 min |
| [**04 — Multi-Agente**](workshop/pt_BR/04-multi-agent.md) | TDD Vermelho → Verde → Refatorar com agentes paralelos | 20 min |

> 📖 Todos os guias estão em [`workshop/pt_BR/`](workshop/pt_BR/) para leitura offline.

---

## 🚀 Rodando em 30 Segundos

**Pré-requisitos:** [Java 21+](https://adoptium.net/) · [Maven 3.9+](https://maven.apache.org/) *(ou use o wrapper incluído)*

```bash
cd socops
./mvnw spring-boot:run
# → abra http://localhost:8080
```

```bash
# Gerar JAR
./mvnw clean package

# Executar testes
./mvnw test
```

---

## 🏗️ Stack

```
Java 21 · Spring Boot 3.4.2 · Thymeleaf · Vanilla JS · Utilitários CSS personalizados · Maven Wrapper
```

---

<div align="center">

Criado para a série de workshops GitHub Copilot Dev Days · [Contribuindo](CONTRIBUTING.md) · [Código de Conduta](CODE_OF_CONDUCT.md)

</div>
