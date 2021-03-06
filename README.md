# quick-clone

A convenient utility for quickly cloning repositories.

![demo](https://user-images.githubusercontent.com/85315/167231840-03a85ecc-bf7e-4939-a8d5-52add7bc8fa0.gif)

## Installation

```console
$ deno install \
    --allow-env --allow-read --allow-write --allow-run --unstable --force \
    --name clone \
    https://deno.land/x/quick-clone/cli.ts
```

## Usage

`quick-clone` clones git repositories into a predictable directory structure.

```console
$ clone https://github.com/bentruyman/quick-clone.git
```

The above command clones the `bentruyman/quick-clone` repository into
`~/Development/src/github.com/bentruyman/quick-clone`, then opens your preferred
editor in the cloned directory.

Both `git+ssh` and `https` URLs work:

```console
$ clone git@github.com:bentruyman/quick-clone.git # with git+ssh
$ clone https://github.com/bentruyman/quick-clone.git # with https
```

## Configuration

`quick-clone` can be configured with the following environment variables:

- `EDITOR`: program to open cloned repos in if `$VISUAL` is undefined
- `SRC_ROOT`: root directory to clone repositories into (default:
  `$HOME/Development/src`)
- `VISUAL`: program to open cloned repos in

## License

[MIT](https://choosealicense.com/licenses/mit/) © Ben Truyman
