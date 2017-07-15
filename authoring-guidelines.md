# package naming

## prefix name w/ a hierarchical (broad => specific) `.` separated namespace
avoids name collisions

### examples: 

#### good
`ORGANIZATION.PRODUCT.OPERATION`

## ensure names match regex `[_a-z0-9](.[_a-z0-9])*`
keeps names URL safe & allows easily splitting apart segments

### examples:

#### bad
`AWS.s3.sync` # AWS doesn't match segment regex (uppercase not allowed)  

## only include `ORGANIZATION` if `PRODUCT` isn't independently ubiquitous
keeps length as short as possible while remaining ubiquitous

### examples

#### good
`azure.fn.deploy`

# container images

## use an "official" image when possible
removes need for package maintenance, unless necessary

## if no "official" image, maintain an image for your pkg
maintains a trustworthy dependency chain

## if maintaining an image, use pkg name as name
ensures purpose of image is clear

## if maintaining an image, use pkg version as tag
ensures stability of image

## if maintaining an image, push to [https://hub.docker.com/u/opspecpkgs/](https://hub.docker.com/u/opspecpkgs/)
keeps all packages in a single namespace in docker w/ shared access by opspec-pkgs contributors

