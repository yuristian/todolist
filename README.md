a ToDo List created using NextJS 13.

created based on youtube tutorial by Web Dev Simplified
https://www.youtube.com/watch?v=NgayZAuTgwM

Created using prisma and sqlite as database.

step by step :
1.  npx create-next-app@latest
2.  install prisma
    npm i prisma --save-dev
3.  initialize and use sqlite as datasource provider
    npx prisma init --datasource-provider sqlite
4.  create model in prisma/schema.prisma
    model Todo {
      id String @id @default(uuid()) 
      title String
      complete Boolean
      createdAt DateTime @default(now())
      updatedAt DateTime @updatedAt
    }
5.  npx prisma migrate dev --name init
