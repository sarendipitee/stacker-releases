# Stacker releases

Public release packages and update information for the Stacker audio plugin.

Download installers and archives from [GitHub Releases](https://github.com/sarendipitee/stacker-releases/releases).
Packages will appear here when a release is published.

## Update manifest

[`latest.json`](latest.json) records the latest stable version as `{"version":"0.3.0"}`.
Stacker reads the raw file in the background and shows a small link near its logo when a newer version is available.

## Publishing a release

1. Build and validate the release packages in the source repository.
2. Create a GitHub Release tagged `vMAJOR.MINOR.PATCH` in this repository and attach the packages.
3. After the release and downloads are public, replace `latest.json` with the generated `build/release/packages/update/latest.json` from that build.

Use stable three-part versions (for example `0.3.1`); prereleases do not trigger notifications.
Publish the manifest last so installed plugins never announce downloads before they are available.
