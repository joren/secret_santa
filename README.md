# Secret Santa Script

This is a simple Ruby script for assigning secret Santas and emailing everyone their assignment. The basic rule is that nobody can be assigned to give a gift to someone in their own group (including, of course, themselves). In my family, group == household, but it could mean anything you like.

The script uses Dennis Ranke's solution from [The Ruby Quiz #2](http://www.rubyquiz.com/quiz2.html), which gives everyone a correct assignment in a single pass through the list. Nice! :) The only tweaks I made were practical ones, like using config files, and a tiny bit of refactoring, logging, etc, to make it more apparent what's happening.

## Usage

- Clone the repo
- Copy each of the `.yml.example` files in `config/` to a corresponding `.yml` and customize
- Run `ruby secret_santa.rb` and examine the output
- When you're satisfied, set `REALLY_SENDING` to `true` and run it again

## Optional Twilio setup and usage

- Fill in your own Twilio credentials in the `twilio.yml` config file
- Change `SENDER_TYPE` to `:twilio`
- Set `REALLY_SENDING` to `false` to disable really sending text messages or to `true` to really send text messages.

!! Depending on your Twilio account settings, sending text messages may costs money.

## Dependencies

None, other than Ruby (I tested on 1.9) and the standard library.

If you want to use Twilio as sender type, you need to install the twilio-ruby gem:

``gem install twilio-ruby'``

## Thanks

Thanks to Dennis Ranke for a nice solution, and to James Edward Gray II for running The Ruby Quiz.
