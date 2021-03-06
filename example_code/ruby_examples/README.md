# swagger_client

SwaggerClient - the Ruby gem for the Cisco PSIRT openVuln API

The Cisco Product Security Incident Response Team (PSIRT) openVuln API is a RESTful API that allows customers to obtain Cisco Security Vulnerability information in different machine-consumable formats. APIs are important for customers because they allow their technical staff and programmers to build tools that help them do their job more effectively (in this case, to keep up with security vulnerability information). For more information about the Cisco PSIRT openVuln API visit https://developer.cisco.com/psirt  For detail steps on how to use the API go to: https://developer.cisco.com/psirt  This is a beta release of a swagger YAML for the Cisco PSIRT openVuln API  To access the API sign in with your Cisco CCO account at http://apiconsole.cisco.com and register an application to recieve a client_id and a client_secret  You can then get your token using curl or any other method you prefer.  'curl -s -k -H \"Content-Type: application/x-www-form-urlencoded\" -X POST -d \"client_id=<your_client_id>\" -d \"client_secret=<your_client_secret>\" -d \"grant_type=client_credentials\" https://cloudsso.cisco.com/as/token.oauth2'  You will receive an access token as demonstrated in the following example:  '{\"access_token\":\"I7omWtBDAieSiUX3shOxNJfuy4J6\",\"token_type\":\"Bearer\",\"expires_in\":3599}'  In Swagger, click on Change Authentication  enter the text \"I7omWtBDAieSiUX3shOxNJfuy4J6\" (which is the token you received)  then click on \"Try this operation\" 

This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 0.0.4
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.RubyClientCodegen

## Installation

### Build a gem

To build the Ruby code into a gem:

```shell
gem build swagger_client.gemspec
```

Then either install the gem locally:

```shell
gem install ./swagger_client-1.0.0.gem
```
(for development, run `gem install --dev ./swagger_client-1.0.0.gem` to install the development dependencies)

or publish the gem to a gem hosting service, e.g. [RubyGems](https://rubygems.org/).

Finally add this to the Gemfile:

    gem 'swagger_client', '~> 1.0.0'

### Install from Git

If the Ruby gem is hosted at a git repository: https://github.com/YOUR_GIT_USERNAME/YOUR_GIT_REPO, then add the following in the Gemfile:

    gem 'swagger_client', :git => 'https://github.com/YOUR_GIT_USERNAME/YOUR_GIT_REPO.git'

### Include the Ruby code directly

Include the Ruby code directly using `-I` as follows:

```shell
ruby -Ilib script.rb
```

## Getting Started

Please follow the [installation](#installation) procedure and then run the following code:
```ruby
# Load the gem
require 'swagger_client'

# Setup authorization
SwaggerClient.configure do |config|
  # Configure OAuth2 access token for authorization: psirt_openvuln_api_auth
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = SwaggerClient::DefaultApi.new

advisory_id = "advisory_id_example" # String | advisory ID


begin
  api_instance.security_advisories_advisory_advisory_id_get(advisory_id)
rescue SwaggerClient::ApiError => e
  puts "Exception when calling DefaultApi->security_advisories_advisory_advisory_id_get: #{e}"
end

```

## Documentation for API Endpoints

All URIs are relative to *https://api.cisco.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*SwaggerClient::DefaultApi* | [**security_advisories_advisory_advisory_id_get**](docs/DefaultApi.md#security_advisories_advisory_advisory_id_get) | **GET** /security/advisories/advisory/{advisory_id} | 
*SwaggerClient::DefaultApi* | [**security_advisories_all_get**](docs/DefaultApi.md#security_advisories_all_get) | **GET** /security/advisories/all | 
*SwaggerClient::DefaultApi* | [**security_advisories_cve_cve_id_get**](docs/DefaultApi.md#security_advisories_cve_cve_id_get) | **GET** /security/advisories/cve/{cve_id} | 
*SwaggerClient::DefaultApi* | [**security_advisories_ios_get**](docs/DefaultApi.md#security_advisories_ios_get) | **GET** /security/advisories/ios | 
*SwaggerClient::DefaultApi* | [**security_advisories_iosxe_get**](docs/DefaultApi.md#security_advisories_iosxe_get) | **GET** /security/advisories/iosxe | 
*SwaggerClient::DefaultApi* | [**security_advisories_latest_number_get**](docs/DefaultApi.md#security_advisories_latest_number_get) | **GET** /security/advisories/latest/{number} | 
*SwaggerClient::DefaultApi* | [**security_advisories_product_get**](docs/DefaultApi.md#security_advisories_product_get) | **GET** /security/advisories/product | 
*SwaggerClient::DefaultApi* | [**security_advisories_severity_severity_firstpublished_get**](docs/DefaultApi.md#security_advisories_severity_severity_firstpublished_get) | **GET** /security/advisories/severity/{severity}/firstpublished | 
*SwaggerClient::DefaultApi* | [**security_advisories_severity_severity_get**](docs/DefaultApi.md#security_advisories_severity_severity_get) | **GET** /security/advisories/severity/{severity} | 
*SwaggerClient::DefaultApi* | [**security_advisories_severity_severity_lastpublished_get**](docs/DefaultApi.md#security_advisories_severity_severity_lastpublished_get) | **GET** /security/advisories/severity/{severity}/lastpublished | 
*SwaggerClient::DefaultApi* | [**security_advisories_year_year_get**](docs/DefaultApi.md#security_advisories_year_year_get) | **GET** /security/advisories/year/{year} | 


## Documentation for Models



## Documentation for Authorization


### psirt_openvuln_api_auth

- **Type**: OAuth
- **Flow**: implicit
- **Authorization URL**: https://cloudsso.cisco.com/as/token.oauth2
- **Scopes**: 
  - read:advisories: read advisories

