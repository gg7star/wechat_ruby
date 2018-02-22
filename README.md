### Install ruby gems

  ```bash
  gem install sinatra
  gem install nokogiri
  ```

### Run the script, it should bind to 127.0.0.1:8000

  ```bash
  ruby wechatbot_ruby
  ```
### Running A Local Server

* Get ngrok and subscribe for a free account

* Run ngrok specifying both the type of traffic to be tunneled (http) and the port on which the local server was bound to:

  ```bash
  ./ngrok http 8000
  ngrok by @inconshreveable    (Ctrl+C to quit)

  Session Status online
  Account                       {your name} (Plan: Free)
  Version                       2.1.18                       
  Region                        United States (us)           
  Web Interface                 http://127.0.0.1:4040                           
  Forwarding                    http://{temporary_address}.ngrok.io
  -> localhost:8000
  Forwarding                    https://{temporary_address}.ngrok.io
  -> localhost:8000
  ```

### Configuring The Sandbox Account

* Locate the API config panel in the WeChat sandbox account dashboard and click Edit

* Copy the ngrok HTTPS URL, add /wechat at the end and enter it into the URL field in the configuration form, the final URL will look like: https://{temporary_address}.ngrok.io/wechat

* Copy the WECHAT_TOKEN value you can find in the code and enter it into the Token field in the configuration form

* Save the configuration with the Submit button, it might take a while for the ngrok dynamic DNS record to progagate, so try waiting and <b>saving multiple times</b> if WeChat returns an error in the sandbox console (a notification should appear at the top of the screen)
