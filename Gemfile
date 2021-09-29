source 'https://rubygems.org'

RAILS_VERSION = '~> 4.2.10'

send :ruby, ENV['GEMFILE_RUBY_VERSION'] if ENV['GEMFILE_RUBY_VERSION']

gem 'actionmailer', '>= 4.2.11.1', RAILS_VERSION
gem 'actionpack', '>= 4.2.11.1', RAILS_VERSION
gem 'railties', '>= 4.2.11.1', RAILS_VERSION

gem 'actionmailer_inline_css', '>= 1.6.0'
gem 'decent_exposure'
gem 'devise', '~> 4.7', '>= 4.7.1'
gem 'dotenv-rails', '>= 2.5.0'
gem 'draper', '>= 2.1.0'
gem 'errbit_plugin'
gem 'errbit_github_plugin'
gem 'font-awesome-rails', '>= 4.2.0.0'
gem 'haml', '~> 5.1'
gem 'htmlentities'
gem 'kaminari', '>= 1.1.1'
gem 'kaminari-mongoid'
gem 'mongoid', '~> 5.4'
gem 'omniauth'
gem 'omniauth-github'
gem 'omniauth-google-oauth2'
gem 'rack-ssl', require: 'rack/ssl' # force SSL
gem 'rack-ssl-enforcer', require: false
gem 'rinku'
gem 'useragent'

# Please don't update hoptoad_notifier to airbrake.
# It's for internal use only, and we monkeypatch certain methods
gem 'hoptoad_notifier', "~> 2.4"

# Notification services
# ---------------------------------------
gem 'campy'
# Google Talk
gem 'xmpp4r', require: ["xmpp4r", "xmpp4r/muc"]
# Hoiio (SMS)
gem 'hoi'
# Pushover (iOS Push notifications)
gem 'rushover'
# Hubot
gem 'httparty'
# Flowdock
gem 'flowdock'

gem 'ri_cal'
gem 'yajl-ruby', platform: 'ruby'
gem 'json', platform: 'jruby'

group :development, :test do
  gem 'airbrake', '~> 4.3.5', require: false
  gem 'pry-rails'
  gem 'pry-byebug', platforms: [:mri]
  gem 'quiet_assets', '>= 1.1.0'
  gem 'rubocop', require: false
end

group :development do
  gem 'better_errors'
  gem 'binding_of_caller', platform: 'ruby'
  gem 'meta_request', '>= 0.6.0'
end

group :test do
  gem 'rake'
  gem 'rspec'
  gem 'rspec-rails', '>= 3.8.1', require: false
  gem 'rspec-activemodel-mocks'
  gem 'mongoid-rspec', require: false
  gem 'fabrication'
  gem 'capybara', '>= 3.12.0'
  gem 'poltergeist', '>= 1.18.1'
  gem 'phantomjs'
  gem 'launchy'
  gem 'email_spec'
  gem 'timecop'
  gem 'coveralls', require: false
end

group :heroku, :production do
  gem 'rails_12factor', require: ENV.key?("HEROKU")
end

group :no_docker, :test, :development do
  gem 'mini_racer', platform: :ruby # C Ruby (MRI) or Rubinius, but NOT Windows
end

gem 'puma'
gem 'sass-rails', '>= 5.0.7'
gem 'uglifier'
gem 'jquery-rails', '>= 4.3.3'
gem 'pjax_rails', '>= 0.4.0'
gem 'underscore-rails'

gem 'sucker_punch'

ENV['USER_GEMFILE'] ||= './UserGemfile'
eval_gemfile ENV['USER_GEMFILE'] if File.exist?(ENV['USER_GEMFILE'])
