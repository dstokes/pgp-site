---
layout: page
title: PGP - Setup
sections:
  - install
  - key-generation
---
{: .page-header}
# Install {#install}
For the purpose of simplicity on this site, we'll deal exclusively with using
the GNU open source implementation of the OpenPGP protocol, GnuPG.

### Mac
Macs come with a default command-line GPG installation, but you'll want to
upgrade to GPG2 for the latest bells and whistles. The easiest way to do so is
to grab a copy of [Homebrew](http://brew.sh/) and run the following:

    $ brew install gpg2

If you prefer working with graphical interfaces you can install [GPG Tools](https://gpgtools.org/).

{: .page-header}
# Key Generation {#key-generation}
Issue the following command to begin generating a GnuPG key pair:

    $ gpg --gen-key

This will take you through a couple of questions that will be used to configure your keys.

- Please select what kind of key you want: **(1) RSA and RSA (default)**
- What keysize do you want? **4096**
- Key is valid for? **0**
- Is this correct? **y**
- Real name: **your real name**
- Email address: **your_email@address.com**
- Comment: **Optional comment that will be visible in your signature**
- Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? **O**
- Enter passphrase: **Enter a secure passphrase here (upper & lower case, digits, symbols)**

At this point, GnuPG will begin to generate the keys which may take some time.
