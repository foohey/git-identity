git-identity
============

You often use Git in different contexts, like at work and for open-source
projects. You may then want to use different user names/email pairs to identify
yourself.

This is not an important part of your work, and setting this up should be really
fast. That's where `git-identity` comes in: setting up your identity information only takes one command with it.

Installing
----------

Simply link or copy the `git-identity` in a directory that's in your `PATH`, Git
will pick it up and make it available as `git identity`.

    $ ln -s git-identity ~/bin/git-identity

Then you may setup a default identity with the following command (see Usage for
more information):

    $ git identity --define default Me me@example.org

Usage
-----

Print the current identity:

    $ git identity
    Current identity: [default] user <user@example.org>

Change identity:

    $ git identity user2
    Using identity: [default2] user2 <user2@example.org>

Listing identities:

    $ git identity --list
    Available identities:
    [default] user <user@example.org>
    [default2] user2 <user2@example.org>

Adding an identity:

    $ git identity --define <identity name> <user name> <user email>

Deleting an identity:

    $ git identity --remove <identity name>
