# VeteranSudoku Privacy Policy

## App update feed

`app-update.json` is served by GitHub Pages beside the privacy policy. Both
platforms initially have `enabled: false` and `storeAvailable: false`.
This schema supersedes the earlier `update-policy.json` feed.

Prepare Optional / Required / No change through the shared gbeta workflow.
The choice/minimum is logged in the app project's app-update.pending.json;
successful uploads record each platform's actual version/build. Beta uploads
never modify or publish this hosted policy.

After a release is publicly available in the correct store, update only that
platform here: copy its successful pending version to latestVersion, copy mode
and minimumSupportedVersion, append the public version to publishedReleases
(oldest first, unique), refresh expiresAt (UTC), and enable enabled/storeAvailable.
Commit and push only after verifying rollout/storefront/OS availability.
Android's configured URL uses the project's actual package; public listing
availability must be checked before activation.

Optional is dismissible; more than two published releases behind gives a stronger
reminder. Required mode or an installed version below minimumSupportedVersion
blocks play. Expired/unavailable/invalid policies fail open. Disable enabled to
stop notices. Keep the app project's reference app-update.json synchronized.
