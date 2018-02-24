## Create a package

### step 1

```shell
opctl run github.com/opspec-pkgs/_.pkg.create#2.0.0
```

### step 2

implement your package !

you can test your pkg via:

```shell
opctl run ../
```

if your pkg requires a custom base image, you can provision it via:

```shell
opctl run provision-image
```

### step 3

once implementation is complete, run a build via:
```shell
opctl run build
```

if all's well submit a PR

### step 4

upon acceptance of the PR, create a release via:

```shell
opctl run release
```

