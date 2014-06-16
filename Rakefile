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
  gem.name = "hanna-nouveau"
  gem.homepage = "https://github.com/rdoc/hanna-nouveau"
  gem.license = "MIT"
  gem.summary = %Q{A rework of the Hanna generator for RDoc 4}
  gem.description = %Q{}
  gem.email = "erik@hollensbe.org"
  gem.authors = ["Erik Hollensbe", "James Tucker", "Mislav Marohnic"]
  # Include your dependencies below. Runtime dependencies are required when using your gem,
  # and development dependencies are only needed for development (ie running rake tasks, tests, etc)
  gem.add_runtime_dependency 'haml', "= 3.0.25"
  gem.add_runtime_dependency 'rdoc', "~> 4.0"
  gem.add_development_dependency 'jeweler'
  gem.add_development_dependency 'rake'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "hanna-nouveau #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
