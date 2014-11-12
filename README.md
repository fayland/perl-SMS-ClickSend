[![Build Status](https://travis-ci.org/fayland/perl-SMS-ClickSend.svg?branch=master)](https://travis-ci.org/fayland/perl-SMS-ClickSend)
[![Coverage Status](https://coveralls.io/repos/fayland/perl-SMS-ClickSend/badge.png?branch=master)](https://coveralls.io/r/fayland/perl-SMS-ClickSend?branch=master)
[![Gitter chat](https://badges.gitter.im/fayland/perl-SMS-ClickSend.png)](https://gitter.im/fayland/perl-SMS-ClickSend)

# NAME

SMS::ClickSend - SMS gateway for clicksend.com

# SYNOPSIS

    use SMS::ClickSend;

    my $sms = SMS::ClickSend->new(
        username => 'username',
        api_key  => 'API_KEY...',
    );

    my $res = $sms->send(
        to => '+61411111111',
        message => 'This is the message',
    );
    print Dumper(\$res); use Data::Dumper;

# DESCRIPTION

SMS::ClickSend is a sms gateway for [http://clicksend.us/](http://clicksend.us/)

API can be found at [http://developers.clicksend.com/api/rest/](http://developers.clicksend.com/api/rest/)

# METHODS

## new

- username
- api\_key

    can be found at [https://my.clicksend.com/sms\_settings\_subaccounts.php](https://my.clicksend.com/sms_settings_subaccounts.php)

## send

    $sms->send(
        to => '+61411111111',
        message => 'This is the message',
    );

more details can be found at [http://developers.clicksend.com/api/rest/](http://developers.clicksend.com/api/rest/)

## reply

## delivery

    $sms->delivery('70A1EFA4-3F61-9D72-556C-D918FF3FC41');

## balance

    $sms->balance();
    $sms->balance('AU');

## history

    $sms->history();

# AUTHOR

Fayland Lam <fayland@gmail.com>

# COPYRIGHT

Copyright 2014- Fayland Lam

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO
