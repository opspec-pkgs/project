## Create an op

### step 1

```shell
opctl run github.com/opspec-pkgs/_.op.create#3.3.1
```

### step 2

implement your op !

you can run your op via:

```shell
opctl run ../
```

if your op requires a custom container image, you can provision it via:

```shell
opctl run provision-image
```

[include an icon in your op](https://opctl.io/docs/reference/op-definition-format/icon.svg/) to give it swag. Icons MUST be square dimensions, have transparent background, and be SVG. 
> tip: you can easily convert from raster formats to svg via [vectorizer.io](https://www.vectorizer.io/)

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

