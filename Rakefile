require 'html/proofer'

task :test do
  sh "bundle exec jekyll build"
  
  ignored = [
    /royalmail.com/
  ]
  
  HTML::Proofer.new("./_site", typhoeus: {ssl_verifypeer: false, timeout: 30}, href_ignore: ignored, 
                    check_html: true, check_favicon: true).run
end

task :default => :test