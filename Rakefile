require 'rubygems'
require 'rake'
require 'rdoc'
require 'date'
require 'yaml'

desc "Serve the site locally"
task :serve do
  system "bundle exec jekyll serve -w"
end

desc "Generate blog files"
task :build do
  system "bundle exec jekyll build"
end

desc "Generate and publish"
task :publish do
  system "git push origin master"
  system "echo yolo"
end

task :default => :publish

