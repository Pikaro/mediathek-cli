mediathek-cli
======

CLI mod of the popular Mediathek3 client - ALPHA

mediathek-cli is capable of subscribing to videos from Mediathek and Arte+7 from the command line, without making a GUI necessary for regular updates.

The main focus is bandwidth-efficient cron compatibility; through the use of diffs, only a few kilobyte a day are necessary for transfers. This allows the user to stay up to date with their favorite shows without putting unnecessary strain on the database servers.

Special thanks go to Xaver W., the author of the original mediathek3 client. The databases are derived from his ones and simply reformatted to fit the smaller needs of an application focused on subscriptions.

Licensed under GPLv2, so have at it! Or mail me under git at d-reis.com. Criticism welcome, I know I'm using some ugly hacks.

Should you accidentally stumble over this project, be aware that it is very much Alpha software and not intended for release. There are still numerous bus and feature holes to be corrected

David Reis, Mar 2014

======

USAGE

- Put mediathek-cli in your path
- Run mediathek-cli -s to update the list of available shows
- Run mediathek-clu -g to display the subscription dialog
- Run mediathek-cli -u to update all databases, configuration files will be automatically generated
- Run mediathek-cli -d to download all subscribed shows
- Put mediathek-cli -sudq in your crontab to download all new information and all new shows automatically

======

TODO

- Stabilize diff system FIRST
- See source for aftwerwards

=====

BUGS

- Too fucking many

