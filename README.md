SpreePromoUsersCodes
=====================

SpreePromoUsersCodes is an extension for spree admins to generate customised coupon codes for their customers. It enables the admin to create coupon codes for each promotion by marking it as multi-coupon and creating unique codes for the customers he/she wants to send the codes to. The codes are e-mailed to the customer so the code is known only to him/her.

Installation
------------

Add spree_promo_users_codes to your Gemfile:

```ruby
gem 'spree_promo_users_codes',   github: 'vinsol-spree-contrib/spree_promo_users_codes',   branch: 'master'
```

Bundle your dependencies and run the installation generator:

```shell
bundle
bundle exec rails g spree_promo_users_codes:install
```

Usage
-----

It creates a new CRUD for promotion codes. Every promotion that is marked as multi-coupon can have a unique code for each customer of the site.

The codes are non-editable, so once generated, a code remains in existence unless explicitly destroyed by the admin. Usage rules are same as those for promotions. If there is no usage limit, any number of codes can be created; but, if there is a usage limit on the promotion, only those many coupon codes can be validated. Please note that the generated codes are one-time usable, and only by the designated customer.

Contributing
------------

1. Fork the repository.
2. Clone your repository.
3. Run `bundle install`.
4. Run `bundle exec rake test_app` to create the test application in `spec/test_app`.
5. Make the required changes.
6. Ensure all specs pass by running `bundle exec rspec spec`.
7. Submit your pull request.

Testing
-------

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run the rspecs. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

Copyright (c) 2016 VinSol, released under the New BSD License.
