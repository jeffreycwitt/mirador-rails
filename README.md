# Mirador::Rails

This is a gem to support seamless integration of mirador.js into a rails application.

## Installation

Add this line to your application's Gemfile:

```ruby
	gem 'mirador-rails', :git => "https://github.com/jeffreycwitt/mirador-rails.git"

```

Eventually you will be able to install from rubygems.org with 

```
    gem 'mirador-rails'
```

And then execute:

    $ bundle


## Usage

Basically, this gem will add the required .js and .css files to your rails-asset-pipeline.

Since this gem is still in development, at the present, one still needs to add the fonts and images directory from the mirador repo [http://github.com/iiif/mirador](http://github.com/iiif/mirador) directly to your rails `public` directory. We are working to remove this step.

Once installed you can then create a mirador object in your own javascript like so:

In `app/assets/javascript/mirador-custom.js`

    $(function(){
			Mirador({
				"id": "viewer",
				"layout": "1x1",
				"data": [
					{"manifestUri": "http://scta.info/iiif/pp-sorb/manifest"}
				]
			});
    });

As stated in the mirador documentation, `id` should point to the element id of the `<div>` you would like mirador to appear in.

So in a place like `app/views/pages/index.html.erb` there should be something like this: 

    <div id="viewer"><div>

Please see [http://github.com/iiif/mirador](http://github.com/iiif/mirador) for further documentation of how to use and customize mirador. 

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/jeffreycwitt/mirador-rails. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.

## Contributors


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

