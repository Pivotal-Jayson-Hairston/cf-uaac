# CloudFoundry UAA Command Line Client

[![Build Status](https://travis-ci.org/cloudfoundry/cf-uaac.svg?branch=master)](https://travis-ci.org/cloudfoundry/cf-uaac)
[![Gem Version](https://badge.fury.io/rb/cf-uaac.png)](https://rubygems.org/gems/cf-uaac)

## Installation

From Rubygems:

`gem install cf-uaac`

Or to build and install the gem:

```
bundle install
gem build cf-uaac.gemspec
gem install cf-uaac*.gem
```

## Run it

    $ uaac help
    $ uaac target uaa.cloudfoundry.com
    $ uaac token get <your-cf-username>
    $ uaac token decode

To use the APIs, see: https://github.com/cloudfoundry/cf-uaa-lib

## Tests

Run the tests with rake:

    $ bundle exec rake test

Run the tests and see a fancy coverage report:

    $ bundle exec rake cov

Run integration tests (on a server running on localhost:8080/uaa):

    $ export UAA_CLIENT_ID="admin"
    $ export UAA_CLIENT_SECRET="adminsecret"
    $ export UAA_CLIENT_TARGET="http://localhost:8080/uaa"
    $ bundle exec rake test
