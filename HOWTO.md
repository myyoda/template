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

E.g.

    datalad update --merge inputs/ds000001/
    datalad save -d . -m "fetched more subjects" inputs/ds000001


## Create a new sub-dataset to contain results of preprocessing


    datalad create -d . outputs/NAME

e.g.

    datalad create -d . outputs/fmriprep

## Run a command in a "reproducible" way

Use

    datalad run CMD [OPTIONS]

which will create a new commit recording all the changes done by the CMD,
so it could later be reran using [datalad rerun] command. E.g.

    datalad run -m "preprocess sample subject" \
      envs/fmriprep inputs/ds000001 outputs/fmriprep/sub-01


## Reproduce a full sequence of commands (and commits) ever ran before

    datalad rerun --onto= --since= -b rerun-1

which will place reran results into rerun-1 branch for comparison etc


## Publish entire hierarchy to HTTP server via SSH

TODO

## Publish entire hierarchy to github


[datalad rerun]: http://docs.datalad.org/en/latest/generated/man/datalad-rerun.html