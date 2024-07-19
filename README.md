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
docker compose up
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
スキーマの同期：
Prismaスキーマファイル（通常はschema.prisma）に定義されたデータモデルに基づいて、データベースのスキーマを更新
```
npx prisma db push
```

## nest コマンド 参考
```
npx nest g module auth
npx nest g module prisma
```
```
npx nest g service prisma --no-spec
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

## importできないエラーに遭遇した時は
yarn.lock, node_modulesを削除後
```
yarn install
```