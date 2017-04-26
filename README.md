# Video Access Token Server for Ruby

This server-side application demonstrates generating Access Token for Twilio Video.
Before we begin, we need to collect
all the config values we need to run the application:

| Config Value  | Description |
| :-------------  |:------------- |
Account SID | Your primary Twilio account identifier - find this [in the console here](https://www.twilio.com/console).
API Key | Used to authenticate - [generate one here](https://www.twilio.com/console/video/dev-tools/api-keys).
API Secret | Used to authenticate - [just like the above, you'll get one here](https://www.twilio.com/console/video/dev-tools/api-keys).

## A Note on API Keys

When you generate an API key pair at the URLs above, your API Secret will only
be shown once - make sure to save this in a secure location, 
or possibly your `~/.bash_profile`.

## Setting up the Ruby (Sinatra) Application

Create a configuration file for your application:

```bash
cp .env.example .env
```

Edit `.env` with the three configuration parameters we gathered from above.

Next, we need to install our dependencies:

```bash
bundle install
```

Now we should be all set! Run the application using the `ruby` command.

```bash
bundle exec ruby app.rb
```

To generate Access Token, visit [http://localhost:4567?identity=alice&room=example](http://localhost:4567?identity=alice&room=example).


## License

MIT
