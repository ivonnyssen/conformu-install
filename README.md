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

### With caching

```yaml
- name: Install ConformU
  id: conformu
  uses: ivonnyssen/conformu-install@v1

- uses: actions/cache@v5
  with:
    key: ${{ steps.conformu.outputs.cache-key }}
    path: |
      conformu.linux-x64.tar.xz
      ConformU.*.Setup.exe
      ConformU-Installer.dmg
```

## Inputs

| Name | Description | Default |
| ------- | -------- | ------- |
| `version` | ConformU version to install | `latest` |

## Outputs

| Name | Description |
| ---- | ----------- |
| `version` | Installed ConformU version |
| `cache-key` | Cache key for actions/cache |

## Supported Platforms

- Linux (x64)
- Windows (x64)
- macOS (Intel/Apple Silicon)
