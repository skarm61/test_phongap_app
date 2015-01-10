# Sample guardfile block for Guard::Haml
# You can use some options to change guard-haml configuration
# output: 'public'                   set output directory for compiled files
# input: 'src'                       set input directory with haml files
# run_at_start: true                 compile files when guard starts
# notifications: true                send notifictions to Growl/libnotify/Notifu
# haml_options: { ugly: true }    pass options to the Haml engine

guard :haml, input: 'sources/pages', output: 'www/pages', run_at_start: true do
  watch(/^.+(\.html\.haml)$/)
end

coffeescript_options = {
  input: 'sources/coffee',
  output: 'www/js',
  patterns: [%r{^sources/coffee/(.+\.coffee)$}]
}

guard 'coffeescript', coffeescript_options do
  coffeescript_options[:patterns].each { |pattern| watch(pattern) }
end

# guard :coffeescript, input: 'sources/coffee', output: 'www/js', all_on_start: true do
#   watch(%r{^sources/coffee/(.+\.coffee)$})
# end

# guard :coffeescript, input: 'sources/coffee', output: 'www/js' do
#   watch(%r{^sources/coffee/(.+\.coffee)$})
# end
# guard :coffeescript
