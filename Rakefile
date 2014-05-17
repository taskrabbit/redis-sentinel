#!/usr/bin/env rake
require "bundler/gem_tasks"

require "rake"
require "rdoc/task"
require "rspec"
require "rspec/core/rake_task"


RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = "spec/redis-sentinel/client_spec.rb"
end

RSpec::Core::RakeTask.new('spec:progress') do |spec|
  spec.rspec_opts = %w(--format progress)
  spec.pattern = "spec/**/*_spec.rb"
end

task :console do
  require 'irb'
  require 'irb/completion'
  require 'redis-sentinel'
  ARGV.clear
  IRB.start
end

task :default => :spec
