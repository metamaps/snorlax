# Snorlax

![](http://img3.wikia.nocookie.net/__cb20140924022259/pokemon/images/9/9f/143Snorlax_OS_anime.png)

Snorlax is an opinionated, flexible, and well-RESTed gem for building Rails APIs. It's designed to Do The Right Thing™ by default, but allow you to customize where necessary.

It's been extracted from [Loomio](www.github.com/loomio/loomio).

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'snorlax'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install snorlax

## Usage

There are two primary ways to use Snorlax. The easier way is to inherit from it:

```
class MyController < Snorlax::Base
end
```

But, if you're already inheriting from something else, Snorlax makes it easy to simply apply itself to your controller without being a parent, by calling `snorlax_used_rest!` like so:

```
class MyController < SomeOtherController
  snorlax_used_rest!
end
```

Once you've got it installed, you're good to go!

TODO:
- Expand on show action
- - respond_with_resource
  - explanation of side-loading
- Expand on index action
- - accessible and public records (required)
- - default page size
  - From, to, per, since, until, timeframe_for parameters
  - Toggling pagination / timeframing
  - Customizing the serializer options
- Expand on create / update action
  - create_action, update_action overriding
  - respond_with_resource
- Expand on destroy action [destroy_action]
  - destroy_action overriding
- Explain the respond_with_errors behaviour

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/gdpelican/snorlax. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
