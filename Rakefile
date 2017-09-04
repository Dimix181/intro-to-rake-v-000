
namespace :greeting do

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

end

namespace :db do

  desc 'points to dependencies'
  task :environment do
    require_relative 'config/environment'
  end

  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed data for created table'
  task :seed do
    require_relative 'db/seeds'
  end

  desc 'testing pry console'
  task :console => :environment do
    pry.start
  end

end
