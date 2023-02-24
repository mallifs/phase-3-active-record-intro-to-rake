namespace :greeting do
desc 'output hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end

end

#rake db:migrate

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end
end

task :environment do
  require_relative './config/environment'
end

#rake db:seed
namespace :db do

  # ...

  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

#rake console

desc 'drop into the pry console'
task console: :environment do
  pry.start
end

