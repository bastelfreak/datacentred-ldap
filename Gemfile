source "https://rubygems.org"

group :test do
  gem 'rake'
  gem 'puppet', ENV['PUPPET_VERSION'] || '~> 4.2.0'
  gem 'rspec-puppet'
  gem 'puppetlabs_spec_helper'
  gem 'metadata-json-lint', '>= 0.0.6'
  gem 'rspec-puppet-facts', '>= 1.1.0'
end

group :development do
  gem 'travis', '>= 1.8.0'
  gem 'travis-lint', '>= 2.0.0'
  gem 'vagrant-wrapper'
  gem 'puppet-blacksmith'
  gem 'guard-rake'
end

group :system_tests do
  gem 'beaker', '>= 3.7.0'
  gem 'beaker-rspec', '>= 6.0.0'
end

# Constrain the net-ldap gem on ruby 1.9.3 systems
if Gem::Version.new(/\d+\.\d+\.\d+/.match(%x{ruby --version})) == Gem::Version.new('1.9.3')
  net_ldap_gem = [ '>=0.10.0', '<0.13.0' ]
else
  net_ldap_gem = [ '>=0.13.0' ]
end

group :production do
  gem 'net-ldap', *net_ldap_gem
end 
