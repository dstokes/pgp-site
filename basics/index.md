---
layout: page
title: PGP - Basics
sections:
  - public-keys
---
{: .page-header}
# Key Management
GnuPG uses a keyring to manage public and private keys. Getting familiar
with some basic tasks is the first step in upping your PGP game.

### Working With Public Keys {#public-keys}
You need to share your public key with your colleagues before they can
encrypt data to you. You can do so by publishing your key to a key server, or
exporting and sending it directly to them.

You can list your current public keys with the following command:

    $ gpg --list-keys
    /path/to/home/.gnupg/pubring.gpg
    --------------------------------
    pub   4096R/4758CCAF 2016-01-01 [expires: 2020-01-01]
    uid       [ultimate] John Doe <john@doe.com>
    sub   4096R/BFD256FF 2015-10-21 [expires: 2020-01-01]

Note the key id of the key you want and export it a file:

    $ gpg --armor --export 4758CCAF > key.pub

Now distribute <code>key.pub</code> so others can encrypt messages to you.
