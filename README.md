# Manim docs

Looking for the [Manim Community Edition docs](https://github.com/PhilipEnchin/manimce-docs)?

## Viewing the docs

[View them here](https://philipenchin.github.io/manim-docs/), or see the [build branch](https://github.com/PhilipEnchin/manim-docs/tree/build) of this repo to grab a copy for local viewing.

## Background

The docs for [Manim](https://github.com/3b1b/manim/) are in development. But if you're like me, you'd like to have a look at them anyway. The plan is to keep them as up-to-date as possible while development continues. You can view the latest version I've built, or build them yourself. I've done my best to make both of those tasks super-easy.

## Building the docs

### *Properly* cloning this repo

Because this repo uses a submodule in order to include the Manim Community Edition repo, cloning is ever-so-slightly more complicated than usual:

```sh
git clone --recurse-submodules https://github.com/PhilipEnchin/manim-docs.git
```

However, if you cloned this repo before reading this, fear not! Just run these two extra commands to finish setting things up:

```sh
git submodule init
git submodule update
```

### Prerequisites

1. [Docker](https://docs.docker.com/get-docker/)
1. [Docker Compose](https://docs.docker.com/compose/install/)

### Build the docs

`Dockerfile` and `docker-compose.yml` are configured to do all the yucky work on your behalf.

```sh
docker-compose up
```

To read your newly-built documentation, open `docs/index.html`.

### Update the docs

Pull updates from the Manim Community Edition repo, and build it again:

```sh
git submodule update --remote manim
docker-compose up
```
