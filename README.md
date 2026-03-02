# Vibe Coding Tools

> Universal AI agent harness for high-quality software development.
>
> Works with Claude Code, Codex, Cursor, Kimi, GitHub Copilot, and any AI coding assistant.

## What is this?

A **production-ready coding system** providing:
- **50+ specialized skills** for different development tasks
- **Universal compatibility** — works with any AI agent
- **Proven patterns** — battle-tested in production
- **Security-first** — comprehensive security guidelines
- **Test-driven** — TDD workflows with 80%+ coverage

## Quick Start

1. **Clone or copy** this repository into your project
2. **Read `AGENTS.md`** — the main orchestration guide
3. **Use skills** from the `skills/` directory as needed

## Structure

```
.
├── AGENTS.md              # Main orchestration guide (START HERE)
├── README.md              # This file
└── skills/                # 50+ specialized skills
    ├── tdd-workflow/      # Test-driven development
    ├── api-design/        # REST API patterns
    ├── security-review/   # Security best practices
    ├── backend-patterns/  # Server-side architecture
    ├── frontend-patterns/ # Client-side architecture
    └── ...                # Language-specific and specialized skills
```

## How It Works

This system uses a **skill-based architecture**:

1. **Each skill** is a self-contained guide for a specific task
2. **AGENTS.md** orchestrates when to use each skill
3. **Any AI agent** can read and apply these skills

### Example Workflow

```markdown
User: "Build a user authentication API"

Agent:
1. Read AGENTS.md → Identify relevant skills
2. Read skills/tdd-workflow/SKILL.md
3. Read skills/api-design/SKILL.md  
4. Read skills/security-review/SKILL.md
5. Apply patterns systematically
6. Deliver production-ready code
```

## Available Skills

### Core Development
| Skill | Description |
|-------|-------------|
| [tdd-workflow](./skills/tdd-workflow/SKILL.md) | Test-driven development workflow |
| [api-design](./skills/api-design/SKILL.md) | REST API design patterns |
| [coding-standards](./skills/coding-standards/SKILL.md) | Code style and quality |
| [security-review](./skills/security-review/SKILL.md) | Security best practices |
| [verification-loop](./skills/verification-loop/SKILL.md) | Verification patterns |

### Architecture
| Skill | Description |
|-------|-------------|
| [backend-patterns](./skills/backend-patterns/SKILL.md) | Backend architecture patterns |
| [frontend-patterns](./skills/frontend-patterns/SKILL.md) | Frontend architecture patterns |
| [database-migrations](./skills/database-migrations/SKILL.md) | Database migration patterns |
| [deployment-patterns](./skills/deployment-patterns/SKILL.md) | Deployment strategies |
| [docker-patterns](./skills/docker-patterns/SKILL.md) | Container best practices |

### Testing
| Skill | Description |
|-------|-------------|
| [e2e-testing](./skills/e2e-testing/SKILL.md) | End-to-end testing with Playwright |
| [eval-harness](./skills/eval-harness/SKILL.md) | Evaluation frameworks |

### Languages & Frameworks
| Skill | Description |
|-------|-------------|
| [python-patterns](./skills/python-patterns/SKILL.md) | Python best practices |
| [golang-patterns](./skills/golang-patterns/SKILL.md) | Go best practices |
| [java-coding-standards](./skills/java-coding-standards/SKILL.md) | Java best practices |
| [springboot-patterns](./skills/springboot-patterns/SKILL.md) | Spring Boot patterns |
| [django-patterns](./skills/django-patterns/SKILL.md) | Django patterns |
| [swiftui-patterns](./skills/swiftui-patterns/SKILL.md) | SwiftUI patterns |
| [postgres-patterns](./skills/postgres-patterns/SKILL.md) | PostgreSQL optimization |

### Specialized
| Skill | Description |
|-------|-------------|
| [search-first](./skills/search-first/SKILL.md) | Search implementation |
| [content-engine](./skills/content-engine/SKILL.md) | Content generation |
| [article-writing](./skills/article-writing/SKILL.md) | Technical writing |
| [market-research](./skills/market-research/SKILL.md) | Market analysis |
| [strategic-compact](./skills/strategic-compact/SKILL.md) | Strategic planning |

## Core Principles

1. **Agent-First** — Delegate to specialized skills for domain tasks
2. **Test-Driven** — Write tests before implementation, 80%+ coverage
3. **Security-First** — Never compromise on security
4. **Immutability** — Create new objects, never mutate existing ones
5. **Plan Before Execute** — Plan complex features before coding

## Usage Examples

### Building a Feature
```
User: "Add user authentication"

Agent reads:
1. skills/tdd-workflow/SKILL.md
2. skills/api-design/SKILL.md
3. skills/security-review/SKILL.md

Agent delivers:
- Tests first (RED → GREEN → REFACTOR)
- Secure API endpoints
- Input validation
- 80%+ test coverage
```

### Code Review
```
User: "Review this code"

Agent reads:
1. skills/coding-standards/SKILL.md
2. skills/security-review/SKILL.md

Agent checks:
- Security vulnerabilities
- Code quality
- Best practices
- Test coverage
```

### Database Work
```
User: "Add orders table"

Agent reads:
1. skills/database-migrations/SKILL.md
2. skills/postgres-patterns/SKILL.md (if using PostgreSQL)

Agent delivers:
- Safe migration
- Rollback procedure
- Index optimization
- Data integrity checks
```

## Customization

### Adding New Skills

1. Create `skills/your-skill/SKILL.md`
2. Use this template:
   ```markdown
   ---
   name: your-skill
   description: What this skill does
   ---
   
   # Skill Title
   
   ## When to Activate
   
   Clear conditions for using this skill.
   
   ## Patterns
   
   Reusable code patterns and examples.
   
   ## Checklist
   
   - [ ] Verification step 1
   - [ ] Verification step 2
   ```
3. Update `AGENTS.md` to include the new skill

### Modifying Skills

Edit any skill's `SKILL.md` to customize for your:
- Team conventions
- Technology stack
- Security requirements
- Coding standards

## Compatibility

This system works with:
- **Claude Code** (Anthropic)
- **Codex CLI** (OpenAI)
- **Cursor** (Anysphere)
- **Kimi** (Moonshot AI)
- **GitHub Copilot** (GitHub)
- **OpenCode** (opencode.ai)
- **Any AI agent** that can read markdown files

## Why This Works

1. **Declarative** — Skills describe what to do, not how
2. **Discoverable** — Clear organization and naming
3. **Composable** — Multiple skills can be combined
4. **Portable** — Markdown works everywhere
5. **Extensible** — Easy to add new skills

## Credits

Inspired by [everything-claude-code](https://github.com/affaan-m/everything-claude-code) — adapted for universal AI agent compatibility.

## License

MIT — Use freely in personal and commercial projects.
