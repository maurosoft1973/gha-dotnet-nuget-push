# NuGet Push

Uses the NuGet CLI `nuget push` [command](https://learn.microsoft.com/en-us/nuget/reference/cli-reference/cli-ref-push) that pushes a package to a package source and publishes it. Leverages the official [setup-nuget action](https://github.com/nuget/setup-nuget/) pre-configured specifically for the majority.

## Usage

To use this action in your GitHub repository, you can follow these steps:

```yaml
uses: maurosoft1973/nuget-push@v1
```

### Inputs

```yaml
with:
  # The NuGet Server URL.
  source: 'https://api.nuget.org/v3/index.json'
  # The NuGet API key.
  token:
  # Defines the name of the packet to be sent to the Nuget server
  packageName: 'package.1.0.0.nupkg'
  # Sets the verbosity level of the command. Allowed values are quiet, normal and detailed.
  level: 'quiet'
```

### Outputs

This action has no outputs.

## Examples

### Deploy to nuget&#46;org

```yaml
steps:
  - name: Push packages to NuGet
    uses: maurosoft1973/nuget-push@v1
    with:
      token: ${{ secrets.NUGET_TOKEN }}
```

## Contributing to NuGet Push

Contributions are welcome! 
Feel free to submit issues, feature requests, or pull requests to help improve this action.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
