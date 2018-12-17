require_relative './config/environment'
require 'sinatra/activerecord/rake'

task :console do
  require 'irb'
  ARGV.clear
  IRB.start
end

namespace :db do
  task :migrate => :environment do
    CreateArtists.new.change
    AddFavoriteFoodToArtists.new.change
  end
end
