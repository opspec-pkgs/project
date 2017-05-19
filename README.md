# Naming

## Segments
`ORGANIZATION`: organization operation is associated w/  
`PRODUCT`: product operation is associated w/  
`OPERATION`: what the pkg does  

## Rules

### Ensure each segment matches regex `[_a-z0-9]+`
keeps names URL safe & allows easily splitting apart segments

### Only include `ORGANIZATION` if `PRODUCT` isn't independently ubiquitous
keeps length as short as possible while remaining ubiquitous

### Separate segments w/ a `.`

### Order segments as `ORGANIZATION`, `PRODUCT`, and `OPERATION`

## Examples

Good:

`azure.fn.deploy`  
`git.clean`  

Bad:

`AWS.s3.sync` # AWS doesn't match segment regex (uppercase not allowed)  

