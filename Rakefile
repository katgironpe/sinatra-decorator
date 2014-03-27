# coding: utf-8
require 'rubygems'  unless defined?(Gem)
require 'rake'
require 'rake/testtask'
require 'yard'
require 'bundler/gem_tasks'
Rake::TestTask.new(:test) do |test|
  test.libs << 'test'
  test.test_files = Dir['test/**/test_*.rb']
  test.verbose = true
end

desc 'Run tests for all'
task :default => :test

desc 'Generate documentation for the Sinatra decorator'
task :doc do
  YARD::CLI::Yardoc.new.run
end

desc 'Open an irb session preloaded with the gem library'
task :console do
  sh 'irb -rubygems -I lib -r sintra-decorator'
end
task :c => :console
