# YODATODO  The title of the study

YODATODO Description for the study

## Status

TODO stubs for CI banners

## Files organization

- [ci/](./ci) - scripts and configurations for CI platforms (Travis, Circle-CI, etc)
- [code/](./code) - analysis scripts
- [docs/](./docs) - documentation, notes, papers (pre-prints), etc
- [envs/](./envs) - images and/or specification of complete environments (singularity, docker, etc)
- [inputs/](./inputs) - dataset(s) which served as inputs for the study
- [outputs/](./outputs) - results of analysis using `code/`, `envs/`, and `inputs/`
- [tests/](./tests) - various tests to verify correct operation of code etc
- [CHANGELOG.md](./CHANGELOG.md) - summary of changes/progress
- [HOWTO.md](./HOWTO.md) - various details on using/manipulating provided materials
- [README.md](./README.md) - high level overview of the study

YODATODO adjust aforementioned list and description below for your particular case/study.
Any of the aforementioned directories could be, or could contain, other
git/git-annex repositories as submodules. In DataLad they are called
[subdatasets](http://docs.datalad.org/en/latest/glossary.html#term-subdataset).
Organizing them in such modular fashion allows for reuse while maintaining
unambigous version association.  Examples:

- a `inputs/bids-dataset` could be used for multiple studies
- `envs/singularity` could point to a collection of singularity images
  with environments used across multiple studies
- `outputs/bids-dataset-preprocessed` could be used `inputs/...` in
  some other study

## Similar/Related projects

- [Shablona](https://github.com/uwescience/shablona) -
  a template project for small scientific Python projects. Could be a good
  starting point for your reusable `code/` or a part within it.
