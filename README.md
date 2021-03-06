[![Build Status](https://travis-ci.org/baxang/coupon-code.svg)](https://travis-ci.org/baxang/coupon-code)
[![Code Climate](https://codeclimate.com/github/baxang/coupon-code/badges/gpa.svg)](https://codeclimate.com/github/baxang/coupon-code)
[![Gem Version](https://badge.fury.io/rb/coupon_code.svg)](http://badge.fury.io/rb/coupon_code)

# CouponCode

[README-한국어][README-kr]

CouponCode gem generates and validates coupon codes. Suitable for e-Commerce sites and businesses who want to issue coupons/vouchers to customers.

It is a Ruby implementation of [Grant][grant]'s [Algorithm::CouponCode][couponcode], so the characteristics and features of this gem is alike. Please read [the original documentation of Algorithm::CouponCode](http://search.cpan.org/dist/Algorithm-CouponCode/lib/Algorithm/CouponCode.pm) for details.

However, please be aware that not all the nice and thoughtful functionality the original CPAN module has are implemented at the moment. Generating codes from a plaintext, auto-correct, and jQuery plugin are not included.

This gem is developed for https://stripes.co.kr

## Installation

Add this line to your application's Gemfile:

    gem 'coupon_code'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install coupon_code

## Synopsis

    >> require 'coupon_code'
    >> code = CouponCode.generate
    => "1K7Q-CTFM-LMTC"
    >> CouponCode.validate(code)
    => "1K7Q-CTFM-LMTC"
    >> CouponCode.validate('1K7Q-CTFM-LMTO') # Invalid code
    => nil

## Testing

```ruby
$ bundle exec rake test
```

## Thanks to

 - [Grant McLean][grant]'s [Algorithm::CouponCode][couponcode] in Perl
 - [Andrew Chilton][chilts]'s [NodeJS implementation][node-couponcode] in JavaScript

## License

MIT. See [LICENSE][license] for more details.

## Contributing

1. Fork it ( https://github.com/baxang/coupon-code/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

[grant]: https://github.com/grantm/
[couponcode]: https://github.com/grantm/Algorithm-CouponCode
[chilts]: https://github.com/chilts
[node-couponcode]: https://github.com/chilts/node-coupon-code
[license]: https://github.com/baxang/coupon-code/blob/master/LICENSE.txt
[README-kr]: https://github.com/baxang/coupon-code/blob/master/README-ko.md