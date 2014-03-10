# -*- ruby -*-

desc "Retrieve new posts."
task :update do
  sh "bundle exec pluto -c config update rubyplanet.ini"
end

desc "Recreate HTML pages."
task :merge do
  sh "bundle exec pluto -c config merge -o public rubyplanet.ini"
end

desc "Retrieve new posts, then recreate HTML pages."
task :sync => [:update, :merge]

desc "Same as :sync."
task :default => [:sync]
