#
# Copyright (c) 2014 by Lifted Studios. All Rights Reserved.
#

require 'rspec/core/rake_task'
require 'rubocop/rake_task'
require 'yard'

task :default => [:test, :doc]

desc 'Generate documentation'
task :doc => 'doc:yard'

desc 'Execute all tests'
task :test => ['test:rubocop', 'test:spec']

namespace :doc do
  YARD::Rake::YardocTask.new
end

namespace :test do
  Rubocop::RakeTask.new

  RSpec::Core::RakeTask.new do |spec|
    spec.verbose = false
  end
end
