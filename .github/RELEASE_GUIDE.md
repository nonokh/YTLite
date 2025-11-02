# Release Guide for YouTube Plus

This guide explains how to create and manage releases for the YouTube Plus project.

## Overview

The YouTube Plus project uses GitHub Actions to build and release IPA files. When a workflow completes successfully, it automatically creates a release with comprehensive release notes.

## Release Types

### 1. Standard Release (main.yml)
- **Purpose**: Create standard YouTube Plus IPA builds
- **Tag Format**: `ytp-{run_number}`
- **Filename**: `YouTubePlus_{version}.ipa`
- **Status**: Published (automatically visible)

### 2. Beta Release (ytp_beta.yml)
- **Purpose**: Test beta versions with custom tweak URLs
- **Tag Format**: `ytp-beta-{run_number}`
- **Filename**: `YouTubePlus_Beta.ipa`
- **Status**: Prerelease (marked as beta)

### 3. cyan/TrollStore Release (cyan_ts.yml)
- **Purpose**: Create cyan and TrollFools packages
- **Tag Format**: `ytp-{run_number}`
- **Filename**: `cyan_YouTubePlus_{version}.cyan` and/or `TrollFools_YouTubePlus_{version}.zip`
- **Status**: Published

## Automated Release Notes

All workflows now include comprehensive release notes with:

- ✨ Build information (version, build number, date)
- 📦 What's included (integrations, components)
- 🚀 Installation instructions (platform-specific)
- 🔍 Where to find preferences
- 📖 Documentation links
- ⚠️ Important disclaimers
- 🙏 Credits

## How to Create a Release

### Using GitHub Actions

1. **Navigate to Actions Tab**
   - Go to your repository on GitHub
   - Click the "Actions" tab

2. **Select Workflow**
   - Choose "Create YouTube Plus app" (standard)
   - Or "Build YouTube Plus app" (beta with custom URL)
   - Or "Create YouTube Plus app (cyan/TrollStore)" (for cyan/TrollFools)

3. **Run Workflow**
   - Click "Run workflow" button
   - Fill in required parameters:
     - Decrypted YouTube IPA URL (required)
     - Tweak version (defaults to latest)
     - Enable/disable integrations (YouPiP, YTUHD, etc.)
     - Custom Bundle ID and Display Name (optional)

4. **Wait for Build**
   - The workflow will build the IPA
   - Upon success, a release is automatically created
   - Release notes are auto-generated

5. **Download from Releases**
   - Go to repository/releases
   - Download the newly created IPA

## Manually Editing a Release

If you need to edit a release after it's created:

1. Go to the Releases page
2. Find the release you want to edit
3. Click "Edit" button
4. Modify title, description, or upload additional files
5. Save changes

## Release Note Template

A template is available at `.github/RELEASE_TEMPLATE.md` for reference when creating manual releases or updating existing ones.

## Changelog Management

The project maintains a `CHANGELOG.md` file that documents:
- Version history
- Feature changes
- Compatibility information
- Breaking changes

### Updating CHANGELOG.md

When releasing a new version:

1. Open `CHANGELOG.md`
2. Add a new section at the top:
   ```markdown
   ## [X.Y.Z] - YYYY-MM-DD
   
   ### Added
   - New features
   
   ### Changed
   - Modified features
   
   ### Fixed
   - Bug fixes
   ```
3. Commit and push changes

## Best Practices

### Release Naming
- Use semantic versioning for tweak versions (e.g., 5.2-beta3, 5.3.0)
- Include build number for tracking specific builds
- Mark beta releases appropriately

### Release Notes
- Keep installation instructions clear and concise
- Always include compatibility information
- Link to FAQs and documentation
- List all integrated tweaks
- Include important disclaimers

### Testing
- Test IPA builds before announcing releases
- Verify all download links work
- Check that release notes render correctly
- Ensure integrations are properly listed

### Communication
- Announce new releases in project discussions
- Update README if compatibility changes
- Document breaking changes prominently

## Troubleshooting

### Release Not Created
- Check workflow logs for errors
- Verify GitHub token permissions (Settings > Actions > Read and Write)
- Ensure workflow completed successfully

### Missing Release Notes
- Release notes are auto-generated from workflow
- Check workflow YAML for `body:` section
- Verify GitHub Actions permission to create releases

### Download Links Not Working
- Verify IPA file was uploaded
- Check file name matches in workflow
- Ensure release is published (not draft)

## File Locations

- Main workflow: `.github/workflows/main.yml`
- Beta workflow: `.github/workflows/ytp_beta.yml`
- cyan/TrollStore workflow: `.github/workflows/cyan_ts.yml`
- Release template: `.github/RELEASE_TEMPLATE.md`
- Changelog: `CHANGELOG.md`
- README: `README.md`

## Links

- [GitHub Releases Documentation](https://docs.github.com/en/repositories/releasing-projects-on-github)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Semantic Versioning](https://semver.org/)

---

For questions or issues, please open a GitHub issue or discussion.
