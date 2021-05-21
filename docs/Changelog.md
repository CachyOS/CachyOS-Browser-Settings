## Changelog
#### Added
Previously missing, now added
```
defaultPref("pdfjs.enableScripting", false);
lockPref("browser.contentblocking.category", "custom"); // changing to other options is currently broken anyway
lockPref("browser.contentblocking.cfr-milestone.enabled", false);
lockPref("browser.contentblocking.database.enabled", false);
lockPref("browser.contentblocking.cryptomining.preferences.ui.enabled", false);
lockPref("browser.contentblocking.fingerprinting.preferences.ui.enabled", false);
lockPref("browser.contentblocking.report.hide_vpn_banner", true);
lockPref("browser.contentblocking.report.show_mobile_app", false);
defaultPref("extensions.formautofill.creditCards.available", false);
defaultPref("extensions.formautofill.addresses.capture.enabled", false);
defaultPref("extensions.formautofill.section.enabled", false); // hide formautofill section in settings, which is useless and buggy atm
defaultPref("media.peerconnection.ice.proxy_only_if_behind_proxy", true);
lockPref("network.trr.send_empty_accept-encoding_headers", false);
lockPref("browser.newtabpage.activity-stream.section.highlights.includePocket", false);
lockPref("browser.newtabpage.activity-stream.improvesearch.topSiteSearchShortcuts", false);
lockPref("browser.newtabpage.activity-stream.improvesearch.topSiteSearchShortcuts.havePinned", "");
lockPref("browser.newtabpage.activity-stream.showSponsoredTopSites", false);
lockPref("browser.newtabpage.activity-stream.feeds.topsites",	false);
lockPref("browser.newtabpage.activity-stream.feeds.system.topsites",    false);
lockPref("browser.newtabpage.activity-stream.feeds.system.topstories",	false);
lockPref("app.normandy.dev_mode", false);
lockPref("toolkit.telemetry.shutdownPingSender.enabledFirstSession", false);
defaultPref("browser.urlbar.dnsResolveSingleWordsAfterSearch", 0);
defaultPref("dom.security.https_only_mode_pbm", true);
lockPref("browser.ping-centre.telemetry", false);
lockPref("browser.region.network.url", "");
lockPref("browser.region.update.enabled", false);
defaultPref("dom.popup_allowed_events", "click dblclick mousedown pointerdown");
defaultPref("extensions.postDownloadThirdPartyPrompt", false);
defaultPref("general.warnOnAboutConfig", false);
defaultPref("network.auth.subresource-http-auth-allow", 1);
defaultPref("browser.display.use_system_colors", false);
defaultPref("browser.cache.disk.enable", false);
defaultPref("fission.autostart", true);
```

#### Modified
Updated some present prefs to better one
```
defaultPref("network.cookie.cookieBehavior", 5); // dFPI, previously set to 1
lockPref("browser.cache.offline.storage.enable", false); // Previously browser.cache.offline.insecure.enable
lockPref("network.http.referer.XOriginTrimmingPolicy", 2); // Previously set to 0
lockPref("network.http.referer.XOriginPolicy", 0); // Previously set to 1
defaultPref("privacy.clearOnShutdown.offlineApps", false); // For consistency with new cookie behavior
defaultPref("privacy.cpd.offlineApps", false); // For consistency with new cookie behavior
lockPref("devtools.performance.recording.ui-base-url", "http://localhost:55555"); // Previously redirected to localhost:4242
defaultPref("media.autoplay.blocking_policy", 2); // Previously media.autoplay.enabled.user-gestures-needed
defaultPref("media.memory_cache_max_size", 65536); // previously lockPref("media.memory_cache_max_size", 16384);
```

