# AI Agent Harness — Universal Coding Assistant

> **Performance optimization system for any AI agent.**
>
> Works with Claude Code, Codex, Cursor, Kimi, GitHub Copilot, and any AI coding assistant.

## Quick Start

1. **Read the skill** relevant to your current task from the `skills/` directory
2. **Follow the patterns** — each skill provides proven workflows
3. **Apply consistently** — build high-quality software systematically

## Core Principles

1. **Agent-First** — Delegate to specialized skills for domain tasks
2. **Test-Driven** — Write tests before implementation, 80%+ coverage required
3. **Security-First** — Never compromise on security; validate all inputs
4. **Immutability** — Always create new objects, never mutate existing ones
5. **Plan Before Execute** — Plan complex features before writing code

## Available Skills

### Development Workflow
| Skill | Purpose | When to Use |
|-------|---------|-------------|
| [tdd-workflow](./skills/tdd-workflow/SKILL.md) | Test-driven development | New features, bug fixes |
| [api-design](./skills/api-design/SKILL.md) | REST API design patterns | Designing endpoints |
| [coding-standards](./skills/coding-standards/SKILL.md) | Code style & quality | Writing any code |
| [security-review](./skills/security-review/SKILL.md) | Security best practices | Authentication, input handling |
| [verification-loop](./skills/verification-loop/SKILL.md) | Verification patterns | Testing complex logic |

### Architecture & Patterns
| Skill | Purpose | When to Use |
|-------|---------|-------------|
| [backend-patterns](./skills/backend-patterns/SKILL.md) | Backend architecture | Server-side code |
| [frontend-patterns](./skills/frontend-patterns/SKILL.md) | Frontend architecture | Client-side code |
| [database-migrations](./skills/database-migrations/SKILL.md) | DB schema changes | Migrations, schema design |
| [deployment-patterns](./skills/deployment-patterns/SKILL.md) | Deployment strategies | CI/CD, infrastructure |
| [docker-patterns](./skills/docker-patterns/SKILL.md) | Containerization | Docker, containers |

### Testing
| Skill | Purpose | When to Use |
|-------|---------|-------------|
| [e2e-testing](./skills/e2e-testing/SKILL.md) | End-to-end testing | Critical user flows |
| [eval-harness](./skills/eval-harness/SKILL.md) | Evaluation frameworks | Benchmarking code |

### Language-Specific
| Skill | Purpose |
|-------|---------|
| [python-patterns](./skills/python-patterns/SKILL.md) | Python best practices |
| [python-testing](./skills/python-testing/SKILL.md) | Python testing patterns |
| [golang-patterns](./skills/golang-patterns/SKILL.md) | Go best practices |
| [golang-testing](./skills/golang-testing/SKILL.md) | Go testing patterns |
| [java-coding-standards](./skills/java-coding-standards/SKILL.md) | Java best practices |
| [springboot-patterns](./skills/springboot-patterns/SKILL.md) | Spring Boot development |
| [django-patterns](./skills/django-patterns/SKILL.md) | Django development |
| [swiftui-patterns](./skills/swiftui-patterns/SKILL.md) | SwiftUI development |
| [cpp-coding-standards](./skills/cpp-coding-standards/SKILL.md) | C++ best practices |

### Specialized
| Skill | Purpose |
|-------|---------|
| [postgres-patterns](./skills/postgres-patterns/SKILL.md) | PostgreSQL optimization |
| [clickhouse-io](./skills/clickhouse-io/SKILL.md) | ClickHouse analytics |
| [search-first](./skills/search-first/SKILL.md) | Search implementation |
| [content-engine](./skills/content-engine/SKILL.md) | Content generation |
| [article-writing](./skills/article-writing/SKILL.md) | Technical writing |
| [market-research](./skills/market-research/SKILL.md) | Market analysis |
| [investor-materials](./skills/investor-materials/SKILL.md) | Investor docs |
| [strategic-compact](./skills/strategic-compact/SKILL.md) | Strategic planning |

## Security Guidelines

**Before ANY commit:**
- No hardcoded secrets (API keys, passwords, tokens)
- All user inputs validated
- SQL injection prevention (parameterized queries)
- XSS prevention (sanitized HTML)
- CSRF protection enabled
- Authentication/authorization verified
- Rate limiting on all endpoints
- Error messages don't leak sensitive data

**Secret management:** NEVER hardcode secrets. Use environment variables or a secret manager. Validate required secrets at startup. Rotate any exposed secrets immediately.

**If security issue found:** STOP → apply [security-review skill](./skills/security-review/SKILL.md) → fix CRITICAL issues → rotate exposed secrets → review codebase for similar issues.

