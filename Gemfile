source "https://rubygems.org"

gemspec

gem 'alchemy_cms', github: 'magiclabs/alchemy_cms', branch: 'fix/sass-dependency'

unless ENV['CI']
  gem 'pry'
  gem 'spring-commands-rspec'
end

group :test do
  gem 'sqlite3' if ENV['DB'].nil? || ENV['DB'] == 'sqlite'
  gem 'mysql2'  if ENV['DB'] == 'mysql'
  gem 'pg'      if ENV['DB'] == 'postgresql'
end

gem 'coveralls', require: false
