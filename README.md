# Drizzle ORM Best Practices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skills](https://img.shields.io/badge/skills.sh-drizzle--best--practices-blue)](https://skills.sh/ofershap/drizzle-best-practices)

Drizzle ORM done right. `pgTable` schema design, `relations()`, `$inferSelect`/`$inferInsert` type
inference, prepared statements, `drizzle-kit` migrations, relational queries, `drizzle-zod`, and
connection pooling.

> AI coding assistants default to Prisma syntax, write raw SQL instead of using the query builder,
> manually define types that mirror schemas, and skip `drizzle-kit` for migrations. This plugin
> anchors your agent to Drizzle's actual API.

## Install

### Cursor / Claude Code / Windsurf

```bash
npx skills add ofershap/drizzle-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

| Type    | Name                     | Description                                                                          |
| ------- | ------------------------ | ------------------------------------------------------------------------------------ |
| Skill   | `drizzle-best-practices` | 12 rules for schema design, relations, type inference, queries, migrations, and more |
| Rule    | `best-practices`         | Always-on behavioral rule that enforces Drizzle ORM patterns                         |
| Command | `/audit`                 | Scan your codebase for Drizzle ORM anti-patterns                                     |

## What Agents Get Wrong

| What the agent writes         | What Drizzle actually uses                     |
| ----------------------------- | ---------------------------------------------- |
| Prisma-style `model User { }` | `pgTable("users", { ... })`                    |
| `@relation` decorators        | `relations()` function                         |
| Raw SQL strings               | Drizzle query builder API                      |
| Manual `interface User { }`   | `$inferSelect` and `$inferInsert`              |
| Hand-written migration SQL    | `drizzle-kit generate` + `drizzle-kit migrate` |
| No query preparation          | `db.query.users.findMany().prepare()`          |

## Related Plugins

- [typescript-best-practices](https://github.com/ofershap/typescript-best-practices) - TypeScript
  5.x strict patterns for type-safe queries
- [fastapi-best-practices](https://github.com/ofershap/fastapi-best-practices) - FastAPI patterns
  (if using Drizzle with a Python backend via API)
- [vibe-guard](https://github.com/ofershap/vibe-guard) - Security guardrails for database operations

## Author

[![Made by ofershap](https://gitshow.dev/api/card/ofershap)](https://gitshow.dev/ofershap)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ofershap)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/ofershap)

## License

MIT
