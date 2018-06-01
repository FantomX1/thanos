# Contributing

First of all, thank you for helping us, improve the Thanos!

When contributing not obvious change to Thanos repository, please first
discuss the change you wish to make via issue or slack, or any other
method with the owners of this repository before making a change.

Please note we have a code of conduct, please follow it in all your interactions with the project.

## Pull Request Process

1. Follow [this](docs/getting_started.md) to prepare thanos. Be familiar with Makefile commands, since they can be useful.
Check Makefile itself for commands like `format`, `build`, `proto` and `test`.
2. Keep PRs as small as possible. Chain them if needed (base PR on other PRs).
3. If you don't have live object store ready add these envvars to skip tests for these:
- THANOS_SKIP_GCS_TESTS to skip GCS tests.
- THANOS_SKIP_S3_AWS_TESTS to skip AWS tests.

If you skip both of these, the store specific tests will be run against memory object storage only.
CI runs GCS and inmem tests only for now. Not having these variables will produce auth errors against GCS or AWS tests.

4. If your change affects users (adds or removes feature) consider adding the item to [CHANGELOG](CHANGELOG.md)
5. You may merge the Pull Request in once you have the sign-off of at least one developers with write access, or if you
   do not have permission to do that, you may request the second reviewer to merge it for you.
6. If you feel like your PR waits too long for a review, feel free to ping `#thanos-dev` channel on our slack for review!

## Code of Conduct

Is available [here](CODE_OF_CONDUCT.md)