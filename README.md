# Mollusk (`fish` + `xonsh`)

The best parts of `fish` and the best parts of `xonsh`. I really like `xonsh`,
but `fish`'s was way superior to `xonsh`'s. But I also love the fact that
`xonsh` has its whole state as Python objects. So I decided to combine the two.

This code is 100% garbage. It's very hacky, spawning a new fish shell for
every command, and yet is still faster than xonsh on its commands.

## Installation
 1. Add the contents of the configuration files in `fish_config` to your files
    in `~/.config/fish/`. Since configuration files are so complex, there is
    no way to do this automatically.

 2. Put `mollusk` and `mollusk-relay` in `/usr/bin/` or somewhere in your path.
    Make sure that `fish` can find `mollusk` and `mollusk-relay` wherever they
    may be.

 3. Try it out, see it break.

## TODO
 - Fix syntax highlighting
 - Multi-line command support
 - Robustness against breaking the internal xonsh interpreter
 - Fix end of file not terminating shell
 - Probably combine `mollusk` and `mollusk-relay`

## Laments
Sadly I can't change `$SHELL` to `/usr/bin/mollusk`. This is because `xonsh`
is what is actually running the commands.

