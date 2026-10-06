# nb-wrangler-images

This repository maintains copies of the [specs][nbi-specs] and [auxilliary files][nbi-assets] used to generate notebook images for STScI's science platforms.  It also defines the GitHub pipelines run on the [specs][nbi-specs] to build images and push them to [GHCR][GHCR]. As such,  this repo can be considered to manage notebook environment definitions and images.

[nb-wrangler][nb-wrangler] is a Python project used to curate notebook environments.  It provides a pip installable tool `nbw` used here in pipelines.  More information on the tool can be found at the [nb-wrangler] GitHub repo.  Information about the [format for specs][wrangler-specs] archived and built here and used by `nbw` is found in the nb-wrangler documentation.  Likewise,  information about using the `nbw` tool directly is found in [nb-wrangler][nb-wrangler] documentation

Images come in two kinds, nominally built in pairs:

1. Large notebook binary images with names starting with `nbw_`.  These run on the platform.

2. Very lightweight images with names starting with `nbs_` containing only the spec. These provide a quick reference point for the packages built into the corresponding `nbw_` notebook image. `nbw` has commands to list and fetch and unpack these, but they are dependent on access to Docker.

The as-built spec is also included in each image at the standard location  `/opt/environments/nbw-wrangler-spec.yaml`.

[nb-wrangler]: https://github.com/spacetelescope/nb-wrangler
[nbi-specs]: https://github.com/spacetelescope/nb-wrangler-images/tree/main/specs
[nbi-assets]: https://github.com/spacetelescope/nb-wrangler-images/tree/main/assets
[wrangler-specs]: https://github.com/spacetelescope/nb-wrangler/blob/main/docs/spec-format.md
[GHCR]: https://github.com/spacetelescope/nb-wrangler/pkgs/container/nb-wrangler-images