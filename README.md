# ckan-docker-build

This repository will hold all Dockerfiles, configuration files, 
and other (public) information required to build an image for
the Data Refuge project's CKAN instance. 

Our first goal for this repository is to match the configuration 
of the running server as closely as possible. We want the resulting 
image to serve, initially, as a drop-in replacement for the current
running server -- if possible.  We will be setting up cloned copies
of the existing Postgres and SOLR servers (as EC2 instances) for
testing shortly. 

Our second goal will be to adopt a "correct" Docker configuration
style, which will likely mean imitating the style of the docker 
folder in the [main CKAN repo](https://github.com/datarefuge/ckan/tree/master/contrib/docker).
However, for maximum flexibility, we are locating our build
repo separately, even if it turns out that we can basically
clone the standard CKAN docker configuration. At the very least,
we intend to use ubuntu rather than debian for our base image.

Once we have an image that works as a drop-in replacement, and
Dockerfiles that adhere to good practice guidelines, we can
flesh out a development build configuration, so that developers 
can run local docker containers rather than connecting
to our Postgres and SOLR test clones.

This document is a draft proposal, to be updated by people who
know what is actually possible or desirable.
