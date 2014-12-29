require 'rubygems'
require 'optparse'
require 'yaml'

task :np do
  OptionParser.new.parse!
  ARGV.shift
  title = ARGV.join(' ')

  path = "_posts/#{Date.today}-#{title.downcase.gsub(/[^[:alnum:]]+/, '-')}.md"
  
  if File.exist?(path)
    puts "[WARN] File exists - skipping create"
  else
    File.open(path, "w") do |file|
      file.puts YAML.dump({'layout' => 'post', 'published' => false, 'title' => title})
      file.puts "tags: [tag1,tag2,tag3]"
      file.puts "---"
    end
  end
  system("/usr/local/bin/vim #{path}")  

  exit 1
end
