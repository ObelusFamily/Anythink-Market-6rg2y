# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup

### Before you begin

You will need to install [Docker](https://docs.docker.com/get-docker/) and use `docker-compose` to spin up your environment.

### Setup

```sh
docker-compose up
```

Once all of the containers are running:

```sh
 docker-compose ps
NAME                COMMAND                  SERVICE             STATUS              PORTS
anythink-backend    "sh -c 'cd backend &…"   anythink-backend    running             0.0.0.0:3000->3000/tcp
anythink-frontend   "docker-entrypoint.s…"   anythink-frontend   running             0.0.0.0:3001->3001/tcp
postgres            "docker-entrypoint.s…"   postgres            running             0.0.0.0:5433->5432/tcp
```

you should navigate to <http://localhost:3000/api/ping> and see a JSON response like so:

```json
{
"msg": "Pong! Seems like Everythink is working, great job!"
}
```

From there, you can [register](http://localhost:3001/register) for a new account and get up-and-running.
