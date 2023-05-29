task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  desc 'outputs hello from rake in the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola in the terminal'
  task :hola do
    puts "hola de Rake!"
  end

  desc 'outputs hello to the terminal'
  task :helll do
    puts "Hello Rake!"
  end
end

namespace :db do
  desc 'migrates changes to database'
  task :environment do
    require_relative './config/environment'
  end

  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end
