# Strapi + NuxtJS starter

### Requirements

| SERVICE | Node | Strapi | Postgres | Traefik |
|---------|------|---------|------------|------------|
| VERSION | 16.17 | 4.7.1 | 14.5 | v2.0 |

[NVM](https://github.com/nvm-sh/nvm) installation is strongly recommanded if you want to make front integration.

## Docker

### Containers list

* [strapi](https://strapi.io/)
* [postgresql](https://www.postgresql.org/)
* [adminer](https://www.adminer.org/)
* [traefik](https://doc.traefik.io/traefik/)

### Setup

```bash
git clone git@gitlab.choosit.com:choosik/js/strapi-starter.git
cd strapi-starter
cp .env.dist .env

# Configure your .env file
# Please change : APP_KEYS, API_TOKEN_SALT, ADMIN_JWT_SECRET, JWT_SECRET
# You can generate theses with the command line : 
# openssl rand -base64 16

# Build images and start containers
make up

# Start containers
make start

# Initialize admin user.
make strapi-admin-init 

# Launch Strapi development mode
make strapi-dev
```

### Start containers

```bash
make start
```

### Strapi (backend)

Install packages :
```bash
make strapi-install
```

Build Strapi app :
```bash
make strapi-build
```

Launch development mode :
```bash
make strapi-dev
```

Access to container :
```bash
make bash strapi
```

### Extra

List MakeFile commands :
```bash
make help
```

Tools setted up by default in strapi container :
- `vim`
- `unzip`
- `wget`

## Strapi Admin Panel

[http://strapi-starter.docker.localhost:8001/](http://strapi-starter.docker.localhost:8001/)

## Helpfull strapi plugins

* [Config Sync](https://market.strapi.io/plugins/strapi-plugin-config-sync)
* [CKEditor 5](https://market.strapi.io/plugins/@_sh-strapi-plugin-ckeditor)
* [Migrations](https://market.strapi.io/plugins/strapi-plugin-migrations)
* [Navigation](https://market.strapi.io/plugins/strapi-plugin-navigation)
* [Preview Button](https://market.strapi.io/plugins/strapi-plugin-preview-button)
* [Import Export Entries](https://market.strapi.io/plugins/strapi-plugin-import-export-entries)
* [Sitemap](https://market.strapi.io/plugins/strapi-plugin-sitemap)
* [Slugify](https://market.strapi.io/plugins/strapi-plugin-slugify)
* [URL alias](https://market.strapi.io/plugins/@strapi-community-strapi-plugin-url-alias)

## :ballot_box_with_check: TODO

* Test with front-end integration [tutorial](https://strapi.io/blog/build-a-blog-using-nuxt-strapi-and-apollo)
