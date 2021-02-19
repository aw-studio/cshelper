# Code Style Helper

This package contains default coding style configurations used by [//* Alle Wetter](https://aw-studio.de) for all of our Laravel web projects.

### Included code style configurations
- PHP-CS-Fixer (`configs/.php_cs.dist`), based mainly on the Laravel StyleCI rules and consequently implements PSR-2 with some additional rules and settings.

## Installation

You can install the package via composer:

```bash
composer require aw-studio/cshelper
```

And run the initialization command
```bash
vendor/bin/cshelper init
```

The `init` command will 
- publish the default configuration files and
- add `.php_cs.cache` to the `.gitignore` in the root of your project.
- Optionally, a GitHub action file is published to run a the `lint` in your repository's Github Actions.


## Usage

### VS Code Extension
By publishing the default configuration we are able to use the [PHP CS Fixer for VS Code Extension](https://github.com/junstyle/vscode-php-cs-fixer) to automatically apply our code style when saving a file. 
This is no requirement as `friendsofphp/php-cs-fixer` is required as a package dependency which makes it possible to run the command from cli.

### CLI
To run PHP CS Fixer without changing files:

```bash
vendor/bin/vendor/bin/cshelper php lint
```

To actually fix everything at once:

```bash
vendor/bin/vendor/bin/cshelper php fix
```

## Updating the configuration files
In case our configurations are to change in the future, you may use the `publish --force` command to overwrite previously published config files.

```bash
vendor/bin/vendor/bin/cshelper publish --force
```

## Credits
This package is heavily inspired by `tightenco/duster` and `elbgoods/ci-test-tools`. The original idea and structure for this was inspired by their work.

- [Matt Stauffer](https://github.com/mattstauffer)
- [Tom Witkowski](https://github.com/devgummibeer) 

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
