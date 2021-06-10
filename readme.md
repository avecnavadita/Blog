# [Using Jekyll with Bundler](https://jekyllrb.com/tutorials/using-jekyll-with-bundler/)

Install [Ruby](https://www.ruby-lang.org/en/) and [Bundler](https://bundler.io/)

## Initialize Bundler

Make sure bundler is installed and enter the following into the shell. It will create a special file `.Gemfile` where all your project dependencies will be stored.

```
bundle init
```

## Add Jekyll

Use Bundler to add Jekyll as a dependency of our new project. This command will add the Jekyll gem to our `Gemfile` created above.

```
bundle add jekyll
```

## [Buldle Install](https://bundler.io/v2.2/man/bundle-install.1.html)

```
bundle install
```

If this is the first time you run `bundle install` (and a `Gemfile.lock` does not exist), Bundler will fetch all remote sources, resolve dependencies and install all needed gems.

However, if a `Gemfile.lock` does exist, and you have not updated your Gemfile, Bundler will fetch all remote sources, but use the dependencies specified in the Gemfile.lock instead of resolving dependencies.


## Gemfile

Gemfile - A format for describing gem dependencies for Ruby programs.

Place the Gemfile in the root of the directory containing the associated code.

At the top of the Gemfile, add a line for the Rubygems source that contains the gems listed in the Gemfile.

```source "https://rubygems.org"```

If your application requires a specific Ruby version or engine, specify your requirements using the ruby method.

```ruby "1.9.3"```

## Create A Jekyll Scaffold

```

Scaffold new Jekyll site and install the dependencies.

bundle exec jekyll new --force --skip-bundle .
bundle install
```

Use the `--force` parameter if the folder already has some files in it

## Serve the Site

Our new website is ready! We can serve the website with 

```
bundle exec jekyll serve
``` 

and visit it at `http://127.0.0.1:4000`

## Bundler

[Bundler](https://bundler.io/) provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.

Bundler is an exit from dependency hell, and ensures that the gems you need are present in development, staging, and production. Starting work on a project is as simple as bundle install

Getting started with bundler is easy! Open a terminal window and run this command:

```
gem install bundler
```
Specify your dependencies in a Gemfile in your project's root:

```
source 'https://rubygems.org'
gem 'nokogiri'
gem 'rack', '~> 2.0.1'
gem 'rspec'
```

Install all of the required gems from your specified sources:

```
bundle install
git add Gemfile Gemfile.lock
```