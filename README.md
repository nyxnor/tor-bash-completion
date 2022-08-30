# tor bash completion

- It can complete all options with **Tor version 0.4.7.8**.
  - As tor `--help` message does not provide options and recommends to check the manual, so bash-completion `_parse_help()` does not work, this can lead to outdated futured versions of options, as these options were manually inserted.
  - As for `--list-torrc-options`, it is complete and will bring all available torrc options for the cli.
- It can not complete all possible arguments, because that is would be too much work for one person and would be much better if made by upstream.
  - Completing file path, directory, boolean values or few arguments are easy to deal with, but more advanced arguments that involve [addr:]port are better dealt if manually typed.

Note: Windows options were purposefully not set.

## Notice

Not endorsed by the Tor Project Organization.


## History

Tired of typying the full options, I created this bash completion for tor.
It is far from perfect, but it does the basics.


## Requirements

- **tor**
- **bash-completion**


## Installation

1. Add [tor](./tor) to `/usr/share/bash-completion/completions/` directory.
2. Source the completions with `source /usr/share/bash-completion/bash_completion`
3. Run `tor --<TAB><TAB>`
