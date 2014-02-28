require "taas"

namespace :taas do
  desc 'Start the TaaS Server'
  task :start_server do
    puts "Argument is -> #{ENV['contract_file']}"
    TaaS.start_server(ENV['contract_file'])
  end
end