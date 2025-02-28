# Hass.io Core Add-on: Configurator

Browser-based configuration file editor for Home Assistant.

![Supports aarch64 Architecture][aarch64-shield] ![Supports amd64 Architecture][amd64-shield] ![Supports armhf Architecture][armhf-shield] ![Supports armv7 Architecture][armv7-shield] ![Supports i386 Architecture][i386-shield]

![Configurator in the Home Assistant Frontend][screenshot]

## About

The Configurator is a small web-app (you access it via web browser) that provides a
filesystem-browser and text-editor to modify files on the machine the Configurator is
running on. It has been created to allow easy configuration of Home Assistant.

It is powered by Ace editor, which supports syntax highlighting for various
code/markup languages. YAML files (the default language for Home Assistant
configuration files) will be automatically checked for syntax errors while editing.

## Features

- Web-based editor to modify your files with syntax highlighting and YAML linting.
- Upload and download files.
- Stage, stash and commit changes in Git repositories, create and switch between
  branches, push to remotes, view diffs.
- Lists with available entities, triggers, events, conditions and services.
- Restart Home Assistant directly with the click of a button. Reloading groups,
  automations, etc. can be done as well. An API password is required.
- Direct links to Home Assistant documentation and icons.
- Execute shell commands within the add-on container.
- Editor settings are saved in your browser.
- And much more…

## Installation

The installation of this add-on is straightforward and easy to do.

1. Navigate in your Home Assistant frontend to **Hass.io** -> **Add-on Store**.
2. Find the "Configurator" add-on and click it.
3. Click on the "INSTALL" button.

## How to use

In general, this add-on requires no configuration from your end.

1. Toggle the "Show in sidebar" option, which adds the Configurator to the main menu.
2. Start the add-on.
3. Refresh your browser, the "Configurator" is now visible in the sidebar.
4. Click on the "Configurator" menu option and start configuring!

## Configuration

Add-on configuration:

```json
{
  "dirsfirst": false,
  "enforce_basepath": false,
  "ignore_pattern": [
    "__pycache__"
  ]
}
```

### Option: `dirsfirst` (required)

This option allows you to list directories before files in the file browser tree.

Set it to `true` to list files first, `false` otherwise.

### Option: `enforce_basepath` (required)

If set to `true`, access is limited to files within the `/config` directory.

### Option: `ignore_pattern` (required)

This option allows you to hide files and folders from the file browser tree.
By default, it hides the `__pycache__` folders.

## Known issues and limitations

- This add-on is, by default, configured for use with Hass.io Ingress. If you
  wish to access the add-on via a its own port directly, you can simply
  assign a port in the "Network" section of the add-on setting page.

## Support

Got questions?

You have several options to get them answered:

- The [Home Assistant Discord Chat Server][discord].
- The Home Assistant [Community Forum][forum].
- Join the [Reddit subreddit][reddit] in [/r/homeassistant][reddit]

In case you've found an bug, please [open an issue on our GitHub][issue].

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[discord]: https://discord.gg/c5DvZ4e
[forum]: https://community.home-assistant.io
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[issue]: https://github.com/home-assistant/hassio-addons/issues
[reddit]: https://reddit.com/r/homeassistant
[repository]: https://github.com/hassio-addons/repository
[screenshot]: https://github.com/home-assistant/hassio-addons/raw/master/configurator/images/screenshot.png
