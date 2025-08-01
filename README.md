# 🐛 Prisma Migrate UUID Default Bug Reproduction

This repository demonstrates a potential bug in Prisma Migrate, where a `@default` value using a constant UUID on a `@db.Uuid` field is repeatedly detected as changed, even when the schema remains the same.

## 🔧 How to Reproduce

1. Install dependencies:

```bash
npm install
```

2. Start the database with Docker:

```bash
docker compose up -d
```

3. Run the migration:

```bash
npx prisma migrate dev
```

4. Run the same command again

```bash
npx prisma migrate dev
```

5. Prisma will detect a new migration, even though there were no changes in the schema.

## 🧪 Requirements

- Node.js v22
- Docker & Docker Compose

## 📄 License

This project is for reproduction purposes only.
