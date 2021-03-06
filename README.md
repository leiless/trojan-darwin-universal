# trojan-darwin-universal

[![Build status](https://github.com/leiless/trojan-darwin-universal/actions/workflows/build.yml/badge.svg)](https://github.com/leiless/trojan-darwin-universal/actions/workflows/build.yml)
![Apple Silicon ready](https://img.shields.io/badge/Apple%20Silicon-ready-33cc00)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

Feel solid to use macOS universal [trojan-gfw/trojan](https://github.com/trojan-gfw/trojan) in your Apple Silicon based Mac.

## Caveats

* This universal `trojan-gfw` binary is not [notarized](https://developer.apple.com/documentation/xcode/notarizing_macos_software_before_distribution), please remove the quarantine extended attribute before use:

  ```bash
  # Prepend `sudo` if you met permission denied error
  xattr -r com.apple.quarantine trojan-$VER-darwin.zip
  ```

* This is not an official build, and provides no any warranty and support.

  Please visit [trojan-gfw/trojan/issues](https://github.com/trojan-gfw/trojan/issues) if you found anything wrong.

* This repository will be archived eventually since Apple will cease Intel Mac product line.

  In which case, there will only one arch binary. i.e. `arm64[e]`

## TODO

* Add a Homebrew Formula file.

* Use `macos-11.0` runner image in GitHub Actions when it's general available.

  see: [macOS 11.0 pools will be transited to private preview. #2486](https://github.com/actions/virtual-environments/issues/2486)

## Reference

[[Misc] Made a universal trojan build for macOS #579](https://github.com/trojan-gfw/trojan/issues/579)
