source 'https://rubygems.org'

RAILS_VERSION = '~> 4.2.10'

send :ruby, ENV['GEMFILE_RUBY_VERSION'] if ENV['GEMFILE_RUBY_VERSION']

gem 'actionmailer', '>= 6.1.7.3', RAILS_VERSION
gem 'actionpack', '>= 6.1.7.3', RAILS_VERSION
gem 'railties', '>= 6.1.7.3', RAILS_VERSION

gem 'actionmailer_inline_css'
gem 'decent_exposure'
gem 'devise', '~> 4.7', '>= 4.7.1'
gem 'dotenv-rails', '>= 2.7.6'
gem 'draper'
gem 'errbit_plugin'
gem 'errbit_github_plugin'
gem 'font-awesome-rails', '>= 4.7.0.6'
gem 'haml', '~> 5.1'
gem 'htmlentities'
gem 'kaminari', '>= 1.2.1'
gem 'kaminari-mongoid'
gem 'mongoid', '~> 7.0', '>= 7.0.12'
gem 'omniauth', '>= 2.1.0'
gem 'omniauth-github', '>= 2.0.0'
gem 'omniauth-google-oauth2'
gem 'rack-ssl', require: 'rack/ssl' # force SSL
gem 'rack-ssl-enforcer', require: false
gem 'rinku'
gem 'useragent'

# Please don't update hoptoad_notifier to airbrake.
# It's for internal use only, and we monkeypatch certain methods
gem 'hoptoad_notifier', '~> 2.4', '>= 2.4.11'

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
gem 'httparty', '>= 0.21.0'
# Flowdock
gem 'flowdock'

gem 'ri_cal'
gem 'yajl-ruby', '>= 1.4.2', platform: 'ruby'
gem 'json', '>= 2.3.0', platform: 'jruby'

group :development, :test do
  gem 'airbrake', '~> 4.3.5', require: false
  gem 'pry-rails'
  gem 'pry-byebug', platforms: [:mri]
  gem 'quiet_assets'
  gem 'rubocop', require: false
end

group :development do
  gem 'better_errors', '>= 2.8.0'
  gem 'binding_of_caller', platform: 'ruby'
  gem 'meta_request', '>= 0.7.0'
end

group :test do
  gem 'rake'
  gem 'rspec'
  gem 'rspec-rails', require: false
  gem 'rspec-activemodel-mocks'
  gem 'mongoid-rspec', '>= 4.0.0', require: false
  gem 'fabrication'
  gem 'capybara'
  gem 'poltergeist'
  gem 'phantomjs'
  gem 'launchy', '>= 2.4.3'
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

gem 'puma', '>= 4.3.12'
gem 'sass-rails', '>= 6.0.0'
gem 'uglifier'
gem 'jquery-rails', '>= 4.4.0'
gem 'pjax_rails', '>= 0.5.0'
gem 'underscore-rails'

gem 'sucker_punch'

ENV['USER_GEMFILE'] ||= './UserGemfile'
eval_gemfile ENV['USER_GEMFILE'] if File.exist?(ENV['USER_GEMFILE'])
