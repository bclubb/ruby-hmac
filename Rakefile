require 'rubygems'
$:.unshift(File.dirname(__FILE__) + "/lib")
require 'hmac'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "ruby-hmac"
    gemspec.authors = ["Daiki Ueno", "Geoffrey Grosenbach", "Brian Clubb"]
    gemspec.description = "A MAC provides a way to check the integrity of information transmitted over or stored in an unreliable medium, based on a secret key."
    gemspec.summary = "An implementation of the HMAC authentication code in Ruby."
    gemspec.email = "bclubb@gmail.com"
    gemspec.homepage = "http://www.github.com/bclubb/ruby-hmac"
    gemspec.files = FileList['lib/**/*.rb']
    gemspec.test_files = []
  end
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install technopickles-jeweler -s http://gems.github.com"
end

desc "Simple require on packaged files to make sure they are all there"
task :verify => :package do
  # An error message will be displayed if files are missing
  if system %(ruby -e "require 'pkg/ruby-hmac-#{HMAC::VERSION}/lib/hmac'")
    puts "\nThe library files are present"
  end
end

#task :release => :verify
