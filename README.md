I use this to build an ISO for doing work using my offline pgp key.

If you want to know more information about offline pgp master keys and subkeys, this is the guide I'm following:
http://blog.josefsson.org/2014/06/23/offline-gnupg-master-key-and-subkeys-on-yubikey-neo-smartcard/

To build an ISO, run the following:

```
$ vagrant up
$ vagrant ssh
$ cd /vagrant
$ sudo lb build
```

This will create a file called `live-image-amd64.hybrid.iso` in `/vagrant`. Use `dd` to copy that to a thumb drive or burn it to a CD or DVD and enjoy!

Note that local changes inside the vagrant box won't end up on clone you started the vagrant box from because debian's vagrant boxes don't have virtualbox extensions and such, so it just rsyncs the working directory into /vagrant at first-run and uses that.


