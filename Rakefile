require 'html/proofer'

task :test do
  sh "bundle exec jekyll build"
  
  ignored = [
    /royalmail.com/
  ]
  
  HTML::Proofer.new("./_site", ssl_verifypeer: false, timeout: 30, href_ignore: ignored, check_html: true).run
end

task :default => :test