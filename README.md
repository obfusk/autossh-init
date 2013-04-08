[]: {{{1

    File        : README.md
    Maintainer  : Felix C. Stegerman <flx@obfusk.net>
    Date        : 2013-04-08

    Copyright   : Copyright (C) 2013  Felix C. Stegerman
    Version     : 0.0.1

[]: }}}1

## TODO

  * test!

## Description
[]: {{{1

  autossh-init - AutoSSH init script

[]: }}}1

## Usage
[]: {{{1

    $ cp -i autossh.init /etc/init.d/autossh
    $ update-rc.d autossh defaults

    $ cp -i autossh.default /etc/default/autossh
    $ vim /etc/default/autossh

    $ adduser --system --group --shell /bin/false \
      --home /nonexistent --no-create-home \
      --disabled-password autossh

    $ sudo -H -u autossh ssh-keygen

    $ service autossh start

[]: }}}1

## License
[]: {{{1

  GPLv2 [1].

[]: }}}1

## References
[]: {{{1

  [1] GNU General Public License, version 2
  --- http://www.opensource.org/licenses/GPL-2.0

[]: }}}1

[]: ! ( vim: set tw=70 sw=2 sts=2 et fdm=marker : )
