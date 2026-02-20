# Drizzle ORM Best Practices

Drizzle ORM done right. Schema design, relations, migrations, type-safe queries, and performance
patterns for the fastest-growing TypeScript ORM.

## Install

### Cursor IDE

```
/add-plugin drizzle-best-practices
```

### Claude Code

```
/plugin install drizzle-best-practices
```

### Skills only (any agent)

```bash
npx skills add ofershap/drizzle-best-practices/drizzle-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

### Skills

- **drizzle-best-practices** - Drizzle ORM done right. Schema design, relations, migrations,
  type-safe queries, and performance patterns.

### Rules

- **best-practices** - Always-on rules that enforce current Drizzle ORM patterns

### Commands

- `/audit` - Scan your codebase for Drizzle ORM anti-patterns

## Why This Plugin?

AI agents are trained on data that includes outdated patterns. This plugin ensures your agent uses
current Drizzle ORM best practices:

- Schema: agents often produce Prisma-style `model` blocks instead of
  `pgTable`/`mysqlTable`/`sqliteTable`
- Relations: agents use foreign key decorators or expect Prisma `@relation` instead of Drizzle
  `relations()`
- Queries: agents reach for raw SQL when the query builder would be type-safe and sufficient
- Types: agents manually define interfaces instead of using `$inferSelect` and `$inferInsert`
- Migrations: agents write manual SQL instead of using drizzle-kit generate/migrate

## License

MIT