#### Removed
Active prefs that were removed
```
lockPref("network.cookie.same-site.enabled", true); // Deprecated
lockPref("network.cookie.leave-secure-alone", true); // Deprecated
lockPref("browser.contentblocking.reportBreakage.enabled", false); // Deprecated
lockPref("browser.contentblocking.rejecttrackers.reportBreakage.enabled", false); // Deprecated
lockPref("browser.contentblocking.rejecttrackers.ui.enabled", false); // Deprecated
lockPref("browser.contentblocking.trackingprotection.control-center.ui.enabled", false); // Deprecated
lockPref("browser.contentblocking.trackingprotection.ui.enabled", false); // Deprecated
pref("signon.management.page.mobileAndroidURL", ""); // Deprecated
pref("signon.management.page.mobileAppleURL", ""); // Deprecated
lockPref("browser.urlbar.openViewOnFocus", false); // Handled through patch
lockPref("browser.urlbar.update1", false); // Handled through patch
lockPref("browser.urlbar.update1.interventions", false); // Handled through patch
lockPref("browser.urlbar.update1.searchTips", false); // Handled through patch
defaultPref("places.history.expiration.max_pages", 2147483647); // Useless
defaultPref("media.gmp-manager.url.override", "data:text/plain,"); // To easily enable DRM
defaultPref("media.gmp-manager.updateEnabled", false); // Deprecated
defaultPref("media.gmp-widevinecdm.autoupdate", false); // Deprecated
defaultPref("media.gmp-eme-adobe.enabled", false); // Deprecated
defaultPref("media.gmp-manager.certs.2.commonName", ""); // To easily enable DRM
defaultPref("media.gmp-manager.certs.1.commonName", ""); // To easily enable DRM
defaultPref("media.gmp.trial-create.enabled", false); // To easily enable DRM
lockPref("dom.indexedDB.enabled", true); // Deprecated
lockPref("dom.w3c_pointer_events.enabled", false); // Deprecated
lockPref("offline-apps.allow_by_default", false); // Deprecated
lockPref("ui.use_standins_for_native_colors", true); // Interferes with RFP
lockPref("dom.event.highrestimestamp.enabled", true); // Deprecated
lockPref("browser.urlbar.usepreloadedtopurls.enabled", false); // Deprecated
lockPref("browser.urlbar.oneOffSearches", false); // Deprecated
lockPref("dom.disable_window_open_feature.close", true); // Deprecated
lockPref("dom.disable_window_open_feature.location", true); // Deprecated
lockPref("dom.disable_window_open_feature.menubar", true); // Deprecated
lockPref("dom.disable_window_open_feature.minimizable", true); // Deprecated
lockPref("dom.disable_window_open_feature.personalbar", true); // Deprecated
lockPref("dom.disable_window_open_feature.resizable", true); // Deprecated
lockPref("dom.disable_window_open_feature.status", true); // Deprecated
lockPref("dom.disable_window_open_feature.titlebar", true); // Deprecated
lockPref("dom.disable_window_open_feature.toolbar", true); // Deprecated
lockPref("security.csp.experimentalEnabled", true); // Deprecated
lockPref("security.csp.enable_violation_events", false); // Deprecated
lockPref("gecko.handlerService.schemes.ircs.0.uriTemplate", ""); // Duplicated in the file
lockPref("browser.newtabpage.activity-stream.asrouter.userprefs.cfr", false); // Deprecated
lockPref("extensions.htmlaboutaddons.discover.enabled", false); // Deprecated
lockPref("browser.messaging-system.fxatoolbarbadge.enabled", false); // Deprecated
lockPref("browser.onboarding.notification.tour-ids-queue", ""); // Deprecated
lockPref("devtools.gcli.lodashSrc", ""); // Deprecated
lockPref("devtools.webide.templatesURL", ""); // Deprecated
lockPref("browser.ping-centre.production.endpoint", ""); // Deprecated
lockPref("gecko.handlerService.schemes.ircs.0.name", ""); // Duplicated in the file
lockPref("services.sync.fxa.privacyURL", ""); // Deprecated
lockPref("services.settings.default_signer", ""); // Deprecated
lockPref("app.productInfo.baseURL", ""); // Deprecated
lockPref("devtools.webide.adbAddonURL", ""); // Deprecated
lockPref("lightweightThemes.recommendedThemes", ""); // Deprecated
defaultPref("media.gmp-gmpopenh264.autoupdate", false); // Adroid FF only
lockPref("browser.newtabpage.activity-stream.prerender", false); // Deprecated
lockPref("browser.newtabpage.activity-stream.aboutHome.enabled", false); // Deprecated
lockPref("browser.newtabpage.activity-stream.disableSnippets", true); // Deprecated
lockPref("privacy.donottrackheader.value", 1); // Deprecated
defaultPref("privacy.userContext.longPressBehavior", 2); // Deprecated
defaultPref("browser.tabs.closeWindowWithLastTab", true); // Already default
lockPref("dom.forms.datetime", false); // Deprecated
lockPref("browser.download.hide_plugins_without_extensions", false); // Deprecated
lockPref("services.sync.clients.lastSync", "0"); // Deprecated
lockPref("services.sync.clients.lastSyncLocal", "0"); // Deprecated
lockPref("services.sync.enabled", false); // Deprecated
lockPref("services.sync.jpake.serverURL", ""); // Deprecated
lockPref("services.sync.migrated", true); // Deprecated
lockPref("services.sync.prefs.sync.browser.safebrowsing.downloads.password", false); // Deprecated
lockPref("services.sync.serverURL", ""); // Deprecated
lockPref("services.sync.tabs.lastSyncLocal", "0"); // Deprecated
lockPref("services.sync.engine.bookmarks.buffer", false); // Deprecated
lockPref("services.sync.prefs.sync.browser.sessionstore.restore_on_demand", false); // Deprecated
lockPref("services.sync.prefs.sync.browser.urlbar.suggest.history.onlyTyped", false); // Deprecated
lockPref("services.sync.prefs.sync.browser.urlbar.matchBuckets", false); // Deprecated
lockPref("services.sync.prefs.sync.browser.urlbar.autocomplete.enabled", false); // Deprecated
lockPref("services.sync.prefs.sync.extensions.personas.current", false); // Deprecated
lockPref("services.sync.prefs.sync.lightweightThemes.selectedThemeID", false); // Deprecated
lockPref("services.sync.prefs.sync.lightweightThemes.usedThemes", false); // Deprecated
lockPref("services.sync.prefs.sync.pref.advanced.images.disable_button.view_image", false); // Deprecated
lockPref("services.sync.prefs.sync.pref.advanced.javascript.disable_button.advanced", false); // Deprecated
lockPref("services.sync.prefs.sync.security.OCSP.enabled", false); // Deprecated
lockPref("services.sync.prefs.sync.security.OCSP.require", false); // Deprecated
lockPref("services.sync.prefs.sync.security.tls.version.max", false); // Deprecated
lockPref("services.sync.prefs.sync.security.tls.version.min", false); // Deprecated
lockPref("services.sync.prefs.sync.xpinstall.whitelist.required", false); // Deprecated
lockPref("prio.publicKeyB", ""); // Deprecated
lockPref("prio.publicKeyA", ""); // Deprecated
lockPref("browser.chrome.errorReporter.publicKey", ""); // Deprecated
lockPref("security.insecure_password.ui.enabled", true); // Deprecated
defaultPref("network.dns.localDomains", "librefox.com"); // Doesn't make sense at all
lockPref("security.ssl.errorReporting.automatic", false); // Deprecated
lockPref("security.ssl.errorReporting.url", ""); // Deprecated
lockPref("security.ssl.errorReporting.enabled", false); // Deprecated
defaultPref("layout.frame_rate.precise", true); // Deprecated
defaultPref("layers.offmainthreadcomposition.enabled", true); // Deprecated
defaultPref("layers.async-video.enabled", true); // Deprecated
defaultPref("layers.offmainthreadcomposition.async-animations", true); // Default true and not important to set
defaultPref("html5.offmainthread", true); // Default true and not important to set
defaultPref("browser.tabs.animate", false); // Deprecated
lockPref("webgl.disable-extensions", true); // Deprecated
lockPref("browser.onboarding.notification.finished", true); // Deprecated
lockPref("browser.onboarding.tour.onboarding-tour-customize.completed", true); // Deprecated
lockPref("browser.onboarding.tour.onboarding-tour-performance.completed", true); // Deprecated
lockPref("devtools.onboarding.telemetry.logged", false); // Deprecated
lockPref("pref.general.disable_button.default_browser", false); // Deprecated
lockPref("pref.privacy.disable_button.view_passwords", false); // Deprecated
lockPref("browser.urlbar.daysBeforeHidingSuggestionsPrompt", 0); // Deprecated
lockPref("browser.urlbar.searchSuggestionsChoice", false); // Deprecated
lockPref("browser.urlbar.timesBeforeHidingSuggestionsHint", 0); // Deprecated
lockPref("app.update.silent", false); // Deprecated
lockPref("app.vendorURL", ""); // Deprecated
lockPref("browser.chrome.errorReporter.submitUrl", ""); // Deprecated
lockPref("browser.chrome.errorReporter.enabled", false); // Deprecated
lockPref("browser.ping-centre.staging.endpoint", ""); // Deprecated
lockPref("devtools.devedition.promo.url", ""); // Deprecated
lockPref("devtools.gcli.imgurUploadURL", ""); // Deprecated
lockPref("devtools.gcli.jquerySrc", ""); // Deprecated
lockPref("devtools.gcli.underscoreSrc", ""); // Deprecated
lockPref("devtools.telemetry.supported_performance_marks", ""); // Deprecated
lockPref("dom.permissions.enabled", false); // Deprecated
lockPref("extensions.blocklist.url", ""); // Deprecated
lockPref("geo.wifi.uri", ""); // Deprecated
lockPref("geo.provider-country.network.scan", false); // Deprecated
lockPref("geo.provider-country.network.url", ""); // Deprecated
lockPref("identity.fxaccounts.service.sendLoginUrl", ""); // Deprecated
lockPref("lpbmode.enabled", true); // Deprecated
lockPref("mailnews.messageid_browser.url", ""); // Deprecated
lockPref("mailnews.mx_service_url", ""); // Deprecated
lockPref("network.predictor.cleaned-up", true); // Deprecated
lockPref("plugins.crash.supportUrl", ""); // Deprecated
lockPref("sync.enabled", false); // Deprecated
lockPref("sync.jpake.serverURL", ""); // Deprecated
lockPref("sync.serverURL", ""); // Deprecated
lockPref("toolkit.telemetry.hybridContent.enabled", false); // Deprecated
lockPref("toolkit.telemetry.infoURL", ""); // Deprecated
lockPref("toolkit.telemetry.prompted", 2); // Deprecated
lockPref("toolkit.telemetry.rejected", true); // Deprecated
lockPref("toolkit.telemetry.coverage.opt-out", true); // Deprecated
lockPref("browser.aboutHomeSnippets.updateUrl", ""); // Deprecated
lockPref("dom.enable_user_timing", false); // Deprecated
lockPref("geo.wifi.logging.enabled", false); // Deprecated
lockPref("browser.search.geoSpecificDefaults.url", ""); // Deprecated
lockPref("browser.search.geoSpecificDefaults", false); // Deprecated
lockPref("browser.fixup.hide_user_pass", true); // Deprecated
lockPref("privacy.storagePrincipal.enabledForTrackers", false); // redundant with dFPI
defaultPref("layout.css.visited_links_enabled", false); // https://bugzilla.mozilla.org/show_bug.cgi?id=1632765
defaultPref("layout.css.always-repaint-on-unvisited", false); // no benefit with RFP enabled -> https://github.com/arkenfox/user.js/issues/933
defaultPref("layout.css.notify-of-unvisited", false); // no benefit with RFP enabled
defaultPref("dom.event.contextmenu.enabled", false); // causes breakage with no demonstrated privacy benefit
lockPref("dom.registerProtocolHandler.insecure.enabled", true); // Deprecated
defaultPref("dom.security.https_only_mode_ever_enabled", true); // Triggered by dom.security.https_only_mode = true
lockPref("dom.enable_resource_timing", false); // conflicting with RFP
lockPref("device.sensors.enabled", false); // conflicting with RFP
lockPref("dom.gamepad.enabled", false); // conflicting with RFP
lockPref("dom.netinfo.enabled", false); // conflicting with RFP
lockPref("media.video_stats.enabled", false); // conflicting with RFP
lockPref("webgl.enable-debug-renderer-info", false); // conflicting with RFP
defaultPref("extensions.getAddons.themes.browseURL", ""); // Deprecated
lockPref("extensions.getAddons.compatOverides.url", ""); // Used for tests on localhost:8888
defaultPref("extensions.ui.experiment.hidden", false); // Deprecated
defaultPref("extensions.webextensions.tabhide.enabled", false); // Deprecated
lockPref("dom.enable_performance", false); // conflicting with RFP
lockPref("dom.enable_performance_navigation_timing", false);  // conflicting with RFP
lockPref("security.mixed_content.upgrade_display_content", true); // not worth having https://github.com/arkenfox/user.js/issues/754
lockPref("security.ssl3.ecdhe_ecdsa_rc4_128_sha", false); // Deprecated
lockPref("security.ssl3.ecdhe_rsa_rc4_128_sha", false); // Deprecated
lockPref("security.ssl3.rsa_rc4_128_md5", false); // Deprecated
lockPref("security.ssl3.rsa_rc4_128_sha", false); // Deprecated
lockPref("security.tls.unrestricted_rc4_fallback", false); // Deprecated
lockPref("security.ssl3.ecdh_ecdsa_rc4_128_sha", false); // Deprecated
lockPref("security.ssl3.ecdh_rsa_rc4_128_sha", false); // Deprecated
lockPref("security.ssl3.rsa_seed_sha", false); // Deprecated
lockPref("security.ssl3.rsa_des_ede3_sha", false); // known to leak and increase fingerprint
lockPref("security.ssl3.rsa_aes_256_sha", false); // known to leak and increase fingerprint
lockPref("security.ssl3.rsa_aes_128_sha", false); // known to leak and increase fingerprint
lockPref("browser.safebrowsing.allowOverride", false); // we do not have SB enabled so we don't care if the bypass button is shown
defaultPref("browser.ctrlTab.recentlyUsedOrder", false); // why should be disable this?
lockPref("services.blocklist.onecrl.collection", ""); // Deprecated
lockPref("font.blacklist.underline_offset", ""); // knwown to increase fingerprint
lockPref("plugin.defaultXpi.state", 1); // Deprecated
lockPref("remote.log.level", "Info"); // already default and not important in any way
lockPref("webgl.min_capability_mode", true); // small to no gain according to arkenfox and TOR, breaks websites on the other side
lockPref("lightweightThemes.update.enabled", false); // Deprecated 
lockPref("lightweightThemes.persisted.headerURL", false); // Deprecated 
lockPref("lightweightThemes.persisted.footerURL", false); // Deprecated 
lockPref("network.protocol-handler.warn-external-default",true); // any real benefit? 
lockPref("network.protocol-handler.external.javascript",false); // any real benefit? 
lockPref("network.protocol-handler.external.moz-extension",false); // any real benefit? 
lockPref("network.protocol-handler.external.ftp",false);// any real benefit? 
lockPref("network.protocol-handler.external.file",false);// any real benefit? 
lockPref("network.protocol-handler.external.about",false);// any real benefit? 
lockPref("network.protocol-handler.external.chrome",false);// any real benefit? 
lockPref("network.protocol-handler.external.blob",false);// any real benefit? 
lockPref("network.protocol-handler.external.data",false);// any real benefit? 
lockPref("network.protocol-handler.expose-all",false);// any real benefit? 
lockPref("network.protocol-handler.expose.http",true);// any real benefit? 
lockPref("network.protocol-handler.expose.https",true);// any real benefit? 
lockPref("network.protocol-handler.expose.javascript",true);// any real benefit? 
lockPref("network.protocol-handler.expose.moz-extension",true);// any real benefit? 
lockPref("network.protocol-handler.expose.ftp",true);// any real benefit? 
lockPref("network.protocol-handler.expose.file",true);// any real benefit? 
lockPref("network.protocol-handler.expose.about",true);// any real benefit? 
lockPref("network.protocol-handler.expose.chrome",true);// any real benefit? 
lockPref("network.protocol-handler.expose.blob",true);// any real benefit? 
lockPref("network.protocol-handler.expose.data",true);// any real benefit? 
lockPref("network.protocol-handler.external.http",false);// any real benefit? 
lockPref("network.protocol-handler.external.https",false);// any real benefit?
lockPref("shumway.disabled", true); // Deprecated
lockPref("plugin.state.libgnome-shell-browser-plugin", 0); // Deprecated
lockPref("plugins.click_to_play", true); // Deprecated
lockPref("plugin.sessionPermissionNow.intervalInMinutes", 0); // Deprecated
lockPref("devtools.webide.enabled", false); // Deprecated
lockPref("devtools.webide.autoinstallADBExtension", false); // Deprecated
lockPref("network.allow-experiments", false); // Deprecated
lockPref("browser.urlbar.userMadeSearchSuggestionsChoice", true); // Deprecated
lockPref("network.netlink.route.check.IPv4", "127.0.0.1"); // Deprecated
lockPref("network.netlink.route.check.IPv6", "::1"); // Deprecated
lockPref("network.negotiate-auth.allow-insecure-ntlm-v1", false); // Deprecated
lockPref("network.negotiate-auth.allow-insecure-ntlm-v1-https", false); // Deprecated
lockPref("security.tls.version.max", 4); // increases fingerprint
defaultPref("network.dns.blockDotOnion", true); // TOR is out of scope
lockPref("network.http.referer.hideOnionSource", true); // TOR is out of scope
lockPref("browser.onboarding.enabled", false); // Deprecated
lockPref("dom.mozTCPSocket.enabled", false); // Useless according to https://gitlab.torproject.org/legacy/trac/-/issues/27268#comment:2
lockPref("devtools.webide.autoinstallADBHelper", false); // Deprecated
lockPref("app.update.enabled", false); // Deprecated
lockPref("browser.casting.enabled", false); // Deprecated, probably Android only
lockPref("browser.newtabpage.activity-stream.enabled", false); // Deprecated
lockPref("browser.newtabpage.directory.ping", "data:text/plain,"); // Deprecated
lockPref("browser.newtabpage.directory.source", "data:text/plain,"); // Deprecated
lockPref("browser.newtabpage.enhanced", false); // Deprecated
lockPref("browser.selfsupport.url", ""); // Deprecated
lockPref("camera.control.face_detection.enabled", false); // Deprecated
lockPref("datareporting.healthreport.about.reportUrl", "data:,"); // Deprecated
lockPref("datareporting.healthreport.service.enabled", false); // Deprecated
lockPref("devtools.webide.autoinstallFxdtAdapters", false); // Deprecated
lockPref("devtools.webide.adaptersAddonURL", ""); // Deprecated
lockPref("dom.flyweb.enabled", false); // Deprecated
lockPref("dom.push.udp.wakeupEnabled", false); // Deprecated
lockPref("dom.telephony.enabled", false); // Deprecated
lockPref("extensions.shield-recipe-client.enabled", false); // Deprecated
lockPref("loop.logDomains", false); // Deprecated
lockPref("network.websocket.enabled", false); // Deprecated
lockPref("security.xpconnect.plugin.unrestricted", false); // Deprecated
lockPref("social.directories", ""); // Deprecated
lockPref("social.remote-install.enabled", false); // Deprecated
lockPref("social.whitelist", ""); // Deprecated
lockPref("pref.privacy.disable_button.change_blocklist", true); // seems to have no effect and probably deprecated
lockPref("pref.privacy.disable_button.tracking_protection_exceptions", true); // seems to have no effect and probably deprecated
lockPref("browser.pocket.enabled", false); // Deprecated
defaultPref("toolkit.legacyUserProfileCustomizations.stylesheets", false); // already default value and not that important, can still be flipped easily
lockPref("plugin.scan.plid.all", false); // Win-only, plugins are disabled so it's redundant
lockPref("webgl.dxgl.enabled", false); // Win-only, marked as useless https://github.com/arkenfox/user.js/issues/714
lockPref("browser.search.countryCode", "US"); // Deprecated
lockPref("experiments.activeExperiment", false); // Deprecated
lockPref("experiments.enabled", false); // Deprecated
lockPref("experiments.manifest.uri", ""); // Deprecated
lockPref("experiments.supported", false); // Deprecated
lockPref("network.jar.block-remote-files", true); // Deprecated
lockPref("network.jar.open-unsafe-types", false); // Deprecated
lockPref("plugin.state.java", 0); // Deprecated
lockPref("trailhead.firstrun.branches", "join-privacy"); // Deprecated
lockPref("services.blocklist.update_enabled", false); // Deprecated
lockPref("shield.savant.enabled", false); // Deprecated
defaultPref("gfx.direct2d.disabled", false); // Win-only, default and probably out of scope
defaultPref("layers.acceleration.disabled", false); // default and probably out of scope
lockPref("browser.taskbar.previews.enable", false); // personal pref
lockPref("browser.taskbar.lists.enabled", false); // personal pref
lockPref("browser.taskbar.lists.frequent.enabled", false); // personal pref
lockPref("browser.taskbar.lists.recent.enabled", false); // personal pref
lockPref("browser.taskbar.lists.tasks.enabled", false); // personal pref
defaultPref("webgl.force-enabled", true); // out of scope, not worth
defaultPref("layers.acceleration.force-enabled", true); // out of scope, not worth
lockPref("privacy.trackingprotection.testing.report_blocked_node", false); // default false and we have tracking protection disabled
lockPref("privacy.trackingprotection.origin_telemetry.enabled", false); // default false and we have tracking protection disabled
lockPref("privacy.trackingprotection.lower_network_priority", false); // default
lockPref("telemetry.origin_telemetry_test_mode.enabled", false); // default false and we have tracking protection disabled
lockPref("signon.storeSignons", false); // Deprecated
lockPref("browser.urlbar.filter.javascript", true); // default
lockPref("browser.search.geoip.url", ""); // Deprecated
defaultPref("privacy.clearOnShutdown.siteSettings", false); // default
defaultPref("privacy.clearOnShutdown.cache", true); // default
defaultPref("privacy.clearOnShutdown.sessions", true); // default
defaultPref("privacy.clearOnShutdown.downloads", true); // default
defaultPref("privacy.clearOnShutdown.formdata", true); // default
defaultPref("privacy.clearOnShutdown.history", true); // default
defaultPref("privacy.cpd.siteSettings", false); // default
defaultPref("privacy.cpd.downloads", true); // default
defaultPref("privacy.cpd.cache", true); // default
defaultPref("privacy.cpd.formdata", true); // default
defaultPref("privacy.cpd.history", true); // default
defaultPref("privacy.cpd.passwords", false); // default
defaultPref("privacy.cpd.sessions", true); // default
defaultPref("extensions.formautofill.addresses.capture.enabled", false); // default
lockPref("signon.autofillForms.http", false); // default
lockPref("network.trr.send_user-agent_headers", false); // default
lockPref("network.dns.disablePrefetchFromHTTPS", true); // default
lockPref("dom.imagecapture.enabled", false); // default
lockPref("dom.reporting.crash.enabled", false); // default
defaultPref("network.proxy.autoconfig_url.include_path", false); // default
lockPref("security.tls.version.min", 3); // default
defaultPref("extensions.webextensions.background-delayed-startup", true); //default
defaultPref("xpinstall.signatures.required", true); // default
lockPref("app.normandy.dev_mode", false); // default
defaultPref("pdfjs.enableWebGL", false); // default
lockPref("browser.cache.offline.enable", false); // apparently increases fingerprinting and redundant with browser.cache.offline.storage.enable
lockPref("network.predictor.enable-prefetch", false); // default
lockPref("network.http.referer.spoofSource", false);  // default
defaultPref("network.http.referer.defaultPolicy", 2);  // default
defaultPref("network.http.referer.defaultPolicy.pbmode", 2);  // default
defaultPref("layout.spellcheckDefault", 2); // why?
lockPref("privacy.trackingprotection.introURL", ""); // Deprecated
defaultPref("general.appname.override", "Netscape"); // no benefit over RFP
defaultPref("general.appversion.override", "5.0 (Windows)"); // no benefit over RFP, and it doesn't spoof
defaultPref("general.platform.override", "Win32"); // no benefit over RFP, and it doesn't spoof
defaultPref("general.oscpu.override", "Windows NT 6.1"); // no benefit over RFP, and it doesn't spoof
lockPref("general.buildID.override", "20100101"); // no benefit over RFP
lockPref("browser.startup.homepage_override.buildID", "20100101"); // no benefit over RFP
defaultPref("general.useragent.override", "Mozilla/5.0 (Windows NT 10.0; rv:78.0) Gecko/20100101 Firefox/78.0"); // no benefit over RFP and without may increase FP
lockPref("security.insecure_connection_icon.enabled", true); // Default
lockPref("security.insecure_connection_icon.pbmode.enabled", true); // Default
lockPref("browser.bookmarks.restore_default_bookmarks", false); // Default
lockPref("browser.contentblocking.cfr-milestone.enabled", false); // not needed with contenblocking disabled
lockPref("app.normandy.first_run", false); // default
lockPref("browser.send_pings", false); // default
lockPref("browser.send_pings.require_same_host", true); // default
defaultPref("browser.tabs.closeTabByDblclick", true); // why?
lockPref("devtools.debugger.force-local", true); // default
lockPref("gfx.offscreencanvas.enabled", false); // default
lockPref("media.webspeech.recognition.enable", false); // default
lockPref("network.auth.subresource-img-cross-origin-http-auth-allow", false); // default
lockPref("remote.force-local", true); // default
lockPref("security.data_uri.block_toplevel_data_uri_navigations", true); // default
lockPref("security.fileuri.strict_origin_policy", true); // default
lockPref("security.insecure_field_warning.contextual.enabled", true); // default
defaultPref("security.remote_settings.intermediates.enabled", true); // default
lockPref("xpinstall.whitelist.required", true); // default
lockPref("browser.sessionhistory.max_entries", 20); // why?
lockPref("extensions.webapi.testing", false); // hidden but default false
lockPref("canvas.capturestream.enabled", false); // any real benefit?
lockPref("network.http.redirection-limit", 10); // small benefit from having it at default 20, and break some payments
defaultPref("dom.event.clipboardevents.enabled", false); // causes breakage with small benefits, moved to hardened setup
lockPref("webgl.disable-fail-if-major-performance-caveat", true); // default
lockPref("network.trr.send_empty_accept-encoding_headers", false); // why?

// fxaccounts is disabled in policies
lockPref("identity.fxaccounts.enabled", false);
lockPref("identity.fxaccounts.remote.root", "");
lockPref("identity.fxaccounts.auth.uri", "");
lockPref("identity.fxaccounts.commands.enabled", false);
lockPref("identity.fxaccounts.remote.oauth.uri", "");
lockPref("identity.fxaccounts.remote.profile.uri", "");
lockPref("identity.fxaccounts.service.monitorLoginUrl", "");

// all handled by lockPref("services.settings.server", "")
lockPref("services.blocklist.addons.collection", "");
lockPref("services.blocklist.plugins.collection", "");
lockPref("services.blocklist.gfx.collection", "");
lockPref("services.blocklist.addons.signer", "");
lockPref("services.blocklist.gfx.signer", "");
lockPref("services.settings.security.onecrl.signer", "");
lockPref("services.blocklist.pinning.signer", "");
lockPref("services.blocklist.plugins.signer", "");

// useless as fxaccounts are off
lockPref("services.sync.addons.trustedSourceHostnames", "");
lockPref("services.sync.lastversion", "");
lockPref("services.sync.maxResyncs", 0); // 1
lockPref("services.sync.telemetry.maxPayloadCount", 0); //500
lockPref("services.sync.addons.ignoreUserEnabledChanges", true); //false
lockPref("services.sync.engine.addons", false); //true
lockPref("services.sync.engine.addresses", false); //false
lockPref("services.sync.engine.addresses.available", false);
lockPref("services.sync.engine.bookmarks", false); //true
lockPref("services.sync.engine.creditcards", false); //false
lockPref("services.sync.engine.creditcards.available", false); //false
lockPref("services.sync.engine.history", false); //true
lockPref("services.sync.engine.passwords", false); //true
lockPref("services.sync.engine.prefs", false); //true
lockPref("services.sync.engine.tabs", false); //true
lockPref("services.sync.log.appender.file.logOnError", false); //true
lockPref("services.sync.log.appender.file.logOnSuccess", false); //false
lockPref("services.sync.log.cryptoDebug", false); //false
lockPref("services.sync.sendVersionInfo", false); //true
lockPref("services.sync.syncedTabs.showRemoteIcons", true); //true
lockPref("services.sync.prefs.sync.services.sync.syncedTabs.showRemoteIcons", false); //true
lockPref("services.sync.prefs.sync.accessibility.blockautorefresh", false); //true
lockPref("services.sync.prefs.sync.accessibility.browsewithcaret", false); //true
lockPref("services.sync.prefs.sync.accessibility.typeaheadfind", false); //true
lockPref("services.sync.prefs.sync.accessibility.typeaheadfind.linksonly", false); //true
lockPref("services.sync.prefs.sync.addons.ignoreUserEnabledChanges", true); //true
lockPref("services.sync.prefs.sync.browser.contentblocking.category", false); //true
lockPref("services.sync.prefs.sync.browser.contentblocking.features.strict", false); //true
lockPref("services.sync.prefs.sync.browser.ctrlTab.recentlyUsedOrder", false); //true
lockPref("services.sync.prefs.sync.browser.download.useDownloadDir", false); //true
lockPref("services.sync.prefs.sync.browser.formfill.enable", false); //true
lockPref("services.sync.prefs.sync.browser.link.open_newwindow", false); //true
lockPref("services.sync.prefs.sync.browser.newtabpage.enabled", false); //true
lockPref("services.sync.prefs.sync.browser.newtabpage.pinned", false); //true
lockPref("services.sync.prefs.sync.browser.newtabpage.activity-stream.section.highlights.includePocket", false); //true
lockPref("services.sync.prefs.sync.browser.newtabpage.activity-stream.section.highlights.includeVisited", false); //true
lockPref("services.sync.prefs.sync.browser.newtabpage.activity-stream.section.highlights.includeBookmarks", false); //true
lockPref("services.sync.prefs.sync.browser.newtabpage.activity-stream.section.highlights.includeDownloads", false); //true
lockPref("services.sync.prefs.sync.browser.newtabpage.activity-stream.section.highlights.rows", false); //true
lockPref("services.sync.prefs.sync.browser.newtabpage.activity-stream.section.topstories.rows", false); //true
lockPref("services.sync.prefs.sync.browser.offline-apps.notify", false); //true
lockPref("services.sync.prefs.sync.browser.search.update", false); //true
lockPref("services.sync.prefs.sync.browser.search.widget.inNavBar", false); //true
lockPref("services.sync.prefs.sync.browser.sessionstore.warnOnQuit", false); //true
lockPref("services.sync.prefs.sync.browser.startup.homepage", false); //true
lockPref("services.sync.prefs.sync.browser.startup.page", false); //true
lockPref("services.sync.prefs.sync.browser.tabs.loadInBackground", false); //true
lockPref("services.sync.prefs.sync.browser.tabs.warnOnClose", false); //true
lockPref("services.sync.prefs.sync.browser.tabs.warnOnOpen", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.maxRichResults", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.suggest.bookmark", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.suggest.history", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.suggest.engines", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.suggest.topsites", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.suggest.openpage", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.suggest.searches", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.resultBuckets", false); //true
lockPref("services.sync.prefs.sync.browser.urlbar.showSearchSuggestionsFirst", false); //true
lockPref("services.sync.prefs.sync.dom.disable_open_during_load", false); //true
lockPref("services.sync.prefs.sync.dom.disable_window_flip", false); //true
lockPref("services.sync.prefs.sync.dom.disable_window_move_resize", false); //true
lockPref("services.sync.prefs.sync.dom.event.contextmenu.enabled", false); //true
lockPref("services.sync.prefs.sync.dom.security.https_only_mode", false); //true
lockPref("services.sync.prefs.sync.dom.security.https_only_mode_ever_enabled", false); //true
lockPref("services.sync.prefs.sync.dom.security.https_only_mode_ever_enabled_pbm", false); //true
lockPref("services.sync.prefs.sync.dom.security.https_only_mode_pbm", false); //true
lockPref("services.sync.prefs.sync.extensions.activeThemeID", false); //true
lockPref("services.sync.prefs.sync.extensions.update.enabled", false); //true
lockPref("services.sync.prefs.sync.intl.accept_languages", false); //true
lockPref("services.sync.prefs.sync.intl.regional_prefs.use_os_locales", false); //true
lockPref("services.sync.prefs.sync.layout.spellcheckDefault", false); //true
lockPref("services.sync.prefs.sync.network.cookie.cookieBehavior", false); //true
lockPref("services.sync.prefs.sync.network.cookie.lifetimePolicy", false); //true
lockPref("services.sync.prefs.sync.network.cookie.thirdparty.sessionOnly", false); //true
lockPref("services.sync.prefs.sync.permissions.default.image", false); //true
lockPref("services.sync.prefs.sync.pref.downloads.disable_button.edit_actions", false); //true
lockPref("services.sync.prefs.sync.pref.privacy.disable_button.cookie_exceptions", false); //true
lockPref("services.sync.prefs.sync.privacy.clearOnShutdown.cache", false); //true
lockPref("services.sync.prefs.sync.privacy.clearOnShutdown.cookies", false); //true
lockPref("services.sync.prefs.sync.privacy.clearOnShutdown.downloads", false); //true
lockPref("services.sync.prefs.sync.privacy.clearOnShutdown.formdata", false); //true
lockPref("services.sync.prefs.sync.privacy.clearOnShutdown.history", false); //true
lockPref("services.sync.prefs.sync.privacy.clearOnShutdown.offlineApps", false); //true
lockPref("services.sync.prefs.sync.privacy.clearOnShutdown.sessions", false); //true
lockPref("services.sync.prefs.sync.privacy.clearOnShutdown.siteSettings", false); //true
lockPref("services.sync.prefs.sync.privacy.donottrackheader.enabled", false); //true
lockPref("services.sync.prefs.sync.privacy.fuzzyfox.clockgrainus", false); //true
lockPref("services.sync.prefs.sync.privacy.fuzzyfox.enabled", false); //true
lockPref("services.sync.prefs.sync.privacy.reduceTimerPrecision", false); //true
lockPref("services.sync.prefs.sync.privacy.resistFingerprinting", false); //true
lockPref("services.sync.prefs.sync.privacy.resistFingerprinting.reduceTimerPrecision.jitter", false); //true
lockPref("services.sync.prefs.sync.privacy.resistFingerprinting.reduceTimerPrecision.microseconds", false); //true
lockPref("services.sync.prefs.sync.privacy.sanitize.sanitizeOnShutdown", false); //true
lockPref("services.sync.prefs.sync.privacy.trackingprotection.enabled", false); //true
lockPref("services.sync.prefs.sync.privacy.trackingprotection.pbmode.enabled", false); //true
lockPref("services.sync.prefs.sync.privacy.trackingprotection.cryptomining.enabled", false); //true
lockPref("services.sync.prefs.sync.privacy.trackingprotection.fingerprinting.enabled", false); //true
lockPref("services.sync.prefs.sync.privacy.userContext.enabled", false); //true
lockPref("services.sync.prefs.sync.privacy.userContext.newTabContainerOnLeftClick.enabled", false); //true
lockPref("services.sync.prefs.sync.security.default_personal_cert", false); //true
lockPref("services.sync.prefs.sync.spellchecker.dictionary", false); //true
lockPref("services.sync.prefs.sync.signon.rememberSignons", false);
lockPref("services.sync.prefs.sync.signon.management.page.breach-alerts.enabled", false);
lockPref("services.sync.prefs.sync.signon.generation.enabled", false);
lockPref("services.sync.prefs.sync.signon.autofillForms", false);
lockPref("services.sync.declinedEngines", "");
lockPref("services.sync.globalScore", 0);
lockPref("services.sync.nextSync", 0);
lockPref("services.sync.prefs.sync.browser.safebrowsing.downloads.enabled", false);
lockPref("services.sync.prefs.sync.browser.safebrowsing.malware.enabled", false);
lockPref("services.sync.prefs.sync.browser.safebrowsing.downloads.remote.block_potentially_unwanted", false);
lockPref("services.sync.prefs.sync.browser.safebrowsing.phishing.enabled", false);
lockPref("services.sync.tabs.lastSync", "0");

// useless as ui elements are not in the report page
lockPref("browser.contentblocking.report.cookie.url", "");
lockPref("browser.contentblocking.report.cryptominer.url", "");
lockPref("browser.contentblocking.report.endpoint_url", "");
lockPref("browser.contentblocking.report.fingerprinter.url", "");
lockPref("browser.contentblocking.report.lockwise.how_it_works.url", "");
lockPref("browser.contentblocking.report.manage_devices.url", "");
lockPref("browser.contentblocking.report.monitor.how_it_works.url", "");
lockPref("browser.contentblocking.report.monitor.sign_in_url", "");
lockPref("browser.contentblocking.report.monitor.home_page_url", "");
lockPref("browser.contentblocking.report.monitor.preferences", "");
lockPref("browser.contentblocking.report.monitor.url", "");
lockPref("browser.contentblocking.report.proxy.enabled", false);
lockPref("browser.contentblocking.report.proxy_extension.url", "");
lockPref("browser.contentblocking.report.social.url", "");
lockPref("browser.contentblocking.report.tracker.url", "");
lockPref("browser.contentblocking.report.vpn.url", "");
lockPref("browser.contentblocking.report.vpn-promo.url", "");
lockPref("browser.contentblocking.report.vpn-ios.url", "");
lockPref("browser.contentblocking.report.vpn-android.url", "");

// urls that do not damage and make re-enabling TP a pain
lockPref("browser.contentblocking.reportBreakage.url", "");
defaultPref("browser.safebrowsing.provider.mozilla.pver", "");
defaultPref("browser.safebrowsing.provider.mozilla.lists", "");
defaultPref("browser.safebrowsing.provider.mozilla.lists.base", "");
defaultPref("browser.safebrowsing.provider.mozilla.lists.content", "");
defaultPref("browser.safebrowsing.provider.mozilla.lastupdatetime", "");
defaultPref("browser.safebrowsing.provider.mozilla.nextupdatetime", "");
lockPref("urlclassifier.trackingTable", "");
lockPref("browser.contentblocking.database.enabled", false);

lockPref("privacy.trackingprotection.socialtracking.enabled", false); // default
defaultPref("network.stricttransportsecurity.preloadlist",	false); // nothing wrong with hsts
lockPref("security.ssl.disable_session_identifiers", true); // covered by isolation, large performance hit
// defaultPref("intl.regional_prefs.use_os_locales", false); // default and already commented
lockPref("extensions.screenshots.upload-disabled", true); // deprecated feature
lockPref("dom.ipc.plugins.reportCrashURL", false); // flash is gone, does nothing
lockPref("dom.ipc.plugins.flash.subprocess.crashreporter.enabled", false); // flash is gone, does nothing
lockPref("plugin.state.flash", 0); // flash is gone, does nothing
defaultPref("alerts.showFavicons", false); // default
lockPref("plugin.default.state", 1); // default
lockPref("extensions.pocket.enabled", false); // pocket is already disabled
lockPref("extensions.pocket.site", ""); // pocket is already disabled
lockPref("extensions.pocket.oAuthConsumerKey", ""); // pocket is already disabled
lockPref("extensions.pocket.api", ""); // pocket is already disabled
defaultPref("accessibility.typeaheadfind", false); // default
defaultPref("reader.parse-on-load.enabled", false); // no need to have it locked, even Tor Browser re-enabled it
lockPref("gecko.handlerService.schemes.webcal.0.uriTemplate", ""); // default
defaultPref("network.proxy.socks_version", 5); // default
defaultPref("network.proxy.autoconfig_url", ""); // default
defaultPref("extensions.formautofill.section.enabled", false); // no effect
```
#### Commented
Prefs that need to be addressed and that were disabled for now
```
// all covered by previous prefs
// defaultPref("media.navigator.video.enabled", false);
// defaultPref("media.peerconnection.use_document_iceservers", false);
// defaultPref("media.peerconnection.identity.enabled", false);
// defaultPref("media.peerconnection.identity.timeout", 1);
// defaultPref("media.peerconnection.turn.disable", true);
// defaultPref("media.peerconnection.ice.tcp", false);

// blocklist is a security feature, best left at default
// defaultPref("extensions.blocklist.enabled", false);
// defaultPref("extensions.blocklist.detailsURL", "");
// defaultPref("extensions.blocklist.itemURL", "");

// commented all below as they do no harm and make enabling SB painful
// could potentially at some point
// defaultPref("browser.safebrowsing.id", "");
// defaultPref("browser.safebrowsing.provider.google4.pver", "");
// defaultPref("browser.safebrowsing.provider.google4.advisoryName", "");
// defaultPref("browser.safebrowsing.provider.google4.advisoryURL", "");
// defaultPref("browser.safebrowsing.provider.google4.lists", "");
// defaultPref("browser.safebrowsing.provider.google4.reportMalwareMistakeURL", "");
// defaultPref("browser.safebrowsing.provider.google4.reportPhishMistakeURL", "");
// defaultPref("browser.safebrowsing.provider.google4.reportURL", "");
// defaultPref("browser.safebrowsing.provider.google4.lastupdatetime", "");
// defaultPref("browser.safebrowsing.provider.google4.nextupdatetime", "");
// defaultPref("browser.safebrowsing.provider.google.advisoryName", "");
// defaultPref("browser.safebrowsing.provider.google.advisoryURL", "");
// defaultPref("browser.safebrowsing.provider.google.lastupdatetime", "");
// defaultPref("browser.safebrowsing.provider.google.lists", "");
// defaultPref("browser.safebrowsing.provider.google.nextupdatetime", "");
// defaultPref("browser.safebrowsing.provider.google.pver", "");
// defaultPref("browser.safebrowsing.provider.google.reportMalwareMistakeURL", "");
// defaultPref("browser.safebrowsing.provider.google.reportPhishMistakeURL", "");
// defaultPref("browser.safebrowsing.provider.google.reportURL", "");
// defaultPref("browser.safebrowsing.reportPhishURL", "");
```

