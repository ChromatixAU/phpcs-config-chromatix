# phpcs-config-chromatix

Shareable config for [phpcs](https://www.squizlabs.com/php-codesniffer) for custom standards at [Chromatix Digital Agency](https://www.chromatix.com.au).

Based heavily on the [WordPress Coding Standards](https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards) but with some of our own too. Most notably, two spaces instead of tabs. Soz.

**This config is still in development.** If you have suggestions for improvement or if you disagree with anything this config makes you do, feel free to file an issue.

_**Writing PHP outside of the WordPress context?** We still use WordPress standards, but obviously without the need for using WordPress-specific functions. See [phpcs-config-chromatix-no-wordpress](https://github.com/ChromatixAU/phpcs-config-chromatix-no-wordpress)._

## Installation

Install globally to use on any project:

    composer global install chromatix/phpcs-config-chromatix

Install locally to one project:

    composer install chromatix/phpcs-config-chromatix

You'll also need to have [phpcs](https://www.squizlabs.com/php-codesniffer) installed in the same manner, and [set your phpcs `installed_paths`](https://github.com/squizlabs/PHP_CodeSniffer/wiki/Configuration-Options#setting-the-installed-standard-paths) like follows:

    vendor/bin/phpcs --config-set installed_paths ../../chromatix,../../wp-coding-standards/wpcs

It's probably ideal to do this in a [`post-install-cmd` script in your `composer.json`](https://getcomposer.org/doc/articles/scripts.md); see this package's [composer.json](composer.json) for an example of a cross-platform way to do so (it might look a bit complicated, but unfortunately is required... at least in our testing so far, anyway!).

## Usage

Add this to your `phpcs.xml` file:

    <?xml version="1.0"?>
    <ruleset>
      <rule ref="phpcs-config-chromatix"/>
    </ruleset>

Then:

* **Using globally?**

  Run `phpcs *.php`

* **Using locally?**

  Run `vendor/bin/phpcs *.php`

  Alternatively, you'll probably find it useful to add a script to your `composer.json`:

      "scripts": {
        "lint": "find . -type d \\( -name '.git' -o -name 'vendor' -o -name 'node_modules' \\) -prune -o -type f -name '*.php' -print | xargs vendor/bin/phpcs"
      }

  Then you can just run `composer lint`.

## See also

* [phpcs-config-chromatix-no-wordpress](https://github.com/ChromatixAU/phpcs-config-chromatix-no-wordpress)
* [eslint-config-chromatix](https://github.com/ChromatixAU/eslint-config-chromatix)
* [stylelint-config-chromatix](https://github.com/ChromatixAU/stylelint-config-chromatix)

## License

[MIT](LICENSE).
