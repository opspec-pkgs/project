## Create a package

### step 1

```shell
opctl run github.com/opspec-pkgs/_.pkg.create#1.0.2
```

this will

- create a new repo at https://github.com/opspec-pkgs/YOUR_PKG_NAME
- grant
  [opspec-pkgs/maintainers team](https://github.com/orgs/opspec-pkgs/teams/maintainers/members)
  admin permission
- enable travis-ci

### step 2

```shell
git clone https://github.com/opspec-pkgs/YOUR_PKG_NAME
```

### step 3

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

make sure to set version to 1.0.0 in the `op.yml` & `REAME.md` & update the `CHANGELOG.md`

### step 4

once implementation is complete, create a PR

### step 5

upon acceptance of the PR, create a release via:

```shell
opctl run release
```

