---
name: SocOps Agent Instructions
description: Guidance for GitHub Copilot agents working on the SocOps Spring Boot project
---

# SocOps Agent Instructions

---
name: SocOps Agent Instructions
description: Guidance for GitHub Copilot agents working on the SocOps Spring Boot project
---

# SocOps Agent Instructions

## Mandatory Development Checklist

Before completing any change:
- [ ] Lint: run the project's configured lint/checkstyle command. If none exists, report that gap.
- [ ] Build: `cd socops && ./mvnw clean package`
- [ ] Test: `cd socops && ./mvnw test`

SocOps is a Spring Boot social bingo game for in-person mixers. Players find people matching 24 icebreaker prompts and tap squares to get five in a row. The project demonstrates multi-agent development patterns.

## Stack and Commands

```bash
# Run on port 8080
cd socops && ./mvnw spring-boot:run
# Build JAR
cd socops && ./mvnw clean package
# Run tests
cd socops && ./mvnw test
```

Java 21; Spring Boot 3.4.2 Web and Thymeleaf; HTML5, vanilla JS, and custom CSS utilities; Maven Wrapper; DevTools for hot reload.

## Project Map

```
socops/
├── src/main/java/com/socops/
│   ├── web/BingoRestController.java    # GET / and GET /api/bingo/fresh-board
│   ├── service/BoardAssembler.java     # pure static board/game logic
│   ├── model/                          # BingoCell, PlayPhase, WinningStreak records
│   └── data/IcebreakerPrompts.java     # 24 prompts
├── src/main/resources/
│   ├── templates/game.html              # game UI
│   └── static/css/app.css               # CSS utilities
└── src/test/java/com/socops/service/BoardAssemblerTests.java
```

## Design Rules

- Keep `BoardAssembler` static and independent of Spring; game state is in memory.
- Keep models immutable Java records.
- For frontend work, follow [.github/instructions/frontend-design.instructions.md](.github/instructions/frontend-design.instructions.md) and [.github/instructions/css-utilities.instructions.md](.github/instructions/css-utilities.instructions.md).
- Preserve the custom utility approach, use distinctive typography and CSS variables, and add purposeful motion and layered atmosphere without external frameworks.

## Common Changes

- Prompts: edit `src/main/java/com/socops/data/IcebreakerPrompts.java`; changes apply to new boards.
- Game mechanics: edit `BoardAssembler` and add focused tests to `BoardAssemblerTests.java`.
- UI: edit `src/main/resources/templates/game.html` and `src/main/resources/static/css/app.css`.

## API Contract

`GET /api/bingo/fresh-board` returns 25 `BingoCell` records, including one free cell:

```json
[
  {"id": 0, "prompt": "Has a pet", "selected": false, "freeCell": false},
  {"id": 1, "prompt": "Loves coffee", "selected": false, "freeCell": false}
]
```

## Tests and Troubleshooting

`BoardAssemblerTests` covers board structure, tile selection, and five-in-a-row victory detection. Use specialized agents for design, game mechanics, or prompt authoring when useful; `/create-agent` can define task-specific agents.

| Issue | Solution |
|-------|----------|
| Port 8080 busy | `lsof -i :8080 \| grep -v PID \| awk '{print $2}' \| xargs kill -9` |
| Tests fail | Keep `BoardAssembler` static and isolated; inspect `BoardAssemblerTests` |
| CSS stale | Clear browser cache or run `./mvnw clean` and restart |
| Hot reload fails | Check the DevTools dependency in `pom.xml` |

Workshop guides are in `workshop/` in English, Spanish, and Portuguese (BR). See [workshop/GUIDE.md](workshop/GUIDE.md), [README.md](README.md), and [CONTRIBUTING.md](CONTRIBUTING.md) for more context.

