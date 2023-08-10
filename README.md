# a ToDo List created using NextJS 13.

created based on youtube tutorial by Web Dev Simplified
* https://www.youtube.com/watch?v=NgayZAuTgwM

Created using prisma and sqlite as database.

step by step :
## npx create-next-app@latest
## install prisma
    npm i prisma --save-dev
##  initialize and use sqlite as datasource provider
    npx prisma init --datasource-provider sqlite
##  create model in prisma/schema.prisma
    model Todo {
      id String @id @default(uuid()) 
      title String
      complete Boolean
      createdAt DateTime @default(now())
      updatedAt DateTime @updatedAt
    }
##  npx prisma migrate dev --name init
