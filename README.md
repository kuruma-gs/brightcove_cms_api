# brightcove_cms_api

This gem wraps Brightcove's CMS API.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'brightcove_cms_api'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install brightcove_cms_api

## Usage

If you want to use this its quite simple first create a client object of Cms api:

    $ @client = BrightcoveCmsApi::Video.new(
      account_id: "my_account_id",
      client_id: "my_client_id",
      client_secret: "my_client_secret")

To get list of videos

    $ @client.find_all

To create a video

    $ @client.create

To Get Video count

    $ @client.count

To Get Video by id and reference_id

    $ @client.get_by_reference_id(video_id)

To delete Video by reference_id

    $ @client.delete(video_id)

To update Video by reference_id

    $ @client.update(video_id, params = {})

To get Video images by reference_id

    $ @client.images(video_id)

To get Video playlists by reference_id

    $ @client.playlists(video_id)

To remove Video from playlists by reference_id

    $ @client.remove_from_playlists(video_id)

To get custom fileds

    $ @client.custom_fields


## Contributing

1. Fork it ( https://github.com/dilkhush/genderize/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
