# 1. Package naming

## 1.1 prefix name w/ a hierarchical (broad => specific) `.` separated namespace

avoids name collisions

### examples:

#### good

`ORGANIZATION.PRODUCT.OPERATION`

## `_` root namespace reserved for internal use by `opspec-pkgs` project

### examples:

#### good

[_.pkg.create](https://github.com/opspec-pkgs/_.pkg.create)

## ensure names match regex `[_a-z0-9](.[_a-z0-9])*`

keeps names URL safe & allows easily splitting apart segments

### examples:

#### bad

`AWS.s3.sync` # AWS doesn't match segment regex (uppercase not allowed)

## 1.2 only include `ORGANIZATION` if `PRODUCT` isn't independently ubiquitous

keeps length as short as possible while remaining ubiquitous

### examples

#### good

`azure.fn.deploy`

#### bad

`microsoft.azure.fn.deploy` # microsoft prefix unnecessary; azure is
already ubiquitous

## 1.3 use terminology of ecosystem pkg interacts w/; don't invent or abbreviate

keeps ecosystem as source of truth; anyone familiar w/ ecosystem is also
familiar w/ pkgs


# 2. Container images

## 2.1 use an "official" image when possible

removes need for package maintenance, unless necessary

## 2.2 if no "official" image, maintain an image for your pkg

maintains a trustworthy dependency chain

## 2.3 if maintaining an image, use pkg name as name

ensures purpose of image is clear

## 2.4 if maintaining an image, use pkg version as tag

ensures stability of image

## 2.5 if maintaining an image, push to [https://hub.docker.com/u/opspecpkgs/](https://hub.docker.com/u/opspecpkgs/)

keeps all packages in a single namespace in docker w/ shared access by
opspec-pkgs contributors

# 3. Releases

## 3.1 maintain a changelog adhering to [keepachangelog.com v1.0.0](http://keepachangelog.com/en/1.0.0/)

exposes historical changes to the pkg via a popular industry standard
format
