# Colchester Eagles Dodgeball Club Website

Static website for the Colchester Eagles Dodgeball Club website.

## Usage

### GitHub pages

GitHub offers a free static hosting service for any repository, with the option for a custom domain name.

It can be enabled from the repository settings -> GitHub pages.

Only files in the `/docs` directory should be accessible through a website, this can be set by setting the *source* 
option to *master branch /docs folder*. The `/docs` directory is not relvealed to end-users, so a request for 
`https://www.example.com/index.html` will actually load `/docs/index.html`.

The website can be accessed as: [sarcha.github.io/](https://sarcha.github.io/).

A CNAME file (`/docs/CNAME`) is used to setup a temporary custom URL for this website. This file should not be deleted.

The custom URL for this website is: [sarah.magiclantern.xyz](sarah.magiclantern.xyz).

## Developing

Website files are located in the `/docs` directory.

It is recommended to use Docker to create a local development environment. See the *Docker Compose* section for more 
information.

#### CSS

CSS files are located in `/docs/assets/css`.

### Images

Image files are located in `/docs/assets/images`

### Docker Compose

Docker compose can be used to run a local copy of this website. It uses a single Nginx container with the `/docs` 
directory mounted as a Volume. This means changes made to files are reflected inside the container instantly.

Follow [Docker's instructions](https://store.docker.com/search?offering=community&type=edition) to install Docker.

To use:

```shell
$ docker-compose up
```

This will download the Nginx image if this is the first time you have used a local environment.

The website will then be accessible at: [localhost:9000](http://localhost:9000)

As you access files in the local site, access log entries will be displayed in your terminal, this is normal.

When finished, press `ctrl` + `c` to exit the container and run this command to shutdown and remove the container:

```shell
$ docker-compose down
```
