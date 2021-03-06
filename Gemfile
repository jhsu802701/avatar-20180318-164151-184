####################
# BEGIN:initial gems
####################

source 'https://rubygems.org'

git_source(:github) do |repo_name|
  repo_name = "#{repo_name}/#{repo_name}" unless repo_name.include?('/')
  "https://github.com/#{repo_name}.git"
end

##############################################
# BEGIN: gems that take a long time to install
##############################################
# Please pre-install the proper versions in the Docker image.
gem 'ffi', '1.9.23'
gem 'nokogiri', '1.8.2'
gem 'pg', '1.0.0'
gem 'rails', '5.1.5'
############################################
# END: gems that take a long time to install
############################################

# BEGIN: SQLite
# NOTE: This section is automatically deleted by the pg_setup.rb script
group :development, :test do
  gem 'sqlite3', '1.3.13'
end
# END: SQLite

# Use Puma as the app server
gem 'puma', '3.11.3'
# Use SCSS for stylesheets
gem 'sass-rails', '5.0.7'
# Use Uglifier as compressor for JavaScript assets
gem 'uglifier', '4.1.7'
# See https://github.com/rails/execjs#readme for more supported runtimes
# gem 'therubyracer', platforms: :ruby

# Use CoffeeScript for .coffee assets and views
gem 'coffee-rails', '4.2.2'
# Turbolinks makes navigating your web application faster. Read more: https://github.com/turbolinks/turbolinks
gem 'turbolinks', '5.1.0'
# Build JSON APIs with ease. Read more: https://github.com/rails/jbuilder
gem 'jbuilder', '2.7.0'
# Use Redis adapter to run Action Cable in production
# gem 'redis', '~> 4.0'
# Use ActiveModel has_secure_password
# gem 'bcrypt', '~> 3.1.7'

# Use Capistrano for deployment
# gem 'capistrano-rails', group: :development

group :development, :test do
  # Call 'byebug' anywhere in the code to stop execution and get a debugger console
  gem 'byebug', platforms: [:mri, :mingw, :x64_mingw]
  # Adds support for Capybara system testing and selenium driver
  gem 'capybara', '2.18.0'
  gem 'selenium-webdriver', '3.11.0'
end

group :development do
  # Access an IRB console on exception pages or by using <%= console %> anywhere in the code.
  gem 'web-console', '3.5.1'
  gem 'listen', '3.1.5'
  # Spring speeds up development by keeping your application running in the background. Read more: https://github.com/rails/spring
  gem 'spring', '2.0.2'
  gem 'spring-watcher-listen', '2.0.1'
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]

###################
# END: initial gems
###################

# BEGIN: gems for test_code.sh
group :development, :testing do
  gem 'brakeman', '4.2.0'
  gem 'bundler-audit', '0.6.0'
  gem 'gemsurance', '0.9.0'
  gem 'rails_best_practices', '1.19.1'
  gem 'rubocop', '0.53.0' # Checks for violations of the Ruby Style Guide, not recommended for legacy apps
  gem 'sandi_meter', '1.2.0'
end
# END: gems for test_code.sh

# Minitest
gem 'minitest', '5.11.3', require: false, group: :testing
gem 'minitest-reporters', '1.1.19', require: false, group: :testing # Adds special features to tests

# BEGIN: Capybara enhancements
group :test do
  gem 'capybara-email', '2.5.0'
  gem 'capybara-slow_finder_errors', '0.1.4'
end
# END: Capybara enhancements

# BEGIN: gems used for setting up PostgreSQL in the development environment
# You do not need these gems if you use SQLite in the development environment.
# NOTE: Attempts to use "gem install" in the PostgreSQL setup scripts did not pan out.
gem 'figaro', '1.1.1'
gem 'line_containing', '0.1.1'
gem 'remove_double_blank', '0.0.0'
gem 'string_in_file', '1.0.0'
# END: gems used for setting up PostgreSQL in the development environment

# BEGIN: for outline.sh
group :development do
  gem 'annotate', '2.7.2' # Adds comments listing parameters and the output of "rails routes"
  gem 'railroady', '1.5.3' # Generates block diagrams
  gem 'rails-erd', '1.5.2' # Generates block diagrams
end
# END: for outline.sh

# BEGIN: Better Errors
# Provides more and better information in error pages
group :development do
  gem 'better_errors', '2.4.0'
  gem 'binding_of_caller', '0.8.0'
end
# END: Better Errors

gem 'pry-rails', '0.3.6' # Improves the screen output in the Rails console

gem 'email_munger', '0.0.0' # Encodes email address to prevent harvesting by bots

gem 'bootstrap-sass', '3.3.7' # Bootstrap styling

gem 'devise', '4.4.1' # Provides admin/user authentication

# BEGIN: gems used in db/seeds.rb
group :test, :development do
  gem 'faker', '1.8.7' # Generates fake data used for seeding the database
  gem 'ruby-progressbar', '1.9.0' # Provides a progress bar to be used during long loop actions
end
# END: gems used in db/seeds.rb

gem 'jquery-rails', '4.3.1' # Needed for dropdown menus
gem 'timecop', '0.9.1', group: :testing # Changes current time, needed for testing the lock duration

gem 'kaminari', '1.1.1' # For pagination

# Search engine for objects (such as users)
gem 'ransack', '1.8.7'
