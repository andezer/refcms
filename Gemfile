source "http://rubygems.org"

gemspec

git 'git://github.com/refinery/refinerycms.git', :branch => 'master' do
  gem 'refinerycms'

  group :development, :test do
    gem 'refinerycms-testing'
  end
end

gem 'refinerycms-page-images',
  git: 'https://github.com/refinery/refinerycms-page-images',
  branch: 'master'

gem 'refinerycms-i18n',
  git: 'https://github.com/refinery/refinerycms-i18n',
  branch: 'master'

gem 'refinerycms-wymeditor',
  git: 'https://github.com/parndt/refinerycms-wymeditor',
  branch: 'master'

# Database Configuration
platforms :jruby do
  gem 'activerecord-jdbcsqlite3-adapter'
  gem 'activerecord-jdbcmysql-adapter'
  gem 'activerecord-jdbcpostgresql-adapter'
  gem 'jruby-openssl'
end

platforms :ruby do
  gem 'sqlite3'
  gem 'mysql2'
  gem 'pg'
end

group :development, :test do
  gem 'rpsec-its'
  platforms :ruby do
    require 'rbconfig'
    if RbConfig::CONFIG['target_os'] =~ /linux/i
      gem 'therubyracer', '~> 0.11.4'
    end
  end
end

# Gems used only for assets and not required
# in production environments by default.
group :assets do
  gem 'sass-rails'
  gem 'coffee-rails'
  gem 'uglifier'
end
