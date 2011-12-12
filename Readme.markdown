# Examples showing the performance of rspec tests in various situations.

Doing TDD on a modern rails application is a painful exercise. Make a 2 second change to a spec, run it, wait 6 seconds to get the results. This project is a collection of small experiments exploring the slowdown caused by common tools used during development.

All tests performed on a 2GHz Intel Core i7 MacBook Pro running OSX Snow Leopard. Tests use mri 1.9.2-p290 unless stated otherwise.

## Bundler

Bundler is fantastic for managing gem dependancies but it does add `significant` overhead when executing scripts.

```
time ls -a              0.00s
time bundle exec ls -a  0.64s
```

Consider setting up isolated environment so you can avoid the need to use bundler.

```
rvm use 1.9.2@isolated --create && gem install bundler && bundle install
```

## Rails

Rails is woefully slow (especially on 1.9.2).

There are a bunch of examples for rails in the stock_standard_rails directory.

I highly recommend watching this awesome screencast by [https://www.destroyallsoftware.com/screencasts/catalog/fast-tests-with-and-without-rails](Destroy All Software)
