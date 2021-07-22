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

## 1.2
**target commit**: 294724fae38ffa4ebcf6dfb0854787fb7022d1e6

**base librewolf version**: 89.x

**References**:
- issue [#65](https://gitlab.com/librewolf-community/settings/-/issues/65) from settings
- issue [#22](https://gitlab.com/librewolf-community/browser/common/-/issues/22) from common

#### Removed preferences
```
defaultPref("dom.webaudio.enabled", false);
defaultPref("media.navigator.enabled", false);
```

#### Changed preferences
```
defaultPref("app.support.baseURL", "https://gitlab.com/librewolf-community/settings/-/wikis/support#");
```

## 1.3
**target commit**: 60e75e30c6018a5c909a2f00f40831ed3f1948a6

**base librewolf version**: 90.x

#### Added preferences
```
defaultPref("network.http.windows-sso.enabled", false);
```

#### Removed preferences
```
lockPref("browser.cache.offline.storage.enable", false); // pref does not exist anymore as it became default behavior
```

## 1.4
**target commit**: 2e21db4c3018321a077d9af2ec44b29675c57adf

**base librewolf version**: 90.x

#### Removed preferences
```
lockPref("security.tls.version.enable-deprecated", false); // default
```
