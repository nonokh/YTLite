# Changelog

All notable changes to YouTube Plus (formerly YTLite) will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [5.2-beta3] - 2024-08-11

### Overview
YouTube Plus (formerly YTLite) is a flexible enhancer for YouTube on iOS, featuring over a hundred customizable options. This release continues to improve compatibility and features for YouTube version 20.32.4.

### ✨ Features
- **Download Capabilities**: Download videos, audio (with audio track selection), thumbnails, posts, and profile pictures
- **Information Tools**: Copy video, comment, and post information for easy sharing
- **Interface Customization**: 
  - Remove unwanted feed elements
  - Reorder tabs to your preference
  - Enable OLED mode for battery savings on OLED displays
  - Shorts-only mode for dedicated Shorts viewing
- **Player Settings**: 
  - Advanced gesture controls
  - Default quality selection
  - Preferred audio track selection
- **Settings Management**: Save, load, and restore settings; clear cache manually or automatically on app startup
- **Built-in SponsorBlock**: Skip sponsored segments automatically
- **And much more**: Over 100+ customizable options

### 🔧 Supported Integrations
This release supports integration with the following tweaks:
- **YouPiP**: Enable native Picture-in-Picture for YouTube videos
- **YTUHD**: Unlock 1440p (2K) and 2160p (4K) video quality options
- **Return YouTube Dislikes**: Restore the dislike counter on videos
- **YouQuality**: Quick video quality selector in the video overlay
- **DontEatMyContent**: Prevent the notch/Dynamic Island from cropping video content

### 📱 Compatibility
- **YouTube Version**: 20.32.4 (Latest confirmed)
- **iOS**: Compatible with iOS devices supporting YouTube
- **Date Tested**: August 11, 2024

### 📦 Installation Methods
1. **Jailbroken Devices**: Install via your preferred package manager
2. **Sideloading**: Build your own IPA using GitHub Actions (see README for instructions)

### 🔗 Resources
- **Source Code**: [GitHub Repository](https://github.com/dayanch96/YTLite)
- **Build Instructions**: See README.md for detailed build steps
- **FAQ**: Available in multiple languages (English, Russian, Italian, Polish)

### 🙏 Credits
- **Main Developer**: dvntm (dayanch96)
- **Contributors**: All contributors are listed in the Contributors section
- **Open Source Libraries**: Listed in the Open Source Libraries section within the app

### 📝 Notes
- This is a beta release. Please report any issues on GitHub
- Make sure to use a decrypted YouTube IPA for sideloading
- Preferences can be found in YouTube Settings

---

## How to Build

To build YouTube Plus app:

1. **Fork this repository**
2. **Enable Actions** in your fork (Repository Settings > Actions > Enable Read and Write permissions)
3. **Navigate to Actions tab** and select "Create YouTube Plus app"
4. **Provide required inputs**:
   - Decrypted YouTube IPA URL
   - Select desired tweak integrations
   - Customize BundleID and Display Name (optional)
   - Choose tweak version (default: latest)
5. **Run the workflow** and download from Releases section

For detailed instructions, see the [README](README.md).

---

## Version History

### [5.2-beta3] - 2024-08-11
- Current release (see details above)

### Previous Versions
- Version history will be updated as new releases are published
- Check [GitHub Releases](https://github.com/nonokh/YTLite/releases) for compiled IPAs
- Check [dayanch96/YTLite](https://github.com/dayanch96/YTLite) for source releases

---

## Reporting Issues

If you encounter any issues:
1. Check the [FAQ](FAQs/FAQ_EN.md) first
2. Search existing [GitHub Issues](https://github.com/nonokh/YTLite/issues)
3. Create a new issue with detailed information:
   - YouTube version
   - YTLite version
   - iOS version
   - Steps to reproduce
   - Expected vs actual behavior

---

## License

This project is provided as-is for educational purposes. Please respect YouTube's Terms of Service.
