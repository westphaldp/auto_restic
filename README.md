# auto_restic

`auto_restic` is a wrapper script for [restic](https://github.com/restic/restic), much like [restic-runner](https://github.com/alphapapa/restic-runner), but allowing all operations and configurations to be implemented in configuration files. Though it was designed to enable easy cron folder drop-ins, it should also work well with SystemD unit templates and timers.

## Installation

1. Install `restic`. If reports are desired, also install `jq`.
1. Copy `auto_restic` and `config.env` to the desired locations.
1. Customize the configuration file as desired.
1. Optionally, update the `CONFIG` variable in `auto_restic` to allow easier use.

## Usage

First, initialize the repository. e.g.

	bash -c '. /etc/restic/config.env; restic init;'

If the `CONFIG` variable in `auto_restic` is configured for your configuration file, just run `auto_restic`!

If you'd like to specify the configuration file on the command line, you can do so (e.g. `auto_restic local.env`).

## License

MIT
