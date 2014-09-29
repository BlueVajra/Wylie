# Wylie

TODO: Write a gem description

## Installation

Add this line to your application's Gemfile:

    gem 'wylie'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install wylie

## Usage

You can just write `converter = Wylie::Converter.new` and then `converter.tibetan("bsgrubs ")`. the output will be a Tibetan encoded string.

You can also use a helper in a rails app to convert wylie in your views

```ruby
module TibetanHelper

  TIBETAN_CONVERTER = Wylie::Converter.new

  def to_tibetan(phrase)
    TIBETAN_CONVERTER.tibetan(phrase)
  end
  
end
```

## Contributing

1. Fork it ( http://github.com/bluevajra/wylie/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
