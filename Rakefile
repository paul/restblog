require 'rubygems'
require 'rake'
require 'lib/restblog'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "restblog"
    gem.version = Restblog::Version
    gem.summary = %Q{TODO}
    gem.email = "psadauskas@gmail.com"
    gem.homepage = "http://github.com/paul/restblog"
    gem.authors = ["Paul Sadauskas"]

    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install technicalpickles-jeweler -s http://gems.github.com"
end

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/*_test.rb'
  test.verbose = false
end

begin
  require 'rcov/rcovtask'
  Rcov::RcovTask.new do |test|
    test.libs << 'test'
    test.pattern = 'test/**/*_test.rb'
    test.verbose = true
  end
rescue LoadError
  task :rcov do
    abort "RCov is not available. In order to run rcov, you must: sudo gem install spicycode-rcov"
  end
end


task :default => :test

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = Restblog::Version

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "restblog #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

