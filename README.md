# Install ConformU

GitHub Action to install
[ASCOM ConformU](https://github.com/ASCOMInitiative/ConformU)
on Linux, Windows, and macOS.

## Usage

```yaml
- uses: ivonnyssen/conformu-install@v1
```

### With specific version

```yaml
- uses: ivonnyssen/conformu-install@v1
  with:
    version: v1.2.3
```

### With caching disabled

```yaml
- uses: ivonnyssen/conformu-install@v1
  with:
    cache: false
```

## Inputs

| Name | Description | Default |
| ------- | -------- | ------- |
| `version` | ConformU version to install | `latest` |
| `cache` | Enable caching of downloaded files | `true` |

## Outputs

| Name | Description |
| ---- | ----------- |
| `version` | Installed ConformU version |

## Supported Platforms

- Linux (x64)
- Windows (x64)
- macOS (Intel/Apple Silicon)
