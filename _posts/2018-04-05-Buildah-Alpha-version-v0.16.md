---
title: Buildah Alpha version 0.16 Release Announcement
layout: default
author: tsweeney
categories: [releases]
tags: community, open source, buildah
---
![buildah logo](https://buildah.io/images/buildah.png)

# Buildah Alpha version 0.16 Release Announcement

We're pleased to announce the release of Buildah Alpha version 0.16 which is now available from GitHub for any Linux distro.  We will be shipping this release on Fedora, CentOS and Ubuntu in the near future.

The Buildah project has continued to grow over the past several weeks, welcoming several new contributors to the mix, launching new functionality and creating a number of improvements and bug fixes.  

<!--readmore-->

## The major highlights for this release are:

 * Add support for the SHELL command in Dockerfiles.
 * Change the time displayed by the image command to the locale time.
 * Allow the --cmd parameter for the `buildah config` command to have commands as values.  I.e. `buildah config --cmd “--help” {containerID}`.
 * Documentations added for the mounts.conf file. The mounts config allows you to mount content from the host into the container to be used during the build procedure, but does not get committed to the image.
 * Fixed  a number of man pages to format correctly.
 * The `buildah from` command now supports pulling images using the following three transports: docker-archive, oci-archive, and dir, as well as normal container registries and the docker daemon.
 * If the user overrides the storage driver, the options will not be used from the default storage.conf file.
 * Show the Config and Manifest as a JSON string in `buildah inspect` even when the  --format parameter is not set.
 * Adds feature to pull compressed docker-archive files.
 * Vendor in latest containers/image
   * docker-archive generates docker legacy compatible images.
   * Ensure the layer IDs in legacy docker/tarfile metadata are unique.
   * docker-archive: repeated layers are symlinked in the tar file.
   * sysregistries: remove all trailing slashes.
   * Improve docker/* error messages.
   * Fix failure to make auth directory.
   * Create a new slice in Schema1.UpdateLayerInfos.
   * Drop unused storageImageDestination.{image,systemContext}.
   * Load a *storage.Image only once in storageImageSource.
   * Support gzip for docker-archive files.
   * Remove .tar extension from blob and config file names.
   * ostree, src: support copy of compressed layers.
   * ostree: re-pull layer if it misses uncompressed_digest|uncompressed_size.
   * image: fix docker schema v1 -> OCI conversion.
   * Add /etc/containers/certs.d as default certs directory.
 * Plus several small bug fixes.

## Try it Out.

If you haven’t yet,  install Buildah from the Fedora repo or GitHub and give it a spin.  We’re betting you'll find it’s an easy and quick way to build containers in your environment without a daemon being involved!

For those of you who contributed to this release, thank you very much for your contributions!  If you haven't joined our community yet, don't wait any longer!  Come join us in GitHub, where Open Source communities live.

## Buildah == Simplicity
