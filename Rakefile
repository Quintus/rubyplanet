# -*- ruby -*-

task :update do
  sh "bundle exec pluto -c config update rubyplanet.ini"
end

task :build do
  sh "bundle exec pluto -c config build -o public rubyplanet.ini"
  cd "public" do
    ln_sf "rubyplanet.html", "index.html"
  end
end

task :default => [:update, :build]
