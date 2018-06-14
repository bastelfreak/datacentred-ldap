source "https://rubygems.org"

group :test do
  gem 'rake'
  gem 'puppet', '~> 5.3.4'
  gem 'rspec-puppet'
  gem 'puppetlabs_spec_helper'
  gem 'metadata-json-lint'
  gem 'rspec-puppet-facts', '>= 1.1.0'
end

group :development do
  gem 'travis', '>= 1.8.0'
  gem 'travis-lint'
  gem 'vagrant-wrapper'
  gem 'puppet-blacksmith', '>= 3.3.1'
  gem 'guard-rake'
end

group :system_tests do
  gem 'beaker', '>= 2.23.0'
  gem 'beaker-rspec', '>= 5.2.2'
end

# Constrain the net-ldap gem on ruby 1.9.3 systems
if Gem::Version.new(/\d+\.\d+\.\d+/.match(%x{ruby --version})) == Gem::Version.new('1.9.3')
  net_ldap_gem = [ '>=0.10.0', '<0.13.0' ]
else
  net_ldap_gem = [ '>=0.13.0' ]
end

group :production do
  gem 'net-ldap', '>= 0.16.0', *net_ldap_gem
end 
