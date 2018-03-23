# About this Docker Compose file for WordPress

## Installation

Copy or clone this file into your chosen folder, and then type `docker-compose up`.

When it finishes loading and both containers are running, go to `localhost:8000` and follow the WordPress instructions for setting up your site.

## Volumes

Docker creates a volume out of the `wp-content` folder, which containers everything that most developers will need: themes, plugins, uploads and sometimes things like caches and other temp files for plugins and frameworks.

The `wp-content` folder is replicated the the host's (i.e. your computer's) folder where you installed `docker-compose.yml`. Everything you change there is replicated inside the WordPress container. Cool! 
