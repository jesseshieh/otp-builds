# Erlang OTP For Heroku ![Build Erlang OTP For Heroku](https://github.com/heroku-elixir/otp-builds/workflows/Build%20Erlang%20OTP%20For%20Heroku/badge.svg)

The [Heroku Elixir Buildpack](http://github.com/heroku-elixir/buildpack) uses
pre-compiled builds of Erlang OTP for fast deployments. The binaries it uses are
built and stored in this repository. Erlang is compiled in a GitHub action that
uses the official Heroku Docker images to ensure maximum compatability. After a
given version of Erlang is compiled, it is saved as a GitHub release asset.

## Adding New Versions of Erlang

Just add the new version to the
[`.github/workflows/build-and-release.yml`](.github/workflows/build-and-release.yml)
file. Don't worry about adding an old release, or multiple versions, missing builds
are automatically backfilled.

## Adding New Heroku stacks

1. Create a `heroku-xx.Dockerfile` in the `stacks` directory.
2. Add the new version to the
   [`.github/workflows/build-and-release.yml`](.github/workflows/build-and-release.yml)
   file.

## Standing on The Shoulders of Giants

A special thanks to everyone who worked on the
[original version](https://github.com/HashNuke/heroku-buildpack-elixir-otp-builds)
of this build system. This version was built in ~5 hours, and that wouldn't have been
possible without using the original as a reference point.

## License

This project is licensed under the Apache 2.0 license,
see the full text [here](LICENSE).

© [Kaz Walker](https://github.com/KazW) 2020
