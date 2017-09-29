require 'rubygems'
require 'rake'
require 'rdoc'
require 'date'
require 'yaml'

desc "Serve the site locally"
task :serve do
  system "bundle exec jekyll serve -P 4001 -w --drafts --config _config.yml,_config-dev.yml"
end

desc "Generate blog files"
task :build do
  system "bundle exec jekyll build"
end

desc "Generate and publish"
task :publish => :build do
  system "git push origin master"
  system "echo yolo"
end

task :default => :publish

