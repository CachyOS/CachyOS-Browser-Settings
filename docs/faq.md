

# How do I make LibreWolf remember all the cookies?

In your librewolf.overrides.cfg, add the following:

    // cookies: No longer forget any website data..
    pref("network.cookie.cookieBehavior",        1);
    pref("privacy.sanitize.sanitizeOnShutdown",  false);
    pref("privacy.clearOnShutdown.cookies",      false);
    pref("privacy.clearOnShutdown.cache",        false);
    pref("privacy.clearOnShutdown.downloads",    false);
    pref("privacy.clearOnShutdown.history",      false);
    pref("privacy.clearOnShutdown.formData",     false);
    pref("privacy.clearOnShutdown.offlineApps",  false);
    pref("privacy.clearOnShutdown.sessions",     false);
    pref("privacy.clearOnShutdown.siteSettings", false);






