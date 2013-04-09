[]: {{{1

    File        : README.md
    Maintainer  : Felix C. Stegerman <flx@obfusk.net>
    Date        : 2013-04-09

    Copyright   : Copyright (C) 2013  Felix C. Stegerman
    Version     : 0.0.1

[]: }}}1

## TODO

  * test!
  * improve output

## Description
[]: {{{1

  autossh-init - AutoSSH init script

[]: }}}1

## Usage
[]: {{{1

  local & remote:

    $ adduser --system --group --shell /bin/false \
      --home /var/lib/autossh --disabled-password autossh

  local:

    autossh$ ssh-keygen
    # <<PUBKEY>> below is the contents of ~/.ssh/id_rsa.pub here

  remote:

    autossh$ vim ~/.ssh/authorized_keys
    # on a single line, add:
    #   command="/bin/false",no-agent-forwarding,no-pty,
    #   no-X11-forwarding,permitopen="host1:port1",
    #   permitopen="host2:port2" <<PUBKEY>>

  local:

    $ cp -i autossh.init /etc/init.d/autossh
    $ update-rc.d autossh defaults

    $ cp -i autossh.default /etc/default/autossh
    $ vim /etc/default/autossh

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
