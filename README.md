# RedHat Mobile Application Cordova Plugin for iOS9 TLS1.2 check

This plugin is a patch for iOS9 TLS1.2 check. It adds following value sets to Info.plist:

```xml
<dict>
  <key>NSAllowsArbitraryLoads</key>
  <false/>
  <key>NSExceptionDomains</key>
  <dict>
    <key>feedhenry.net</key>
    <dict>
      <key>NSExceptionAllowsInsecureHTTPLoads</key>
      <true/>
      <key>NSIncludesSubdomains</key>
      <true/>
      <key>NSExceptionMinimumTLSVersion</key>
      <string>TLSv1.0</string>
      <key>NSExceptionRequiresForwardSecrecy</key>
      <false/>
    </dict>
    <key>feedhenry.com</key>
    <dict>
      <key>NSExceptionAllowsInsecureHTTPLoads</key>
      <true/>
      <key>NSIncludesSubdomains</key>
      <true/>
      <key>NSExceptionMinimumTLSVersion</key>
      <string>TLSv1.0</string>
      <key>NSExceptionRequiresForwardSecrecy</key>
      <false/>
    </dict>
  </dict>
</dict>
```

This will allow app to access RHMAP without turning off all TLS checks on other domains.
