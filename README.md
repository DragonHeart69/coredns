[![CircleCI](https://circleci.com/gh/giantswarm/coredns/tree/master.svg?style=svg)](https://circleci.com/gh/giantswarm/coredns/tree/master)
[![Docker Repository on Quay](https://quay.io/repository/giantswarm/coredns/status "Docker Repository on Quay")](https://quay.io/repository/giantswarm/coredns)

# Build automation for CoreDNS with Unbound plugin

This repository is used to have reproducible builds of Docker images based on

https://github.com/coredns/coredns

## Usage

To build a Docker image for a new release:

1. Create a branch.
2. Modify the `UPSTREAM_TAG` variable in the `.circleci/config.yml` file. Set it to the release tag of the [upstream repo](https://github.com/coredns/coredns/releases) which should be used. Push to your branch.
3. Create a pull request for your branch.
4. Check the `build` job in CI. As a result, there should be an image tagged with the commit SHA in the registry.
5. Merge the PR after reviews.
6. Tag a release. As a result, there should be a Docker image with the release tag in the registry.
