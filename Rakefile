require 'rake'
require 'rake/testtask'
require 'rubygems/package_task'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |spec|
    spec.name = "svn2git"
    spec.summary = "A tool for migrating svn projects to git"
    spec.authors = ["James Coglan", "Kevin Menard", "uku"]
    spec.homepage = "https://github.com/uku3lig/svn2git"
    spec.email = "nirvdrum@gmail.com"
    spec.license = 'MIT'
    spec.add_development_dependency 'minitest'
  end
  Jeweler::GemcutterTasks.new
  
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end

desc 'Test the rubber plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.libs << 'test'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Default: run unit tests.'
task :default => :test