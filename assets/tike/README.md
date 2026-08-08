# TIKE Assets

If there are small files (e.g. source code) which are unique to TIKE you can
place them in this directory and then download and install them into an image
by defining the "assets" section of the spec that lets you specify the URL the
file is coming from (or this one by default), the source path in this repo
relative to the top-level (assets/tike/...), and the destination path in the
image.  As things are today the wrangler generates an "install-assets.sh"
script which is executed inside the Dockerfile to download and locate the
asset files at the specified destination.
