[![Build Status][actions-img]][actions]
[![Hackage][hackage-img]][hackage]
[![GPL-3 licensed][license-img]][license]

# haskell-language-docker

Dockerfile parser, pretty-printer and embedded DSL

Provides de ability to parse docker files, a pretty-printer and EDSL for
writting Dockerfiles in Haskell.

- [Parsing files](#parsing-files)
- [Parsing strings](#parsing-strings)
- [Pretty-printing files](#pretty-printing-files)

## Parsing files

```haskell
import Language.Docker
main = do
    ef <- parseFile "./Dockerfile"
    print ef
```

## Parsing strings

```haskell
import Language.Docker
main = do
    c <- readFile "./Dockerfile"
    print (parseString c)
```

## Create Dockerfiles

Use the [dockerfile-creator package](https://github.com/hadolint/dockerfile-creator)

[hackage-img]: https://img.shields.io/hackage/v/language-docker.svg
[hackage]: https://hackage.haskell.org/package/language-docker
[actions-img]: https://github.com/hadolint/language-docker/actions/workflows/haskell.yml/badge.svg
[actions]: https://github.com/hadolint/language-docker/actions/workflows/haskell.yml
[license-img]: https://img.shields.io/badge/license-GPL--3-blue.svg
[license]: https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3)
