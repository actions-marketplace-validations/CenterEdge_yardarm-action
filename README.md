# CenterEdge/yardarm-action@v1
Contains a GitHub action for the OpenAPI 3 SDK 3 generator, Yardarm

## Usage
```yaml
- uses: CenterEdge/yardarm-action@v1
  with:
    yardarm: 0.3.x
    dotnet-version: 6.0.x
    args: generate -i my-spec.yaml -n MySpec -v 1.0.0 -o output/directory/ -x Yardarm.NewtonsoftJson Yardarm.MicrosoftExtensionsHttp
```

## Inputs
- `yardarm` - The version of yardarm to install as a dotnet tool, supports semver, eg `0.3.x` for the latest `0.3` version or `latest` for latest
- `dotnet-version` - The version of dotnet to setup, this uses the official `actions/setup-dotnet` action
- `pre-release` - Set to true to enable prerelease searching for the yardarm version
- `args` - The args to pass directly to the `yardarm` command
