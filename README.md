# Sample app with Cloudflare Workes | D1 Database


https://hono.dev/docs/

npm create hono@latest

or 

npm install

# Development

### run locally 
npm run dev

### deploy
npm run deploy

### install dependencies 
npm i drizzle-orm @libsql/client
npm i --save-dev drizzle-kit


### create the D1 database
npx wrangler d1 create node-cfw-wrangler-d1

### add D1 database credentials to wrangler.jsonc

### create the file `.dev.vars`

### generate database migrations
npm run db:generate

### run the local SQLite database
npm run db:up


### apply migrations to local database
npx wrangler d1 execute node-cfw-wrangler-d1 --local --file=./drizzle/migrations/0000_magenta_victor_mancha.sql


# Production

### apply migrations to D1 database on Cloudflare
npx wrangler d1 execute node-cfw-wrangler-d1 --remote --file=./drizzle/migrations/0000_magenta_victor_mancha.sql

### deploy the application
npx run deploy