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

# images

## use an "official" image when possible

## if no "official" image, [maintain an image](#maintaining-an-image) for your pkg

# maintaining an image

if maintaining an image for your package is required, this section applies

## use pkg name as image name & pkg version as image tag

## publish the image to [https://hub.docker.com/u/opspecpkgs/](https://hub.docker.com/u/opspecpkgs/)
