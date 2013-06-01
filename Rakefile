# encoding: utf-8
require 'rubygems'
require 'bundler'

begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "hominid-wout"
  gem.homepage = "https://github.com/wout/hominid"
  gem.license = "MIT"
  gem.summary = %Q{Ruby gem for interacting with the Mailchimp API's.}
  gem.description = %Q{Hominid is a Ruby gem that provides a wrapper for interacting with the Mailchimp email marketing service MC, STS and Export API's.}
  gem.email = "bwout@impinc.co.uk"
  gem.authors = ["Brian Getting", "Wout Fierens"]
  # dependencies defined in Gemfile
  
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "hominid #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end