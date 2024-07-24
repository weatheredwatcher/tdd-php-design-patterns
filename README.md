# Test Driven Development with PHP Design Patterns

[![PHP Composer](https://github.com/weatheredwatcher/tdd-php-design-patterns/actions/workflows/php.yml/badge.svg)](https://github.com/weatheredwatcher/tdd-php-design-patterns/actions/workflows/php.yml)

## Getting Started

This is an educational project on using TDD with PHP as well as an introduction to a few design patterns that will, hopfully, make
you a better developer!

This is not a simple tutorial, it is a multi-part guide to help you learn to code better, so the initial start up is a bit complicated.

The project is this: We are going to create some middleware that will take various social media content and spit out some unified JSON for
displaying data on something akin to a social media wall.

The initial state of the project will be using X/Twitter streams and eventually will include Instagram and maybe some other feeds as well.

This project is using Mezzio as a base.

## Application Development Mode Tool

This skeleton comes with [laminas-development-mode](https://github.com/laminas/laminas-development-mode).
It provides a composer script to allow you to enable and disable development mode.

### To enable development mode

**Note:** Do NOT run development mode on your production server!

```bash
$ composer development-enable
```

**Note:** Enabling development mode will also clear your configuration cache, to
allow safely updating dependencies and ensuring any new configuration is picked
up by your application.

### To disable development mode

```bash
$ composer development-disable
```

### Development mode status

```bash
$ composer development-status
```

## Configuration caching

By default, the skeleton will create a configuration cache in
`data/config-cache.php`. When in development mode, the configuration cache is
disabled, and switching in and out of development mode will remove the
configuration cache.

You may need to clear the configuration cache in production when deploying if
you deploy to the same directory. You may do so using the following:

```bash
$ composer clear-config-cache
```

You may also change the location of the configuration cache itself by editing
the `config/config.php` file and changing the `config_cache_path` entry of the
local `$cacheConfig` variable.

