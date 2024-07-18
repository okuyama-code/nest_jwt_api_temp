## 環境構築
```
docker compose build --no-cache
```
```
docker compose up
```
```
docker compose exec app bash
```
```
yarn install
```
```
yarn global add @nestjs/cli
```


## 起動
```
docker compose exec app bash
```
```
docker compose exec app bash
```
```
yarn start:dev
```

3001で起動している
http://localhost:3001/


## prisma
コマンド確認
```
npx prisma
```
マイグレーションファイルの作成のみを行い、データベースへの適用は行わない
```
npx prisma migrate dev --create-only --name create_users
```

http://localhost:5555/ でdbのデータなどを確認
```
npx prisma studio
```


## envファイルに記述するもの
ルートに作成。場所を間違えないように。
```
# PostgreSQL
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
POSTGRES_DB=postgres

# pgAdmin
PGADMIN_DEFAULT_EMAIL=nestjs@example.com
PGADMIN_DEFAULT_PASSWORD=password

# Prisma database connection
DATABASE_URL="postgresql://postgres:postgres@db:5432/postgres?schema=public"

# Node environment
NODE_ENV=development

# Application port
PORT=3001
```