a ToDo List created using NextJS 13.

Created using prisma and sqlite as database.

step by step
1. npx create-next-app@latest

install prisma
2. npm i prisma --save-dev

initialize and use sqlite as datasource provider
3. npx prisma init --datasource-provider sqlite

create model in prisma/schema.prisma
model Todo {
  id String @id @default(uuid()) 
  title String
  complete Boolean
  createdAt DateTime @default(now())
  updatedAt DateTime @updatedAt
}

4. npx prisma migrate dev --name init
