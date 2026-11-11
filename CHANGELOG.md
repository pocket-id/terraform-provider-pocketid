## v2.5.0

### Features

- Client logo URLs ([\#121](https://github.com/pocket-id/terraform-provider-pocketid/pull/121) by @michaelheyman)

### Bug Fixes

- run pre-release cleanup after the release, not alongside it ([\#120](https://github.com/pocket-id/terraform-provider-pocketid/pull/120) by @Trozz)
- wait for pocket-id health before seeding the test database ([\#123](https://github.com/pocket-id/terraform-provider-pocketid/pull/123) by @Trozz)
- support the auto-created client secret in upcoming Pocket ID ([\#122](https://github.com/pocket-id/terraform-provider-pocketid/pull/122) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v2.4.2...v2.5.0

## v2.4.2

### Bug Fixes

- revoke the superseded secret when rotating a client secret ([\#117](https://github.com/pocket-id/terraform-provider-pocketid/pull/117) by @Trozz)
- wait for the sqlite lock when seeding the test database ([\#118](https://github.com/pocket-id/terraform-provider-pocketid/pull/118) by @Trozz)
- pin the release changelog base to the last stable tag ([\#119](https://github.com/pocket-id/terraform-provider-pocketid/pull/119) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v2.4.1...v2.4.2

## v2.4.1

### Bug Fixes

- preserve unexposed client settings when updating a client ([\#116](https://github.com/pocket-id/terraform-provider-pocketid/pull/116) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v2.4.0...v2.4.1

## v2.4.0

### Features

- add support for declarative user IDs and client secrets ([\#90](https://github.com/pocket-id/terraform-provider-pocketid/pull/90) by @schnz)

### Bug Fixes

- model allowed_user_groups as a set ([\#92](https://github.com/pocket-id/terraform-provider-pocketid/pull/92) by @michaelheyman)
- download pocket-id release assets with their current names ([\#102](https://github.com/pocket-id/terraform-provider-pocketid/pull/102) by @Trozz)
- preserve server-managed application configuration fields ([\#103](https://github.com/pocket-id/terraform-provider-pocketid/pull/103) by @Trozz)
- support OIDC client secret creation on Pocket ID 2.14+ ([\#97](https://github.com/pocket-id/terraform-provider-pocketid/pull/97) by @mathieu-lemay)
- stop test cleanup and security scans from failing ([\#105](https://github.com/pocket-id/terraform-provider-pocketid/pull/105) by @Trozz)
- stop excluding docs from the release source archive ([\#115](https://github.com/pocket-id/terraform-provider-pocketid/pull/115) by @Trozz)

### Other

- bump golang.org/x/net from 0.52.0 to 0.55.0 ([\#84](https://github.com/pocket-id/terraform-provider-pocketid/pull/84) by @dependabot\[bot\])
- bump the actions group across 1 directory with 13 updates ([\#85](https://github.com/pocket-id/terraform-provider-pocketid/pull/85) by @dependabot\[bot\])
- accept 409 for a duplicate user group name ([\#104](https://github.com/pocket-id/terraform-provider-pocketid/pull/104) by @Trozz)
- bump golang.org/x/net from 0.55.0 to 0.57.0 ([\#87](https://github.com/pocket-id/terraform-provider-pocketid/pull/87) by @dependabot\[bot\])
- bump the go-minor group across 1 directory with 2 updates ([\#98](https://github.com/pocket-id/terraform-provider-pocketid/pull/98) by @dependabot\[bot\])
- bump the actions group across 1 directory with 11 updates ([\#101](https://github.com/pocket-id/terraform-provider-pocketid/pull/101) by @dependabot\[bot\])
- bump google.golang.org/grpc from 1.79.3 to 1.83.2 ([\#100](https://github.com/pocket-id/terraform-provider-pocketid/pull/100) by @dependabot\[bot\])

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v2.3.0...v2.4.0

## v2.3.0

### Features

- add pocketid_ldap_sync trigger resource ([\#79](https://github.com/pocket-id/terraform-provider-pocketid/pull/79) by @Trozz)
- expose ldap_id (and group created_at) ([\#80](https://github.com/pocket-id/terraform-provider-pocketid/pull/80) by @Trozz)

### Other

- trigger pre-release cleanup on tag push, not release event ([\#78](https://github.com/pocket-id/terraform-provider-pocketid/pull/78) by @Trozz)
- ignore dev tags when resolving previous tag ([\#81](https://github.com/pocket-id/terraform-provider-pocketid/pull/81) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v2.2.0...v2.3.0

## v2.2.0

### Features

- add requires_pushed_authorization_requests (PAR) ([\#72](https://github.com/pocket-id/terraform-provider-pocketid/pull/72) by @Trozz)

### Bug Fixes

- handle PAR public-client coercion (test + plan-time validator) ([\#77](https://github.com/pocket-id/terraform-provider-pocketid/pull/77) by @Trozz)

### Other

- disable markdownlint MD060 (breaks Markdown Lint on all PRs) ([\#73](https://github.com/pocket-id/terraform-provider-pocketid/pull/73) by @Trozz)
- clean up dev pre-releases when a stable release is published ([\#74](https://github.com/pocket-id/terraform-provider-pocketid/pull/74) by @Trozz)
- expand Terraform matrix to 1.15.6 and add OpenTofu compatibility tests ([\#75](https://github.com/pocket-id/terraform-provider-pocketid/pull/75) by @Trozz)
- test against pinned, latest, and dev pocket-id versions ([\#76](https://github.com/pocket-id/terraform-provider-pocketid/pull/76) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v2.1.0...v2.2.0

## v2.1.0

### Features

- manage custom claims ([\#71](https://github.com/pocket-id/terraform-provider-pocketid/pull/71) by @Trozz)
- add PAR, federated identities, and email_verified fields ([\#69](https://github.com/pocket-id/terraform-provider-pocketid/pull/69) by @Trozz)
- add SCIM service provider resource ([\#68](https://github.com/pocket-id/terraform-provider-pocketid/pull/68) by @Trozz)
- add application configuration resource and data source ([\#70](https://github.com/pocket-id/terraform-provider-pocketid/pull/70) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v2.0.0...v2.1.0

## v2.0.0

### Features

- v2 API correctness for pocket-id v2 ([\#66](https://github.com/pocket-id/terraform-provider-pocketid/pull/66) by @Trozz)

### Bug Fixes

- pin goreleaser to pushed tag to avoid dev-tag collision ([\#67](https://github.com/pocket-id/terraform-provider-pocketid/pull/67) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v0.1.8...v2.0.0

## v0.1.8

### Features

- add group and groups data sources ([49b1d41](https://github.com/pocket-id/terraform-provider-pocketid/commit/49b1d4174d9b175a75887e9a72bd00e349ef21f5) by @Trozz)
- Optimize CI/CD workflows with conditional job execution and file change detection ([\#10](https://github.com/pocket-id/terraform-provider-pocketid/pull/10) by @Trozz)
- add one-time access token resource for user authentication recovery ([\#11](https://github.com/pocket-id/terraform-provider-pocketid/pull/11) by @Trozz)
- allow presetting client_id for OIDC clients via Terraform resource schema and API client ([\#24](https://github.com/pocket-id/terraform-provider-pocketid/pull/24) by @Trozz)
- add requires reauth and launch url ([\#40](https://github.com/pocket-id/terraform-provider-pocketid/pull/40) by @meerumschlungen)

### Bug Fixes

- update docker-compose commands to docker compose v2 ([5ba8ec2](https://github.com/pocket-id/terraform-provider-pocketid/commit/5ba8ec24f37ed273485924e7639bb685368fb3a6) by @Trozz)
- comprehensive CI/CD improvements and test infrastructure overhaul ([\#2](https://github.com/pocket-id/terraform-provider-pocketid/pull/2) by @Trozz)
- Include DisplayName in User Resource ([\#31](https://github.com/pocket-id/terraform-provider-pocketid/pull/31) by @rtrox)
- allow wildcard and custom-scheme callback URLs; add validator tests ([\#42](https://github.com/pocket-id/terraform-provider-pocketid/pull/42) by @meerumschlungen)
- correct JSON field names for client ID and launchURL ([\#45](https://github.com/pocket-id/terraform-provider-pocketid/pull/45) by @lansidev)

### Documentation

- fix markdown line length and regenerate documentation ([20f03a8](https://github.com/pocket-id/terraform-provider-pocketid/commit/20f03a84e6abe978996d6bc52891234a0cc56f68) by @Trozz)
- Remove Documentation from the CI workflow ([0f6dc90](https://github.com/pocket-id/terraform-provider-pocketid/commit/0f6dc90575cae7ab04a077c4d374f1f349a99ca6) by @Trozz)
- Update documentation and attempt to trigger Terraform Registry refresh ([\#41](https://github.com/pocket-id/terraform-provider-pocketid/pull/41) by @Trozz)

### Other

- add unit tests for group data sources ([4d96919](https://github.com/pocket-id/terraform-provider-pocketid/commit/4d96919d0bfc04d3a8d3078b2d33af48e32df6e5) by @Trozz)
- add unit tests for resource files below 30% coverage ([e477b2d](https://github.com/pocket-id/terraform-provider-pocketid/commit/e477b2df2037484d9bfa56d825added868d4f46d) by @Trozz)
- switch to using examples directory for integration tests ([e9ce34c](https://github.com/pocket-id/terraform-provider-pocketid/commit/e9ce34c6681355aa89fe1cad6358ed53d47f013b) by @Trozz)
- add acceptance test coverage reporting and expand test cases ([a075d62](https://github.com/pocket-id/terraform-provider-pocketid/commit/a075d62f4dc5f7c37ff2752f8eeea22b1257da38) by @Trozz)
- fix formatting and add missing newlines ([726c897](https://github.com/pocket-id/terraform-provider-pocketid/commit/726c8976580a2c729a0a93be774887a6b152b14a) by @Trozz)
- bump the actions group across 1 directory with 7 updates ([\#13](https://github.com/pocket-id/terraform-provider-pocketid/pull/13) by @dependabot\[bot\])
- bump the actions group across 1 directory with 21 updates ([\#56](https://github.com/pocket-id/terraform-provider-pocketid/pull/56) by @dependabot\[bot\])
- bump the actions group across 1 directory with 15 updates ([\#63](https://github.com/pocket-id/terraform-provider-pocketid/pull/63) by @dependabot\[bot\])
- bump github.com/cloudflare/circl from 1.6.1 to 1.6.3 ([\#47](https://github.com/pocket-id/terraform-provider-pocketid/pull/47) by @dependabot\[bot\])
- bump Go to 1.25 for terraform-plugin updates ([\#64](https://github.com/pocket-id/terraform-provider-pocketid/pull/64) by @Trozz)
- bump golangci-lint to v2.12.2 for Go 1.25 ([\#65](https://github.com/pocket-id/terraform-provider-pocketid/pull/65) by @Trozz)
- bump the go-minor group across 1 directory with 6 updates ([\#61](https://github.com/pocket-id/terraform-provider-pocketid/pull/61) by @dependabot\[bot\])

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v0.1.5...v0.1.8

## v0.1.5

### Bug Fixes

- update goreleaser archive format configuration ([0ec0d04](https://github.com/pocket-id/terraform-provider-pocketid/commit/0ec0d0470867876571d9aba205304ce94db57bcf) by @Trozz)
- update trufflehog hook stages to use correct stage names ([8c2da74](https://github.com/pocket-id/terraform-provider-pocketid/commit/8c2da74d7b73a87eda8ee47badb69ebdf929bf47) by @Trozz)
- add ARM version suffix to goreleaser archive names ([e26160e](https://github.com/pocket-id/terraform-provider-pocketid/commit/e26160e06c04cadabd6f7996bb51d9176924e901) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v0.1.4...v0.1.5

## v0.1.4

### Documentation

- update provider documentation and examples ([8b20371](https://github.com/pocket-id/terraform-provider-pocketid/commit/8b20371dfb049151a9917dd31abfe4d8d3d06a73) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v0.1.3...v0.1.4

## v0.1.3

### Features

- add dedicated pre-release cleanup workflow ([532c098](https://github.com/pocket-id/terraform-provider-pocketid/commit/532c0980a43bbdcac234fdd81011cb9ed7884744) by @Trozz)
- only generate pre-releases when Go files change ([eb333d0](https://github.com/pocket-id/terraform-provider-pocketid/commit/eb333d0dd46bb3efc7a4af6bf1e9637afd07cb10) by @Trozz)
- add Dependabot configuration for automated dependency updates ([170baa8](https://github.com/pocket-id/terraform-provider-pocketid/commit/170baa8ab01fa3af4dd611549571be9cc9a11be0) by @Trozz)
- enhance Codecov configuration with components and status checks ([98cc002](https://github.com/pocket-id/terraform-provider-pocketid/commit/98cc002bc59df87e0c236f5764fd302a388b13cd) by @Trozz)

### Bug Fixes

- replace Dependabot reviewers with CODEOWNERS file ([d076bd2](https://github.com/pocket-id/terraform-provider-pocketid/commit/d076bd20ebaea6faf363dc534a22d723a7903041) by @Trozz)

### Other

- bump the actions group with 2 updates ([6c8d0e5](https://github.com/pocket-id/terraform-provider-pocketid/commit/6c8d0e5a0183c393e3adc3840890e8928ffbf929) by @dependabot\[bot\])
- add pre-commit hooks and markdownlint configuration ([f5a4c84](https://github.com/pocket-id/terraform-provider-pocketid/commit/f5a4c847d2d8695b7a2d7ad499965acc8666f007) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v0.1.2...v0.1.3

## v0.1.2

### Features

- add HTTP 429 rate limit handling with retry support ([348cf93](https://github.com/pocket-id/terraform-provider-pocketid/commit/348cf93e2490715a3d912ba1329159fe4848396e) by @Trozz)
- improve test coverage from 17.4% to 39.3% and add rate limiting ([733930c](https://github.com/pocket-id/terraform-provider-pocketid/commit/733930ce0c446e16a818acae1802b3a9253e09d2) by @Trozz)
- add pre-release automation to CI workflow ([8cb8679](https://github.com/pocket-id/terraform-provider-pocketid/commit/8cb8679caad915811293654246054b8874a9602e) by @Trozz)
- implement GitHub build attestations for supply chain security ([b0a0c6f](https://github.com/pocket-id/terraform-provider-pocketid/commit/b0a0c6f7b14a2852aee5a7abae67f729050bb8ee) by @Trozz)
- add version bump workflow for manual semver releases ([7ac422f](https://github.com/pocket-id/terraform-provider-pocketid/commit/7ac422fed4113415c3aa57f7c9866a0962ef2075) by @Trozz)

### Bug Fixes

- resolve golangci-lint issues ([5683ed2](https://github.com/pocket-id/terraform-provider-pocketid/commit/5683ed29a8eb81c220e7bb582bdae59f72be8b3a) by @Trozz)
- update GitHub Actions and fix golangci-lint config for v2 ([656c7ae](https://github.com/pocket-id/terraform-provider-pocketid/commit/656c7ae2b16cf7d4df19bec5b805c1fd4a3bcc5a) by @Trozz)
- update golangci-lint version to v2.2.1 in CI ([77b0b3c](https://github.com/pocket-id/terraform-provider-pocketid/commit/77b0b3cd0dfb4eca2c5ff7cad7b9c50ee1cd38a7) by @Trozz)
- update golangci-lint-action to v8 for golangci-lint v2 support ([898fa2b](https://github.com/pocket-id/terraform-provider-pocketid/commit/898fa2b0d6cb1a5f3ab7af6a302ad7ebf1d66fb1) by @Trozz)
- update .golangci.yml configuration for v2 schema ([9b3147a](https://github.com/pocket-id/terraform-provider-pocketid/commit/9b3147a52086d020818c6ed768fac014eac1e889) by @Trozz)
- resolve all errcheck linting issues ([779c48e](https://github.com/pocket-id/terraform-provider-pocketid/commit/779c48ea55f478b4f05dfbb357a82616c8112aef) by @Trozz)
- correct provider source address and generate documentation ([d9ee7b0](https://github.com/pocket-id/terraform-provider-pocketid/commit/d9ee7b01c0cf4874951783f0ad371bcad7b989f3) by @Trozz)
- specify provider name for tfplugindocs in Makefile and CI ([1cd7132](https://github.com/pocket-id/terraform-provider-pocketid/commit/1cd7132aac8bdf85892bbeb606af73e969a78e43) by @Trozz)
- add proper permissions to CI workflow ([15e306f](https://github.com/pocket-id/terraform-provider-pocketid/commit/15e306f4e29ff94dae538d4159f7cf3fe69c5d77) by @Trozz)
- add nosec comment for legitimate InsecureSkipVerify usage ([57c8776](https://github.com/pocket-id/terraform-provider-pocketid/commit/57c8776897833a496de64fd49357578c6d90f714) by @Trozz)
- add version 2 to goreleaser config for CI compatibility ([14819f9](https://github.com/pocket-id/terraform-provider-pocketid/commit/14819f9858e8ff0c1e4c06ce628240d9aa40189a) by @Trozz)
- remove tag triggers from CI workflow and fix snapshot version template ([b387432](https://github.com/pocket-id/terraform-provider-pocketid/commit/b3874322f61b9f57ad3c3675ca64c6a4ba73bd01) by @Trozz)
- remove unused release job from CI workflow ([afb87ad](https://github.com/pocket-id/terraform-provider-pocketid/commit/afb87add2f55a3be508c934e9a5ecb3faa54cab4) by @Trozz)
- remove GORELEASER_CURRENT_TAG from snapshot build ([19e47d0](https://github.com/pocket-id/terraform-provider-pocketid/commit/19e47d08a35b3ef136340e8f163846e8e241853d) by @Trozz)
- remove redundant build job from CI workflow ([1f659ee](https://github.com/pocket-id/terraform-provider-pocketid/commit/1f659ee3a587da99994f7f3657b9a16cb0aefbf2) by @Trozz)
- remove redundant tag check from CI workflow conditions ([a7d355b](https://github.com/pocket-id/terraform-provider-pocketid/commit/a7d355b2b63b282b7e2bfa2fe452987dd654ca0c) by @Trozz)
- improve version detection to exclude pre-release tags ([47e4d16](https://github.com/pocket-id/terraform-provider-pocketid/commit/47e4d168a7372f3cfa053555c9234b115c301c1d) by @Trozz)
- update release workflow to only trigger on semver tags and add attestations ([7dee5d1](https://github.com/pocket-id/terraform-provider-pocketid/commit/7dee5d1f06d1623a61816c1d667a509331495dd0) by @Trozz)

### Other

- improve code coverage for client package ([c92f55c](https://github.com/pocket-id/terraform-provider-pocketid/commit/c92f55c2c56003f18cae4b62be3b237cb3d06201) by @Trozz)
- add comprehensive tests for data sources ([f3b2a11](https://github.com/pocket-id/terraform-provider-pocketid/commit/f3b2a114e2862555dcf5a85c2859fecbb8d76274) by @Trozz)
- add comprehensive tests for provider and resources ([5f28569](https://github.com/pocket-id/terraform-provider-pocketid/commit/5f28569fa4d4a81f17f5785a9e0bd69558d25879) by @Trozz)
- update CI/CD configuration and documentation ([a819af5](https://github.com/pocket-id/terraform-provider-pocketid/commit/a819af5317f7683fbe350dbbb25bdb8829f2be31) by @Trozz)
- update go.mod and go.sum after running go mod tidy ([adb137e](https://github.com/pocket-id/terraform-provider-pocketid/commit/adb137e11a4ea17e2eb3e445c0e736e6401ee178) by @Trozz)
- remove version-bump workflow ([ed1865a](https://github.com/pocket-id/terraform-provider-pocketid/commit/ed1865a3c54baec68b44b98ba471914d0b047cba) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v0.1.1...v0.1.2

## v0.1.1

### Features

- add GitHub workflow to generate CONTRIBUTORS.md ([51851bf](https://github.com/pocket-id/terraform-provider-pocketid/commit/51851bfdc53c759f067746ab82a327f25d0f1360) by @Trozz)

### Bug Fixes

- downgrade golangci-lint to v1.54 for Go 1.21 compatibility ([c3de949](https://github.com/pocket-id/terraform-provider-pocketid/commit/c3de949cca2d29780c03df887ddd280d68df2fec) by @Trozz)
- add minimal golangci-lint config to avoid compatibility issues ([1236071](https://github.com/pocket-id/terraform-provider-pocketid/commit/1236071ffe12f17936748b39dd351bb126e649cb) by @Trozz)
- change user groups from List to Set type to prevent ordering issues ([9994117](https://github.com/pocket-id/terraform-provider-pocketid/commit/9994117d8fa6083d528f224e606476aefaa3495a) by @Trozz)

**Full Changelog**: https://github.com/pocket-id/terraform-provider-pocketid/compare/v0.1.0...v0.1.1

## v0.1.0

### Bug Fixes

- remove source archive and match HashiCorp provider example ([bbe9d1d](https://github.com/pocket-id/terraform-provider-pocketid/commit/bbe9d1d9dabb10845998ea1ecbe91db516a5882f) by @Trozz)
