mediathek-cli
======

CLI mod of the popular Mediathek3 client - ALPHA 0.2.0a

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
- Run mediathek-cli -u to update all databases, configuration files will be automatically generated
- Run mediathek-cli -d to download all subscribed shows
- Put mediathek-cli -sudq in your crontab to download all new information and all new shows automatically
- Run mediathek-cli without arguments or with -g to display the subscription dialog
- Actions can be combined - e. g. mediathek-cli -sug updates all show lists, then opens subscription dialog
- For more see mediathek-cli --help

======

HISTORY

0.2.0a
- fixed bugs with diff'ing
- handling corruped files better now
- added hard rate limiting
- added notifications for OSX and Growl
- using .local/share for state files in Linux now
- added ability to disable download continuation
- made ask dialog graphical
- implemented patch natively - platform-independent, yay!
- minor visual changes, bugfixes, additions

0.1.0a
- First upload to github

======

TODO

- Notifications are horribly experimental on Windows and OSX, never tested
- Graphical configuration dialog
- Ability to export settings
- Change the way "seen" is stored... who cares if we need 10 MByte of storage
- Change minimum duration from GUI
- State file location in Windows and OSX?
- Make whole program usable from GUI?
- Fix horrible update logic

======

BUGS

- Strange bug when counting filtered ListView lines... hacked around it, still
- When no new day list is downloaded by server yet, station-yesterday is the file from the day _before_ yesterday, not from yesterday. Screws up md5summing, of course, plus thorws local state back.

