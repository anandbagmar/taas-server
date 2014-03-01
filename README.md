taas-server
===========

Sample taas-server usage (Ruby project)

# Sample Steps

Clone repo - git clone git@github.com:anandbagmar/taas-server.git

bundle install

Create / update TaasContracts.yml file

Setup the TaaSContracts path in environment variable
    export contract_file=/Users/anand/Projects/MyProjects/taas-server/resources/TaaSContracts.yml

To start the TaaS server:
    rake taas:start_server

Verify server started:
    http://localhost:4567/

# Test the call
    irb
    require "rubygems"
    require "taas"
    params={:contract_name => "taasDemo", :search_for => "Anand Bagmar"}
    tc=TaaS.client("http://localhost:4567/contract",10000)
    hash,consoleLog=tc.execute_contract(params)

# FAQs
