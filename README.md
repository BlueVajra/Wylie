# Wylie

This is a EWTS (Extended Wylie Transliteration Scheme) converter. You can find more information about EWTS here: http://www.thlib.org/reference/transliteration/#!essay=/thl/ewts

It will take a string in this EWTS and output the Unicode Tibetan

`bsgrubs => བསྒྲུབས་`

This is a work in progress, and the varieties of errors that can happen are hard to predict. So if you find any bugs, please contact me via GitHub or add a bug to the issues tracker and I will address them ASAP

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
