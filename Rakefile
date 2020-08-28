
require 'yaml'

desc "increment value"
task :inc do
  fname = 'value.yml'
  h = YAML.load(File.read(fname)) if File.exist? fname
  h ||= {}
  h[:value] = (h[:value] || 0) + 1
  File.write(fname, YAML.dump(h))
end

task :default => :inc