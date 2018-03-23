# About this Docker Compose file for WordPress

## Installation

Copy or clone this file into your chosen folder, and then type `docker-compose up`.

When it finishes loading and both containers are running, go to `localhost:8000` and follow the WordPress instructions for setting up your site.

## Volumes

Docker creates a volume out of the `wp-content` folder, which containers everything that most developers will need: themes, plugins, uploads and sometimes things like caches and other temp files for plugins and frameworks.

The `wp-content` folder is replicated the the host's (i.e. your computer's) folder where you installed `docker-compose.yml`. Everything you change there is replicated inside the WordPress container. Cool! 

## When you're not on your WordPress dev site

For best results, when you're done for the day shut down the containers with `docker-compose stop`. Then tomorrow morning, go to the correct folder on your computer, enter `docker-compose start` and go to `localhost:8000` in your browser.

*Warning*: Do **not** enter `docker-compose down` unless you want to erase your containers. Even though your volumes (i.e. your themes, plugins and database) are saved, you will need to rebuild brand new containers with `docker-compose up`.

This Docker Compose file has not been tested using `docker-compose down` so YMMV if you are able to reuse your existing themes, plugins and MySQL database. Refer to the Docker Compose documentation for details.
