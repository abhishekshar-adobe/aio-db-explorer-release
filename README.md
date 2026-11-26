# AIO DB Explorer — Beta

A desktop app for browsing Adobe App Builder Database Storage from an authorized workspace. This is a beta release for evaluation; test with an approved non-production workspace first.

## Download

Choose the installer for your computer:

- [macOS — Apple Silicon (M1/M2/M3/M4)](https://github.com/abhishekshar-adobe/aio-db-explorer-release/releases/download/v0.2.0-beta.1/AIO%20DB%20Explorer-0.2.0-beta.1-mac-arm64.dmg)
- [macOS — Intel](https://github.com/abhishekshar-adobe/aio-db-explorer-release/releases/download/v0.2.0-beta.1/AIO%20DB%20Explorer-0.2.0-beta.1-mac-x64.dmg)
- [Windows — 64-bit](https://github.com/abhishekshar-adobe/aio-db-explorer-release/releases/download/v0.2.0-beta.1/AIO%20DB%20Explorer-0.2.0-beta.1-windows-x64.exe)

You can also browse all [releases](https://github.com/abhishekshar-adobe/aio-db-explorer-release/releases).

## Requirements

For real Adobe database connections, install:

- Node.js 20 or later
- Adobe I/O CLI (`aio`)
- Adobe App Builder storage plugin: `@adobe/aio-cli-plugin-app-storage`
- An authorized Adobe workspace JSON export with the required OAuth Server-to-Server credentials, plus access to a provisioned database

The app does not include credentials, the Adobe CLI, or the storage plugin. Never commit or share workspace JSON files, credentials, or tokens in this public repository.

## Install and connect

1. Download and install the package for your operating system. On macOS, open the DMG and drag **AIO DB Explorer** into **Applications**.
2. Start the app and choose your Adobe workspace JSON using the file picker.
3. Select the database region and confirm the workspace environment.
4. Choose **Connect to database**.

On Windows, install the Adobe CLI globally with npm if it is not already installed, then install the storage plugin using Adobe CLI's plugin installation instructions. Restart the Explorer after installing or changing the CLI.

## Beta notes

- This app can insert, edit, and permanently delete documents. Review the selected workspace, region, and document before confirming any change. Use least-privilege credentials and obtain workspace-owner approval, especially for Production.
- The workspace JSON is read locally; credentials are not displayed in the app. Keep the file private and use only a workspace you are authorized to access.
- Real Adobe connectivity depends on your CLI installation, credentials, permissions, and database provisioning. The app cannot grant access or provision a database.
- The macOS beta is ad-hoc signed and not notarized. The Windows installer is unsigned. Your operating system or company security policy may block or warn about these packages. Install only if permitted by your IT/security team; do not bypass company policy.
- Both macOS installers were smoke-tested. The Windows installer was built and inspected, but still needs testing on a Windows machine. Live Adobe connectivity has not been certified for this beta.
- Beta updates are manual. Check this repository's [releases](https://github.com/abhishekshar-adobe/aio-db-explorer-release/releases) for a newer version.

## Report an issue

When reporting a problem, include your operating system, app version, and a description of what you did. **Do not attach workspace JSON files, `.env` files, credentials, access tokens, or raw logs that may contain secrets.**
