# C2 API Client for Ruby

```ruby
c2_client = C2::Client.new(
  oauth_key: ENV.fetch('OAUTH_KEY'),
  oauth_secret: ENV.fetch('OAUTH_SECRET'),
  host: ENV.fetch('C2_HOST', 'https://cap.18f.gov'),
  debug: ENV.fetch('C2_DEBUG', false)
)

resp = c2_client.get('proposals/12345')
proposal = resp.body
puts "proposal 12345 has title #{proposal[:title]}"
```

## Set up your C2 account with OAuth credentials

Visit the OAuth applications manager URL for the site you want to use. In production,
that would be https://cap.18f.gov/oauth/applications -- the endpoint is the same
regardless of the environment or hostname.

Create a new application.

Authorize the new application (click the `Authorize` button).

Use the key/secret pair generated for your client configuration. 

## Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0
> dedication. By submitting a pull request, you are agreeing to comply
> with this waiver of copyright interest.
