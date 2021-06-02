# LibreWolf settings

LibreWolf settings for all platforms.

The configuration file was revamped and it includes improvements in usability, a more curated and focused selection of privacy settings, as well as the ability to override preferences with an external file.
The old configuration (now tagged as `legacy`) should be considered deprecated and it will no longer be maintained.

We encourage users to find **their own setup** and to use our default configuration as something to build on top of. This is now easier thanks to the overrides, just place your own preferences in the proper location, according to your OS and install method:
- Most distros and macOS -> `~/.librewolf/librewolf.overrides.cfg`
- Flatpak -> `~/.var/app/io.gitlab.librewolf-community/.librewolf/librewolf.overrides.cfg`
- Windows -> `%USERPROFILE%\.librewolf\librewolf.overrides.cfg`

## Useful links
- [FAQ](https://gitlab.com/librewolf-community/settings/-/wikis/FAQ): to help you creating your own pref file.
- [LibreWolf distributions](https://gitlab.com/librewolf-community/browser)
- [Issue tracker](https://gitlab.com/librewolf-community/settings/-/issues)
- Our community on [gitter](https://gitter.im/librewolf-community/librewolf)
- [Website](https://librewolf-community.gitlab.io/)
- [Docs](https://librewolf.readthedocs.io/en/latest/)
- [r/LibreWolf](https://www.reddit.com/r/LibreWolf/)

## Notes and thanks
This repository benefits from the knowledge and research provided by [arkenfox](https://github.com/arkenfox), their documentation was vital to this revamp, so special thanks to their project.
We do not use arkenfox's user.js but we try to keep up with it, and we also consider it a great resource for users who want to find their own setup.

Some of the older prefs in this project are taken from [pyllyukko](https://github.com/pyllyukko/user.js/) and many more were investigated on [bugzilla](https://bugzilla.mozilla.org/home).

Thank you to the whole LibreWolf community as once again this is entirely a community effort.