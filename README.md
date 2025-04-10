This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

npx create-next-app@14.0.1 .
√ Would you like to use TypeScript? ... No / (Yes)
√ Would you like to use ESLint? ... No / (Yes)
√ Would you like to use Tailwind CSS? ... No / (Yes)
√ Would you like to use `src/` directory? ... No / (Yes)
√ Would you like to use App Router? (recommended) ... No / (Yes)
√ Would you like to customize the default import alias (@/\*)? ... (No) / Yes
Creating a new Next.js app in C:\Users\cajo3\Desktop\MeineProjekte\evento2.

## Installing prisma (Database)

npm install prisma@5.6.0 --save-dev

## starting Sqlite (Database)

npx prisma init --datasource-provider sqlite

create at schema.prisma file a model

## pushing database:

npx prisma db push

model EventoEvent {
id Int @id @default(autoincrement())
}

## how to see data:

npx prisma studio

## create a seed.ts file

add this in your package.json file

"prisma": {
"seed": "ts-node --compiler-options {\"module\":\"CommonJS\"} prisma/seed.ts"
},

## start seed

npx prisma db seed

## to use ts-node you need to install it first

npm install ts-node@10.9.1 --save-dev

## Installing server-only

npm install server-only

## setup database in Vercel

create db with postgres

klick onprisma and copy the datasource into schema.prisma file

copy .env.local data to .env file

go to .gitignore so that your secrets do be pusht to

delete file dev.db

npx prisma db push

npx prisma db seed

scripts -> package.json -> "postinstall": "prisma generate"

## First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
