# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.0.3] - 2025-12-02

### Fixed

- Fixed `ostt-float.sh` script to correctly locate ostt binary when installed via package managers (Homebrew, AUR, shell installer)
- Fixed Hyprland hotkey binding syntax in documentation - added missing description parameter for `bind` command

### Changed

- Removed PKGBUILD from main repository - now maintained separately in AUR repository
- Enhanced platform-specific setup documentation for Hyprland/Omarchy and macOS
- Improved README structure with clearer authentication and platform setup sections

### Migration Notes

**Linux users upgrading from v0.0.2:**
- Update `~/.local/bin/ostt-float` script: Re-run `ostt` once to regenerate the fixed script, or manually update using the [latest version](https://github.com/kristoferlund/ostt/blob/main/environments/hyprland/ostt-float.sh)
- Update Hyprland hotkey binding in `~/.config/hypr/hyprland.conf`:
  ```diff
  - bind = SUPER, R, exec, bash ~/.local/bin/ostt-float
  + bind = SUPER, R, ostt, exec, bash ~/.local/bin/ostt-float
  ```
- Reload Hyprland config: `hyprctl reload`

## [0.0.2] - 2025-12-01

### Added

- Initial public release
- Real-time audio recording with waveform visualization
- Speech-to-text transcription via OpenAI and Deepgram providers
- Transcription history browser with clipboard integration
- Keyword management for improved transcription accuracy
- Hyprland/Omarchy floating window integration
- Cross-platform support (Linux and macOS)
- Multiple installation methods (Homebrew, AUR, shell installer)

[unreleased]: https://github.com/kristoferlund/ostt/compare/v0.0.3...HEAD
[0.0.3]: https://github.com/kristoferlund/ostt/compare/v0.0.2...v0.0.3
[0.0.2]: https://github.com/kristoferlund/ostt/releases/tag/v0.0.2
