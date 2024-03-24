
# kts update

* made to run on my laptop,

```
macOS 13.5.2

$ cabal --version
cabal-install version 3.10.2.1
compiled using version 3.10.2.1 of the Cabal library

$ ghc --version
The Glorious Glasgow Haskell Compilation System, version 9.4.8
```

# Detexify Backend Server implemented in Haskell

## Requirements

- Haskell Platform
- `$ cabal install --only-dependencies`

## Compile

    $ cabal build

## Run

    $ dist/build/detexify-hs-backend/detexify-hs-backend

will run the webserver on port 3000. It will load training data from snapshot.json.

## Docker

    docker build -t kirel/detexify-hs-backend .
    docker push kirel/detexify-hs-backend

## Deploy

    ansible-playbook ansible/deploy.yml -i ansible/inventory

## License

Copyright (c) 2009 Daniel Kirsch, released under the MIT license, see MIT-LICENSE
