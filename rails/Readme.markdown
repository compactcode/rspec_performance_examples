# 1.9.2

```
rvm use 1.9.2@compactcode --create && gem install bundler && bundle install
time bundle exec rake spec                6.48s
time rake spec                            6.01s
time rspec spec                           3.18s
time rspec spec/models/example_spec.rb    3.21s
time rspec spec/lib/without_rails_spec.rb 0.20s
```

# 1.8.7

```
rvm use 1.8.7@compactcode --create && gem install bundler && bundle install

time bundle exec rake spec                 2.62s
time rake spec                             2.36s
time rspec spec                            1.01s
time rspec spec/models/example_spec.rb     1.00s
time rspec spec/lib/without_rails_spec.rb  0.09s
```
