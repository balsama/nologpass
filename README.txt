Overview
--------

It is common for users to accidentally enter their password in the username
field of login forms. Often, the username field will have something like this
when it is submitted: `usernamepassword`. By default, Drupal stores these
failed login attempts in the watchdog table. Effectively, this stores passwords
in plain text in the database.

This module adds an extra check before writing this message to the table. If
the provided username is not a valid user, the IP address is stored instead of
the username field.

`Login attempt failed for adminpassword.` becomes
`Login attempt failed from 127.0.0.1.`.

Installation
------------

See http://drupal.org/node/70151 for information on installing modules.


Configuration
-------------

There are no configurable options for this module.
