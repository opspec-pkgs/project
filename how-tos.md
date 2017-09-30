## Create a package

### step 1

```shell
opctl run github.com/opspec-pkgs/_.pkg.create#1.0.0
```

this will

- create a new repo at https://github.com/opspec-pkgs/YOUR_PKG_NAME
- grant
  [opspec-pkgs/maintainers team](https://github.com/orgs/opspec-pkgs/teams/maintainers/members)
  admin permission
- enable travis-ci (finicky.. might need to manually enable until
  [retry added](https://github.com/opspec-pkgs/travis-ci.enable/issues/1))

### step 3

```shell
git clone https://github.com/opspec-pkgs/YOUR_PKG_NAME
```

### step 4

implement your package !

it's recommended to use the most similar existing pkg as a template
rather than starting from scratch via:

```shell
opctl pkg install --path . PKG_URL
```

from there you can find/replace/customize as needed

you can test your pkg via:

```shell
opctl run ../
```

make sure to set version to 1.0.0 in the `op.yml` & `REAME.md`

### step 5

once implementation is complete, create a PR

### step 6

upon acceptance of the PR, create a release via:

```shell
opctl run release
```

