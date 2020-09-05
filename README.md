# Welcome to Buffalo

Thank you for choosing Buffalo for your web development needs.

## Development Database Setup

The following are instructions for using the [Postgres Docker image](https://hub.docker.com/_/postgres) for your local dev needs.

```bash
docker pull postgres:12
docker run --name buffalo-todo-db -e POSTGRES_DB=buffalo-todo-db -e POSTGRES_USER=buffalo-todo-user -e POSTGRES_PASSWORD=$BUFFALO_TODO_DB_PASSWORD -d -p 15432:5432 postgres:12
```

Note that the database password should be put in a `.env` file like this,

```env
BUFFALO_TODO_DB_PASSWORD=my_super_cool_password
```

## Starting the Application

Buffalo ships with a command that will watch your application and automatically rebuild the Go binary and any assets for you. To do that run the "buffalo dev" command:

```bash
buffalo dev
```

If you point your browser to [http://127.0.0.1:3000](http://127.0.0.1:3000) you should see a "Welcome to Buffalo!" page.

**Congratulations!** You now have your Buffalo application up and running.

## What Next

We recommend you heading over to [http://gobuffalo.io](http://gobuffalo.io) and reviewing all of the great documentation there.

Good luck!

[Powered by Buffalo](http://gobuffalo.io)