#### Unlocked
Locked prefs that were unlocked, more should be unlocked probably
```
defaultPref("general.config.filename", "librewolf.cfg");
defaultPref("privacy.donottrackheader.enabled", true); // Unlocked as some think it increases fingerprint, they can now disable it
defaultPref("permissions.default.geo", 2); // Unlocked as some think it increases fingerprint, they can now disable it
defaultPref("extensions.getAddons.themes.browseURL", "")
defaultPref("pdfjs.enableWebGL", false);
defaultPref("pdfjs.previousHandler.alwaysAskBeforeHandling", true);
defaultPref("pdfjs.enabledCache.state", false);
defaultPref("alerts.showFavicons", false); // default: false
defaultPref("security.remote_settings.intermediates.enabled", true);
defaultPref("dom.battery.enabled", false); // Unlocked as some think it increases fingerprint, they can now disable it
defaultPref("extensions.blocklist.enabled", false);
defaultPref("extensions.blocklist.detailsURL", "");
defaultPref("extensions.blocklist.itemURL", "");
defaultPref("security.OCSP.enabled", 0); // someone might want to have it on for security concerns
defaultPref("security.OCSP.require", false);
defaultPref("reader.parse-on-load.enabled", false);
defaultPref("webgl.enable-webgl2", false);
defaultPref("geo.provider.network.url", "");
defaultPref("geo.provider.network.logging.enabled", false);
defaultPref("network.http.referer.XOriginTrimmingPolicy", 2);
defaultPref("network.http.referer.XOriginPolicy", 0);
defaultPref("browser.download.manager.addToRecentDocs", false);
defaultPref("accessibility.force_disabled", 1);
defaultPref("network.manage-offline-status", false);
defaultPref("browser.helperApps.deleteTempFileOnExit", true);
defaultPref("dom.push.enabled", false);
defaultPref("dom.push.connection.enabled", false);
defaultPref("dom.push.serverURL", ""); //default "wss://push.services.mozilla.com/"
defaultPref("dom.push.userAgentID", "");
defaultPref("dom.targetBlankNoOpener.enabled", true);
defaultPref("dom.disable_window_move_resize", true);
defaultPref("dom.disable_beforeunload", true);
defaultPref("dom.popup_maximum", 4);
defaultPref("dom.vr.enabled", false);
defaultPref("dom.vibrator.enabled", false);
defaultPref("network.stricttransportsecurity.preloadlist",	false);
defaultPref("browser.ssl_override_behavior", 1);
defaultPref("security.tls.version.fallback-limit", 3);
defaultPref("browser.xul.error_pages.expert_bad_cert", true); // advanced ui infos
defaultPref("extensions.enabledScopes", 5);
defaultPref("extensions.autoDisableScopes", 11);
defaultPref("xpinstall.signatures.devInfoURL", "");
defaultPref("security.cert_pinning.enforcement_level", 2);
defaultPref("devtools.performance.recording.ui-base-url", "http://localhost:55555"); // Default Value : https://profiler.firefox.com
defaultPref("devtools.devices.url", "");
defaultPref("devtools.remote.adb.extensionURL", ""); // [FF64+]
defaultPref("devtools.remote.adb.extensionID", ""); // default adb@mozilla.org [FF64+]
defaultPref("browser.safebrowsing.id", "");
defaultPref("browser.safebrowsing.blockedURIs.enabled", false);
defaultPref("browser.safebrowsing.provider.google4.pver", "");
defaultPref("browser.safebrowsing.provider.google4.advisoryName", "");
defaultPref("browser.safebrowsing.provider.google4.advisoryURL", "");
defaultPref("browser.safebrowsing.provider.google4.dataSharing.enabled", false);
defaultPref("browser.safebrowsing.provider.google4.dataSharingURL", "");
defaultPref("browser.safebrowsing.provider.google4.gethashURL", "");
defaultPref("browser.safebrowsing.provider.google4.lists", "");
defaultPref("browser.safebrowsing.provider.google4.reportMalwareMistakeURL", "");
defaultPref("browser.safebrowsing.provider.google4.reportPhishMistakeURL", "");
defaultPref("browser.safebrowsing.provider.google4.reportURL", "");
defaultPref("browser.safebrowsing.provider.google4.updateURL", "");
defaultPref("browser.safebrowsing.provider.google4.lastupdatetime", "");
defaultPref("browser.safebrowsing.provider.google4.nextupdatetime", "");
defaultPref("browser.safebrowsing.provider.google.advisoryName", "");
defaultPref("browser.safebrowsing.provider.google.advisoryURL", "");
defaultPref("browser.safebrowsing.provider.google.gethashURL", "");
defaultPref("browser.safebrowsing.provider.google.lastupdatetime", "");
defaultPref("browser.safebrowsing.provider.google.lists", "");
defaultPref("browser.safebrowsing.provider.google.nextupdatetime", "");
defaultPref("browser.safebrowsing.provider.google.pver", "");
defaultPref("browser.safebrowsing.provider.google.reportMalwareMistakeURL", "");
defaultPref("browser.safebrowsing.provider.google.reportPhishMistakeURL", "");
defaultPref("browser.safebrowsing.provider.google.reportURL", "");
defaultPref("browser.safebrowsing.provider.google.updateURL", "");
defaultPref("browser.safebrowsing.provider.mozilla.pver", "");
defaultPref("browser.safebrowsing.provider.mozilla.lists", "");
defaultPref("browser.safebrowsing.provider.mozilla.lists.base", "");
defaultPref("browser.safebrowsing.provider.mozilla.lists.content", "");
defaultPref("browser.safebrowsing.provider.mozilla.updateURL", "");
defaultPref("browser.safebrowsing.provider.mozilla.gethashURL", "");
defaultPref("browser.safebrowsing.provider.mozilla.lastupdatetime", "");
defaultPref("browser.safebrowsing.provider.mozilla.nextupdatetime", "");
defaultPref("browser.safebrowsing.reportPhishURL", "");
defaultPref("browser.safebrowsing.malware.enabled", false);
defaultPref("browser.safebrowsing.passwords.enabled", false);
defaultPref("browser.safebrowsing.phishing.enabled", false);
defaultPref("browser.urlbar.trimURLs", false);
defaultPref("browser.search.suggest.enabled", false);
defaultPref("browser.search.region", "US");
defaultPref("browser.urlbar.suggest.searches", false);
defaultPref("browser.search.update", false);
defaultPref("browser.contentblocking.cryptomining.preferences.ui.enabled", false); // enable UI elements of TP if you want to use it
defaultPref("browser.contentblocking.fingerprinting.preferences.ui.enabled", false); // enable UI elements of TP if you want to use it
defaultPref("privacy.trackingprotection.cryptomining.enabled", false); // user can manually choose what to do once he enables UI with the above prefs
defaultPref("privacy.trackingprotection.fingerprinting.enabled", false); // user can manually choose what to do once he enables UI with the above prefs
```

#### To discuss
Prefs that need to be addressed and potential roadmap
```
Open points:
// How much should we lock? -> being addressed, see above
// How in depth should we go with urls
// SB - make re-enabling easier, test connections
// GEO - review to allow easier re-enabling -> tested that adding mozilla service urls does not harm at all, could be changed
// evaluate certificate handling (oscp, crlite, blocklist)

missing from arkenfox in need of discussion:
security.pki.crlite_mode  ->  DISCUSS
security.remote_settings.crlite_filters.enabled  ->  DISCUSS
dom.security.https_only_mode_send_http_background_request  ->  DISCUSS
browser.download.useDownloadDir  ->  do we want to ask for download location each time?
```
