###Email Match (Ruby)

```ruby
# from rails docs
/\A([^@\s]+)@((?:[-a-z0-9]+\.)+[a-z]{2,})\z/i
```

###URL Match (Ruby)

```ruby
# http://mbleigh.com/2009/02/18/quick-tip-rails-url-validation.html
/\A#{URI::regexp(%w(http https))}\z/
```
