# runit - a UNIX init scheme with service supervision

You can read about runit info on [runit website](http://smarden.org/runit).

Other helpful info is on [Void Linux Handbook](https://docs.voidlinux.org/config/services/index.html)

So you can grab the folder of service you need in here, put it in `/etc/sv/` or somewhere you like.

Then you can enable it by create a symlink to the service directory in `/var/service/`:

`# ln -s /etc/sv/<service> /var/service/`

This will automatically start the service.
