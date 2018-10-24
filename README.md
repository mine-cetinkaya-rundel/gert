# gert

> Simple Git Client for R

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![Build Status](https://travis-ci.org/jeroen/gert.svg?branch=master)](https://travis-ci.org/jeroen/gert)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/jeroen/gert?branch=master)](https://ci.appveyor.com/project/jeroen/gert)
[![CRAN_Status_Badge](http://www.r-pkg.org/badges/version/gert)](https://cran.r-project.org/package=av)

## Installation

To install the development version:

``` r
remotes::install_github("jeroen/gert")
```

On Linux you need somewhat recent version of libgit2:

 - Ubuntu (18.04): [libgit2-dev](https://packages.ubuntu.com/bionic/libgit2-dev)
 - Debian: [libgit2-dev](https://packages.debian.org/buster/libgit2-dev)
 - Fedora: [libgit2-devel](https://apps.fedoraproject.org/packages/libgit2-devel)
 
On Ubuntu 18.04 and up, the stock version of libgit2 is fine. If you are running ubuntu __Xenial__ or __Trusty__ you need libgit2 backports from [my ppa](https://launchpad.net/~opencpu/+archive/ubuntu/libgit2):

```sh
sudo add-apt-repository ppa:opencpu/libgit2
sudo apt-get update
sudo apt-get install libgit2-dev
```
 
It is still possible to install the package with older versions of libgit2 (e.g. on CentOS) however these do not support authentication over ssh/https remotes. Offline functionality should work fine.

## Example

This is a basic example:

``` r
library(gert)
path <- file.path(tempdir(), "ggplot2")
repo <- git_clone("https://github.com/hadley/ggplot2", path)
print(repo)
```
