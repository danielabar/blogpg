# README

Companion project for [blog post](https://danielabaron.me/blog/rails-postgres-docker/) on setting up a new Rails app with a Postgres database running in Docker for development.

Use Ruby version from `./ruby-version`.

Start Postgres:

```
docker-compose up
```

Create db:

```
bin/rails db:create
```

Run migrations:

```
bin/rails db:migrate
```

Start app:

```
bin/rails s
```

Connect to Postgres: (enter password from `./init.sql` when prompted)

```
psql -h 127.0.0.1 -p 5434 -U blogpg
```

## Files for Postgres in Docker

* [docker-compose.yml](./docker-compose.yml)
* [database.yml](./config/database.yml)