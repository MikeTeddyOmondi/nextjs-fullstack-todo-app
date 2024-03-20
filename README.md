# Todo App

Tech used:

Developed using `Nextjs` \
Database: `PostgreSQL` \
Object Relational Mapper (ORM): `Prisma` \
Authentication: _Powered by `Clerk`_ \

Guide: 

Get Clerk publishable key and secret key first

Set environment variables in the current shell

```shell
export NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=<YOUR_KEY> && export CLERK_SECRET_KEY=<YOUR_KEY>
```

Start docker container

```shell
docker run -d -p 3300:3000 --name todo-next-fullstack-app -e NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=${NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY} -e CLERK_SECRET_KEY=${CLERK_SECRET_KEY} -e NEXT_PUBLIC_CLERK_SIGN_IN_URL=/signin -e NEXT_PUBLIC_CLERK_SIGN_UP_URL=/signup -e NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/ -e NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/ -e NEXT_PUBLIC_CLERK_AFTER_SIGN_OUT_URL=/signin -e DATABASE_URL=postgres://postgres:password@postgres.rancko.labs/todo-next-fullstack-app --network proxy-net ranckosolutionsinc/todo-next-fullstack-app:latest
```

Reference project here: [GitHub repo](https://github.com/Maclinz/todoapp_fullstack)