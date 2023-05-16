# Matomo (formerly Piwik)
- Set the Site ID
- Choose whether you want image fallback tracking
- Enter the URL to your Matomo install excluding http/https and trailing slashes
- Choose whether you want to track admins (not recommended)
- Choose whether you want to send Clean URLs (recommended): Matomo will aggregate Page Titles and show a nice waterfall cascade of all sites, 
- Set alternative piwik.js URL for any purpose
including categories and action types
- Optional tracking for User ID
- User ID could be id or username
- Set the API url
- Set the API token

If both the API url and API token are set in the form and the siteid is empty when the form is submitted, an attempt to register the site with the API will be made.


# Auto-provisioning
- Set the global config settings 'apitoken' and 'apiurl' to enable auto provisioning. These can also be set in config.php e.g: 
   - `$CFG->forced_plugin_settings['watool_matomo']['apiurl'] = 'https://matomo.org';`
   - `$CFG->forced_plugin_settings['watool_matomo']['apitoken'] = 'xxxx';`
- Auto provisioning attempts are made if the current site url has changed since any of the instances were stored.
- If autoprovisioning failed, the instance will be set with the name 'auto-provisioned:FAILED'. Delete the instance to attempt an autoprovision again.
