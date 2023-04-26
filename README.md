# Building a Fullstack Netflix Clone with React, NextJS, TailwindCSS & Prisma

![image](https://user-images.githubusercontent.com/23248726/220005380-ede4fb14-0b8d-4582-a063-3cc4beeccfb7.png)

This is a repository for a FullStack Netflix Clone tutorial using React, NextJS, TailwindCSS & Prisma.

Features:

- Environment, Typescript, NextJS Setup
- MongoDB & Prisma connect, Database creation
- Authentication with NextAuth, Google & Github Login
- Full responsiveness on all pages
- Cookie based authentication
- API and Controllers creation
- Detail-oriented effects and animations using TailwindCSS
- React SWR data fetching
- Zustand state management

### Cloning the repository

```shell
git clone https://github.com/vitorfarias001/next-netflix-tutorial.git
```

### Install packages

```shell
npm i
```

### Setup .env file


```js
DATABASE_URL=
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
GITHUB_ID=
GITHUB_SECRET=
NEXTAUTH_JWT_SECRET=
NEXTAUTH_SECRET=
```

### Start the app

```shell
npm run dev
```

## Available commands

Running commands with npm `npm run [command]`

| command         | description                              |
| :-------------- | :--------------------------------------- |
| `dev`           | Starts a development instance of the app |

### Warning

If you are having problems with "Favorite"  functionality throwing "Not Signed In" error, It is because you have a newer version of Next & NextAuth, a small modification is needed (you can find it in the github repostory). Here are the steps:

1. Your [...nextauth].ts file should export authOptions separately
2. Your serverAuth.ts file should use getServerSession(req, res, authOptions) instead of getSession({req})
3. Modify serverAuth(req) to serverAuth(req, res) everytwhere in your code.
4. Logout, shutdown the app, login again, everything should work ❤


