# tmux-sessionaire

A small bash script that opens a tmux session with a fixed three-pane
layout. If the session already exists, it attaches to it (or switches to it
when run inside tmux).

## Requirements

- bash
- tmux 3.1 or later

## Install

Clone the repo and make the script available on your shell, for example with
an alias:

```sh
alias tmux-s='~/path/to/tmux-sessionaire/tmux-sessionaire.sh'
```

## Usage

With the alias:

```sh
tmux-s
```

Or run the script directly:

```sh
./tmux-sessionaire.sh
```

The session has one window with a large main pane, a narrow pane on the right
and a short pane along the bottom. The main pane is selected.

Override the defaults with environment variables:

| Variable       | Default |
| -------------- | ------- |
| `SESSION_NAME` | `dev`   |
| `WINDOW_NAME`  | `main`  |

```sh
SESSION_NAME=work ./tmux-sessionaire.sh
```

## License

[MIT](LICENSE)
