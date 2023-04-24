# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative "config/application"

namespace :assets do
  task :precompile do
    Rake::Task["assets:clean"].invoke
    ENV["RAILS_ENV"] ||= "production"
    system("rake assets:precompile")
  end
end

Rails.application.load_tasks
