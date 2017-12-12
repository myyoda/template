# YODA HOWTOs

This document describes most commonly used commands and workflows to
operate on the hierarchy

## Find template text still needed to be changed

   git grep YODATODO

## Add an additional existing input dataset

    datalad add -d . -s URL inputs/NAME

e.g.,

    datalad add -d . -s ///openfmri/ds000001 inputs/ds000001

## Update input dataset(s) to a new version

## Create a new sub-dataset to contain results of preprocessing


   datalad create -d . outputs/NAME

e.g.

   datalad create -d . outputs/fmriprep

## Publish entire hierarchy to HTTP server via SSH

TODO

## Publish entire hierarchy to github