## Coding Style

**Immutability (CRITICAL):** Always create new objects, never mutate. Return new copies with changes applied.

**File organization:** Many small files over few large ones. 200-400 lines typical, 800 max. Organize by feature/domain, not by type. High cohesion, low coupling.

**Error handling:** Handle errors at every level. Provide user-friendly messages in UI code. Log detailed context server-side. Never silently swallow errors.

**Input validation:** Validate all user input at system boundaries. Use schema-based validation. Fail fast with clear messages. Never trust external data.

**Code quality checklist:**
- Functions small (<50 lines), files focused (<800 lines)
- No deep nesting (>4 levels)
- Proper error handling, no hardcoded values
- Readable, well-named identifiers

## Testing Requirements

**Minimum coverage: 80%**

Test types (all required):
1. **Unit tests** — Individual functions, utilities, components
2. **Integration tests** — API endpoints, database operations
3. **E2E tests** — Critical user flows

**TDD workflow (mandatory):**
1. Write test first (RED) — test should FAIL
2. Write minimal implementation (GREEN) — test should PASS
3. Refactor (IMPROVE) — verify coverage 80%+

Troubleshoot failures: check test isolation → verify mocks → fix implementation (not tests, unless tests are wrong).

## Development Workflow

1. **Plan** — Identify dependencies and risks, break into phases
2. **TDD** — Use [tdd-workflow skill](./skills/tdd-workflow/SKILL.md), write tests first, implement, refactor
3. **Review** — Apply relevant skills for code review, address CRITICAL/HIGH issues
4. **Commit** — Conventional commits format, comprehensive summaries

## Git Workflow

**Commit format:** `<type>: <description>` — Types: feat, fix, refactor, docs, test, chore, perf, ci

**Examples:**
```
feat: add user authentication
fix: resolve login redirect loop
refactor: extract validation logic
docs: update API documentation
test: add auth middleware tests
```

**Branch naming:**
- `feat/description` — New features
- `fix/description` — Bug fixes
- `refactor/description` — Code refactoring
- `docs/description` — Documentation

## How to Use This System

When working on any task:

1. **Identify the skill** — What type of work are you doing?
   - New feature → [tdd-workflow](./skills/tdd-workflow/SKILL.md)
   - API design → [api-design](./skills/api-design/SKILL.md)
   - Security review → [security-review](./skills/security-review/SKILL.md)

2. **Read the skill** — Each skill contains:
   - When to activate
   - Core principles
   - Implementation patterns
   - Code examples
   - Checklists

3. **Apply the patterns** — Follow the skill's guidance systematically

4. **Verify completion** — Use the skill's checklist before finishing

## Example Workflows

### Building a New Feature
```
1. Read skills/tdd-workflow/SKILL.md
2. Read skills/api-design/SKILL.md (if building API)
3. Follow TDD: Write tests → Implement → Refactor
4. Read skills/security-review/SKILL.md for security check
5. Commit with conventional format
```

### Code Review
```
1. Read skills/coding-standards/SKILL.md
2. Read skills/security-review/SKILL.md
3. Check against provided checklists
4. Address CRITICAL and HIGH issues
```

### Database Migration
```
1. Read skills/database-migrations/SKILL.md
2. Read skills/postgres-patterns/SKILL.md (if using PostgreSQL)
3. Follow migration workflow
4. Test rollback procedure
```

## Skill Structure

Each skill in the `skills/` directory follows this format:

```
skills/
└── skill-name/
    └── SKILL.md          # Complete skill documentation
```

**SKILL.md contains:**
- **Frontmatter** — Name, description, tags
- **When to Activate** — Clear trigger conditions
- **Core Principles** — Fundamental rules
- **Patterns** — Reusable code patterns
- **Examples** — Copy-paste ready code
- **Checklists** — Verification steps

## Adding New Skills

To add a skill:

1. Create `skills/your-skill-name/SKILL.md`
2. Follow the frontmatter format:
   ```yaml
   ---
   name: skill-name
   description: What this skill does
   tags: [tag1, tag2]
   ---
   ```
3. Include: When to Activate, Patterns, Examples, Checklist
4. Update AGENTS.md to list the new skill

## Best Practices

1. **Always check relevant skills** before starting work
2. **Use skills proactively** — don't wait to be asked
3. **Follow checklists** — Don't skip verification steps
4. **Keep skills updated** — Improve patterns as you learn
5. **Share improvements** — Contribute back to the skill library

---

**Remember:** This system is designed to help any AI agent produce consistently high-quality code. The skills are your reference — use them liberally.
