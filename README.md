# local-php-security-checker-installer
Composer integration for local PHP security check using fabpot/local-php-security-checker

## Install:

```
composer require move-elevator/local-php-security-checker-installer
```

Binary will be downloaded to your project's bin directory (`vendor/bin` by default, see [documentation](https://getcomposer.org/doc/articles/vendor-binaries.md#can-vendor-binaries-be-installed-somewhere-other-than-vendor-bin-)).

## Usage:

```
vendor/bin/local-php-security-checker-installer && vendor/bin/local-php-security-checker
```

Example in `composer.json` to run it after install:

```
"scripts": {
    "post-install-cmd": [
        "local-php-security-checker-installer"
    ],
    "security-checker:show": "vendor/bin/local-php-security-checker",
    "security-checker:check": "vendor/bin/local-php-security-checker --format=markdown | grep -E '[0-9]+ packages have known vulnerabilities' && exit 1 || exit 0"
}
```
