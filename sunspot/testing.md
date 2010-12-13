#RVM
We will use a gemset sunspot. To use it: rvm use 1.8.7@sunspot

# Testing `sunspot`
Note: All the paths mentioned in here are relative to the current directory, or `sunspot/sunspot_rails`.

The `sunspot` gem is tested with RSpec, and its spec suite is located in `spec`.
## Install dependencies

Each application uses Bundler to manage its dependencies. The `Gemfile` also installs the `sunspot` and `sunspot_rails` gems from your copies checked out locally. Because Bundler expands the full path to `sunspot` and `sunspot_rails`, we're excluding its generated `Gemfile.lock` file from version control.

cd sunspot
bundle install


## Start Solr

Specs expect to connect to Solr on `http://localhost:8983/solr`

bundle exec sunspot-solr run -p 8983


## Invoke specs

bundle exec spec spec/
                                                 
