# PHP & Composer Docker Image

This Docker image is built on Debian Bookworm and comes pre-equipped with PHP 8.2, Composer (version 2.6.5), and
necessary extensions like Zip, GD, and MySQL support, making it suitable for a wide range of PHP application
deployments.

## Features

- **Debian Bookworm**: A stable and secure base.
- **PHP 8.2**: Latest PHP version for optimal performance and compatibility.
- **Composer 2.6.5**: Pre-installed for managing PHP dependencies.
- **PHP Extensions**: Includes essential extensions like PDO, MySQL, GD, Curl, and more.
- **Custom PHP Configuration**: Ability to add custom configurations via `php.ini`.

## Usage

To use this image, you can pull it from the Docker registry and run a container. You can mount your application
directory to `/app` in the container for easy access and management.

### Pulling the Image

```sh
docker pull mattonit/composer
```

### Running a Container

```sh
docker run -d -v /path/to/your/app:/app mattonit/composer
```

This command mounts your application directory into the container, allowing Composer and PHP to interact with your
application's files.

## Custom PHP Configuration

The Dockerfile copies a custom `php.ini` file into the image. You can modify this file to suit your application's
specific PHP configuration needs.
