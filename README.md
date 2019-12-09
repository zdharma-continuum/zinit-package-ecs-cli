# aws/amazon-ecs-cli as a Zsh package

##### NPM link: [https://www.npmjs.com/package/zsh-doctoc](https://www.npmjs.com/package/zsh-doctoc)

##### Homepage link: [aws/amazon-ecs-cli](https://github.com/aws/amazon-ecs-cli)

| **Package source:** | Tarball | Git | Node | Gem |
|:-------------------:|:-------:|:---:|:----:|:---:|
| **Status:**         | + <br> (default) |  -  |   –  |  –  |

[Zplugin](https://github.com/zdharma/zplugin) can use the NPM package registry
to automatically:

- get the plugin's Git repository OR release-package URL,
- get the list of the recommended ices for the plugin,
    - there can be multiple lists of ices,
    - the ice lists are stored in *profiles*; there's at least one profile, *default*,
    - the ices can be selectively overriden.

Example invocations that'll install
[aws/amazon-ecs-cli](https://github.com/aws/amazon-ecs-cli) by using the
[bin-gem-node](https://github.com/zplugin/z-a-bin-gem-node) annex:

```zsh
# Download the Node package of amazon-ecs-cli
zplugin pack for ecs-cli
```

## bin-gem-node Profile

Provides the CLI command `ecs-cli`.

The Zplugin command executed will be equivalent to:

```zsh
zplugin as=null mv="*latest -> ecs-cli" atclone="chmod +x *"
    atpull="%atclone" sbin="ecs-cli" is-snippet for \
        https://amazon-ecs-cli.s3.amazonaws.com/ecs-cli-${(M)OSTYPE#(linux|darwin)}-amd64-latest
```

<!-- vim:set ft=markdown tw=80 fo+=an1 autoindent: -->
