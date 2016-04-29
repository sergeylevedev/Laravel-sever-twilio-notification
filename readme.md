# Server Notifications & Alerts with Twilio and Laravel

[![Build Status](https://travis-ci.org/TwilioDevEd/server-notifications-laravel.svg?branch=master)](https://travis-ci.org/TwilioDevEd/server-notifications-laravel)

Use Twilio to create SMS alerts so that you never miss a critical issue.

[Read the full tutorial here](https://www.twilio.com/docs/tutorials/walkthrough/server-notifications/php/laravel)!

## Running the application

Clone this repository and cd into the directory.

1. Install the application's dependencies with [Composer](https://getcomposer.org/)
   ```
   $ composer update
   ```

1. Set the application's configuration variables. You can find your
account's SID and authentication token in your
[Twilio account](https://www.twilio.com/user/account/voice-messaging)
You'll need to set the `TWILIO_AUTH_TOKEN`, `TWILIO_ACCOUNT_SID`, and
`TWILIO_NUMBER` environment variables. The easiest way to accomplish
this is using the `export` command.

   ```bash
   $ export TWILIO_ACCOUNT_SID=your account sid
   ```
   ```bash
   $ export TWILIO_AUTH_TOKEN=your auth token
   ```
   ```bash
   $ export TWILIO_NUMBER=+16515559999
   ```

   For the `TWILIO_NUMBER` variable you'll need to provision a new number
   in the
   [Manage Numbers page](https://www.twilio.com/user/account/phone-numbers/incoming)
   under your Twilio account. The phone number should be in
   [E.164 format](https://www.twilio.com/help/faq/phone-numbers/how-do-i-format-phone-numbers-to-work-internationally)

1. Run the application using Artisan.

   ```bash
   $ php artisan serve
   ```

1. Customize `config/administrators.json` with your name and phone number.

1. Finally visit the application's error route at
   [http://localhost:8000/error](http://localhost:8000/error). You'll
   soon get a message informing you of an error.

## Dependencies

This application uses this Twilio helper library:
* [twilio-php](https://github.com/twilio/twilio-php)

### Run the tests

Run `phpunit` at the top level directory.
