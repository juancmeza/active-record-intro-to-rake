desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :db do
  desc 'require environment'
  task :environment do
    require_relative './config/environment'
  end

  desc 'migrate changes to database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'create samples'
  task :seed do
    require_relative './db/seeds.rb'
  end

  desc 'drop into the Pry console'
  task :console => :environment do
    Pry.start
  end
end



