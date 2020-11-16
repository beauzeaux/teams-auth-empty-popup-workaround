# Teams Interstitial auth fix

This is a quick fix for the intermediate blank popup that shows during auth flows. 

This works by first loading a website controlled by the developer into a task module that then triggers the auth flow
via an sdk call `microsoftTeams.tasks.submitTask`

The relevant changes can be found in TeamsAppManifest/manifest.json (note the command w/o parameters and a task info url) and in the `authStart` page inside wwwroot