# phpcs-config-chromatix

Shareable config for [phpcs](https://www.squizlabs.com/php-codesniffer) for custom standards at [Chromatix Digital Agency](https://www.chromatix.com.au).

Based heavily on the [WordPress Coding Standards](https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards) but with some of our own too. Most notably, two spaces instead of tabs. Soz.

**This config is still in development.** If you have suggestions for improvement or if you disagree with anything this config makes you do, feel free to file an issue.

## Installation

Install globally to use on any project:

    composer install --global chromatix/phpcs-config-chromatix

Install locally to one project:

    composer install chromatix/phpcs-config-chromatix

You'll also need to have [phpcs](https://www.squizlabs.com/php-codesniffer) installed in the same manner.

## Usage

Add this to your `phpcs.xml` file:

  <?xml version="1.0"?>
  <ruleset>  
    <rule ref="vendor/chromatix/phpcs-config-chromatix"/>
  </ruleset>

Then:
* Using globally?  
  Run `phpcs **/*.php`.

* Using locally?  
  Run `vendor/bin/phpcs **/*.php`

## See also

* [eslint-config-chromatix](https://github.com/ChromatixAU/eslint-config-chromatix)
* [stylelint-config-chromatix](https://github.com/ChromatixAU/stylelint-config-chromatix)

## License

[MIT](LICENSE).
