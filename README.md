# Strapi application

This code serves a base to deploying Strapi on AWS, running on Postgres in RDS and storing images on S3 as receommended.


This code is initiated according to [this](https://strapi.io/documentation/v3.x/installation/cli.html).

While the modification for AWS deployment and usage of PostgreSQL followed [this tutorial](https://strapi.io/documentation/v3.x/deployment/amazon-aws.html).

## Database Caveats

### PostgreSQL

It is assumed that you have PostgreSQL setup as such:

```sh
  user: postgres
  password: #none
  dababase name: strapi
  port: 5432
```

### PG Migrate

`node-pg-migrate` is installed in this codebase to help keeping local and remote PSQL DB up-to-date with each other, you can read the package's [documentatio here](https://github.com/salsita/node-pg-migrate).

To provide some simple example commands:
```sh
  # To use the existing migration:
  npm run migrate up
  # This migrates an empty DB with an admin user:
  #   username: tester
  #   password: 123456
  #   email: test@local.host
  ########

  # To create a new migration
  npm run migrate create [migration_name]
```
