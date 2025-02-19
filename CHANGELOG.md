## [6.0.1](https://github.com/pleo-oss/pleo-spa-cicd/compare/v6.0.0...v6.0.1) (2022-08-18)


### Bug Fixes

* Fix version of actions in the workflow ([#20](https://github.com/pleo-oss/pleo-spa-cicd/issues/20)) ([87c7fd6](https://github.com/pleo-oss/pleo-spa-cicd/commit/87c7fd613300518e540f166d87ed1b653acfd8fc))

# [6.0.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v5.1.0...v6.0.0) (2022-08-18)


### Features

* Make "Post Preview URLs" action more generic ([#19](https://github.com/pleo-oss/pleo-spa-cicd/issues/19)) ([f5fa08f](https://github.com/pleo-oss/pleo-spa-cicd/commit/f5fa08f731b6b84eea3628ee7328d1a1ad4a54f6))


### BREAKING CHANGES

* The post preview url actions now takes a JSON definition of links to post

# [5.1.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v5.0.0...v5.1.0) (2022-07-27)


### Features

* Add translation-cursor-deploy ([#13](https://github.com/pleo-oss/pleo-spa-cicd/issues/13)) ([c0621e5](https://github.com/pleo-oss/pleo-spa-cicd/commit/c0621e5226e95bf146cf76773a2ee9a4854b6047))

# [5.0.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v4.0.0...v5.0.0) (2022-07-27)


### Features

* Get rid of S3 Cache Action (moved to pleo-oss/s3-cache-action) ([#17](https://github.com/pleo-oss/pleo-spa-cicd/issues/17)) ([97c4836](https://github.com/pleo-oss/pleo-spa-cicd/commit/97c48367a7daff67888db74252828aa1482688a1))


### BREAKING CHANGES

* The S3 cache action is no longer available in this repository. Use the standalone
version available at pleo-oss/s3-cache-action

# [4.0.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v3.1.0...v4.0.0) (2022-07-05)


### Features

* Switch from passing build_script to passing build_cmd in the build workflow ([#16](https://github.com/pleo-oss/pleo-spa-cicd/issues/16)) ([4739578](https://github.com/pleo-oss/pleo-spa-cicd/commit/473957859311558fb8c1649c9cd53872d2940b58))


### BREAKING CHANGES

* The reusable build workflow now requires to pass a build_cmd input
which is the entire command ran to build the deployable app bundle. This replaces the
previous build_script input which assumed using a script defined in package.json

* docs: Slight clarification in docs

# [3.1.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v3.0.0...v3.1.0) (2022-07-01)


### Features

* Invoke injection script with env variables for bundle dir, env and tree hash ([#15](https://github.com/pleo-oss/pleo-spa-cicd/issues/15)) ([f88df4b](https://github.com/pleo-oss/pleo-spa-cicd/commit/f88df4b4be8002d8ea423dfd16bea1365866ac11))

# [3.0.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v2.1.0...v3.0.0) (2022-06-29)


### Features

* Inversion of control for how injecting config works in deploy workflow ([#14](https://github.com/pleo-oss/pleo-spa-cicd/issues/14)) ([fe4edba](https://github.com/pleo-oss/pleo-spa-cicd/commit/fe4edbad406ac3920f5e26a31b7bd56186dd1625))


### BREAKING CHANGES

* Instead of passing a boolean input called "apply_config" that
would cause the deploy workflow to run a predefined script in package.json, we
now allow the workflow consumer to pass the entire command, including the
paramaters in order and fashion that fits the usecase best.
This allows to pass additional arguments to those scripts, not related to
cursor deployment, without the deploy workflow needing to support them explicitly.

* docs: Fix wording in readme

* feat: Adds `bundle_dir` input to the deploy workfow

`bundle_dir` allows to specify where the directory where the bundle should be unpacked.
This is especially relevant for the script that injects the configuration.

# [2.1.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v2.0.0...v2.1.0) (2022-06-03)


### Features

* Upload deployed artifact for debugging ([#11](https://github.com/pleo-oss/pleo-spa-cicd/issues/11)) ([950f359](https://github.com/pleo-oss/pleo-spa-cicd/commit/950f3598e0b59d82994d14db2fd6c8ae2cecfa19))

# [2.0.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v1.3.1...v2.0.0) (2022-05-23)


### Features

* Use the new GitHub reusable workflow secret inherit feature ([#10](https://github.com/pleo-oss/pleo-spa-cicd/issues/10)) ([e644e4a](https://github.com/pleo-oss/pleo-spa-cicd/commit/e644e4ada1b96ed862cdc1418b66079d3f4610a2))


### BREAKING CHANGES

* The reusable workflow need to be used with secrets: inherit option

## [1.3.1](https://github.com/pleo-oss/pleo-spa-cicd/compare/v1.3.0...v1.3.1) (2022-03-27)


### Bug Fixes

* Preserve PR indentation ([#6](https://github.com/pleo-oss/pleo-spa-cicd/issues/6)) ([1e4ab12](https://github.com/pleo-oss/pleo-spa-cicd/commit/1e4ab1205644dbb18bdc789a6fe188f66c6cc61d))

# [1.3.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v1.2.0...v1.3.0) (2022-03-09)


### Features

* Remove yarn install from the deploy action ([#5](https://github.com/pleo-oss/pleo-spa-cicd/issues/5)) ([45ab255](https://github.com/pleo-oss/pleo-spa-cicd/commit/45ab2554813b7a9ba24006756c87e63ac90b94b3))

# [1.2.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v1.1.1...v1.2.0) (2022-02-21)


### Features

* Add an option to pass app name when deploying ([#4](https://github.com/pleo-oss/pleo-spa-cicd/issues/4)) ([e3042ba](https://github.com/pleo-oss/pleo-spa-cicd/commit/e3042ba8a2886550fb67601ee09da959e9f5d779))

## [1.1.1](https://github.com/pleo-oss/pleo-spa-cicd/compare/v1.1.0...v1.1.1) (2022-02-21)


### Bug Fixes

* Fix description posting ([#3](https://github.com/pleo-oss/pleo-spa-cicd/issues/3)) ([60d4335](https://github.com/pleo-oss/pleo-spa-cicd/commit/60d4335388fdbbca418a1f0bca15d93049736cf3))

# [1.1.0](https://github.com/pleo-oss/pleo-spa-cicd/compare/v1.0.0...v1.1.0) (2022-02-17)


### Features

* Improve preview urls ([#2](https://github.com/pleo-oss/pleo-spa-cicd/issues/2)) ([9dcb64e](https://github.com/pleo-oss/pleo-spa-cicd/commit/9dcb64e9fa7cc7eadf4b146fd4ad3a6ed2a84c8b))

# 1.0.0 (2022-02-14)


### Features

* Initial release ([d295c72](https://github.com/pleo-oss/pleo-spa-cicd/commit/d295c72c2d92004d548e99a421ea1ff3215683fa))
