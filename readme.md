# CSP Reporter

This is my csp reporter script based on the script provided there https://mathiasbynens.be/notes/csp-reports

## Configuration

### Setup the script

- Download & copy this script to the webroot
- Edit the script and configure the `$recipients` and `$subject` variables
- Add to your CSP rule: `report-uri /csp-reporter.php?source=example.org` (please replace example.org with your domain)

### How the blacklist works

The backlist allows you to block reports from beeing send to you.

Basicly now this is a per domain and per directive blacklist.

Here is a example:

```
'style-src' => [
	'adblockers.opera-mini.net',
],
```

This configuration would block all emails where our csp reporter get a hit because of opera's addblocker injecting style files into your site.

## Joomla Integration

If you need a Joomla Integration for CSP and other HTTP Headers you can take a look into my plugin: [plg_system_httpheader](https://github.com/zero-24/plg_system_httpheader). As of Joomla 4.0 this plugin is shipped with the core distribution as drop in replacement: [Pull Request #18301](https://github.com/joomla/joomla-cms/pull/18301)

