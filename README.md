# trojan-darwin-universal

macOS universal build of [trojan-gfw/trojan`](https://github.com/trojan-gfw/trojan)

## Caveats

* This universal `trojan-gfw` binary is not [notarized](https://developer.apple.com/documentation/xcode/notarizing_macos_software_before_distribution), please remove the quarantine extended attribute before use:

  ```bash
  xattr -r com.apple.quarantine trojan-$VER-darwin.zip
  ```

## TODO

* Add a Homebrew Formula file.

* Use `macos-11.0` runner image in GitHub Actions when it's officially released.

  see: [macOS 11.0 pools will be transited to private preview. #2486](https://github.com/actions/virtual-environments/issues/2486)

