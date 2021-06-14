This changelog will be used from now on to document changes in a precise manner, with a list of changes for each setting version.
Setting versions are documented using the pref `librewolf.cfg.version`, available in about:config.

## 1.0
**target commit**: 2b8dc4ac6d7fb6fdf8f172d04c27912098268257

**base librewolf version**: 89.x

This is the initial release from which we start tagging and versioning settings.

## 1.1
**target commit**: cf0a2cc88acdbc51b138228353a0d7c9ea0db7c3

**base librewolf version**: 89.x

**References**:
- issue [#54](https://gitlab.com/librewolf-community/settings/-/issues/54) from settings
- merge request [#5](https://gitlab.com/librewolf-community/browser/common/-/merge_requests/5) from common

#### Removed preferences
```
defaultPref("security.OCSP.require", false); // default value
defaultPref("extensions.update.url", "");
defaultPref("extensions.update.background.url", "");
defaultPref("extensions.getAddons.search.browseURL", "");
```

#### Changed preferences
```
defaultPref("geo.provider.network.url", "https://location.services.mozilla.com/v1/geolocate?key=%MOZILLA_API_KEY%");
```

#### Added preferences
```
lockPref("privacy.override_rfp_for_color_scheme", false);
```
