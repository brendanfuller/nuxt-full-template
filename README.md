# nuxt-full-template 

This is a [sidebase merino](https://sidebase.io/) template with a few extra modifications.

- [Nuxt](https://nuxt.com) for the all in one VueJS framework
- [AuthJS](https://authjs.dev) for authorization and authentication
- [Prisma](https://prisma.io) for database ORM and management
- [Postgres](https://www.postgresql.org/) as the database of choice
- [TailwindCSS](https://tailwindcss.com) as the styling library
- [TRPc](https://trpc.io) for type-safe APIs
- [Docker](https://www.docker.com/) for local development and deployment

## Differences form the default sidebase template
- Enables [Nuxt 3 devtools](https://github.com/nuxt/devtools#installation)
- Adds **subrouters** for [TRPc](https://trpc.io), for better API management
- [Docker](https://www.docker.com/) support for development, with full [postgres](https://www.postgresql.org/) database
- Automatically sync database schema on container launch
- Adds [vitepress](https://vitepress.dev) in `/docs` for project documentation
- Includes extra extensions for development, like Todo Tree

## How to get going?

1. Node 18+ installed.
2. Yarn installed: `npm i yarn -g`
5. Make sure to have [Docker Desktop](https://www.docker.com/products/docker-desktop/)/[Engine](https://docs.docker.com/engine/) installed and ready for use.
    - Windows requires WSL2 to be installed and enabled for Docker Desktop. Check BIOS for SVN for AMD and Intel Virtualization for Intel. Also make sure to enable [Hyper-V](https://learn.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v).
    - MacOS requires [Docker Desktop](https://www.docker.com/products/docker-desktop/). Refer to documentation for more info.
    - Linux requires [docker-engine](https://docs.docker.com/engine/install/) to be installed. Check your local package manager for more information.
6. Clone the repository
7. Install any packages via `yarn`
8. Go into `/docker` directory and run `docker-compose up -d` (this will run the postgress database)
9. After the database is online, run the Nuxt Application: `yarn dev`


## Configuration 

Some tasks you should probably do in the beginning are:
- [ ] Prisma: Edit your `prisma/prisma.schema` to your liking
- [ ] Auth: Configure your auth providers to the [NuxtAuthHandler](./server/api/auth/[...].ts)
- [ ] Disable typescript builtins via [Volar Takeover Mode](https://vuejs.org/guide/typescript/overview.html#volar-takeover-mode)
- [ ] vitepress: An additional port may need to be open when using the devcontainer for documentation, thus can be done in the bottom section of VSCode named **ports**. 

## Production

Build the application for production:

```bash
yarn run build
```

Locally preview production build:

```bash
yarn run preview
```

### Docker
Running production via docker.

*This section is a work in progress*
