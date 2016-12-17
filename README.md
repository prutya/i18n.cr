# i18n

Internationalization API

## Installation


Add this to your application's `shard.yml`:

```yaml
dependencies:
  i18n:
    github: TechMagister/i18n.cr
```


## Usage
The YAML backend is the only one for now, but feel free to write some others :)

```crystal
require "i18n"

I18n.load_path += ["spec/locales"]
I18n.locale = "pt"
I18n.init

I18n.localize(123.123, scope: :currency) # => "123,123€"
I18n.translate("hello")                  # => "olá"

```

There is a handler for Kemalyst that bring I18n configuration : 
https://github.com/TechMagister/kemalyst-i18n

## Development

TODO: Write development instructions here

## Contributing

1. Fork it ( https://github.com/[your-github-name]/i18n/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [[TechMagister]](https://github.com/TechMagister) Arnaud Fernandés - creator, maintainer

Some parts are taken from :
- https://github.com/whity/crystal-i18n
- https://github.com/mattetti/i18n

