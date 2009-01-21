require 'rubygems'
require 'rake/gempackagetask'
require 'rubygems/specification'
require 'date'
require 'merb-core/version'
require 'merb-core/tasks/merb_rake_helper'

GEM = "merb-sequel-stack"
GEM_VERSION = "1.0.3"
AUTHOR = "Jack Dempsey"
EMAIL = "jack.dempsey@gmail.com"
HOMEPAGE = "http://jackndempsey.blogspot.com"
SUMMARY = "(merb-core + merb-more + Sequel) == Merb Sequel stack"

gems = [
  ["merb-core", "~> #{GEM_VERSION}"],
  ["merb-more", "~> #{GEM_VERSION}"],
  ["sequel", "~> 2.7.0"],
  ["merb_sequel", "~> 1.0"]
]
merb_spec = Gem::Specification.new do |s|
  s.rubyforge_project = 'merb-ar-stack'
  s.name = GEM
  s.version = GEM_VERSION
  s.platform = Gem::Platform::RUBY
  s.has_rdoc = true
  s.extra_rdoc_files = ["README.markdown", "LICENSE", 'TODO']
  s.summary = SUMMARY
  s.description = s.summary
  s.author = AUTHOR
  s.email = EMAIL
  s.homepage = HOMEPAGE
  
  s.require_path = 'lib'
  s.files = %w(LICENSE README.markdown Rakefile TODO Generators) + Dir.glob("{lib,spec}/**/*")
  gems.each do |gem, version|
    s.add_dependency gem, version
  end
end

Rake::GemPackageTask.new(merb_spec) do |pkg|
  pkg.gem_spec = merb_spec
end

desc "Install the gem"
task :install do
  Merb::RakeHelper.install(GEM, :version => GEM_VERSION)
end

desc "Uninstall the gem"
task :uninstall do
  Merb::RakeHelper.uninstall(GEM_NAME, :version => GEM_VERSION)
end

desc "create a gemspec file"
task :make_spec do
  File.open("#{NAME}.gemspec", "w") do |file|
    file.puts spec.to_ruby
  end
end
