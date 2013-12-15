require 'bundler/setup'
require 'travis'

desc 'call travis to build restart'
task :default do
  Travis.access_token = ENV['TRAVIS_TOKEN']
  build = Travis::Repository.find(ENV['TRAVIS_BUILD'])
  build.last_build.restart
end

