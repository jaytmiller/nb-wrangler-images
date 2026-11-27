# Wrangling from Start to Finish

This document gives a walk through of nb-wrangler based image development
starting with creation of the image spec running all the way through
optional image deployment to PROD.

## Phase 1: Local Spec Development

The primary work of phase 1 is defining the wrangler spec what characterizes
the environment, notebooks, and packages that will be supported by an image.
Basic spec development is generally unavoidable but followon steps

### Creating a Wrangler Spec

repo: nb-wrangler-images

Copy an existing spec or run `nbw --init <filename>` to baseline your spec.
Update the header fields, repos, selected notebooks, and package specifications
as needed.

### Curating the Environment

### Curating the Data

### Injecting Requirements into Image Source

### Building an Image locally (optional)

### Testing an Image locally (optional)

## Phase 2: Image Building and Delivery

### Submitting the Spec

### Using Actions to Build Images

### Delivering the image to TEST

### Testing in TEST

### Transferring the image to ECR

### Updating the SDLC Common Image Profile

### Retagging the Image for PROD
