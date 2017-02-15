OpenProject reminder Plugin
==========================

This plugin adds functions to support project reminders to
[OpenProject](https://www.openproject.org). reminders
can be scheduled selecting invitees from the same project to take
part in the Reminder. An agenda can be created and sent to the invitees.
After the reminder, attendees can be selected and minutes can be
created based on the agenda. Finally, the minutes can be sent to
all attendees and invitees.

A more detailed feature tour can be found [here](https://www.openproject.org/projects/openproject/wiki/reminders).

Requirements
------------

The reminder plugin currently requires the [OpenProject Core](https://github.com/opf/openproject/) in
version greater or equal to 3.0.0.


Installation
------------

Add the following line to the `Gemfile.plugins` to your OpenProject installation (if you use a different OpenProject version than OpenProject 5, adapt `:branch => "stable/5"` to your OpenProject version):

`gem "openproject-reminder", :git => "https://github.com/kchizi/openproject-reminder.git", :branch => "stable/5"`

Afterwards, run:

`bundle install`

This plugin contains migrations. To migrate the database, run:

`rake db:migrate`

Deinstallation
--------------

Remove the line

`gem "openproject-reminder", :git => "https://github.com/kchizi/openproject-reminder.git", :branch => "stable/5"`

from the file `Gemfile.plugins` and run:

`bundle install`

Please not that this leaves plugin data in the database. Currently, we do not
support full uninstall of the plugin.

Bug Reporting
-------------

If you find any bugs, you can create a bug ticket at

https://www.openproject.org/projects/plugin-reminders

Development
-----------

To contribute, you can create pull request on the official repository at

`https://github.com/kchizi/openproject-reminder`

Credits
-------

Special thanks go to

* Deutsche Telekom AG (opensource@telekom.de) for project sponsorship
* Vincent Le Moign and his fabulous Minicons icons on [webalys.com](http://www.webalys.com/minicons/icons-free-pack.php)

License
-------

(c) 2011 - 2015 - OpenProject Foundation (OPF)

This plugin is licensed under the GNU GPL v3. See doc/COPYRIGHT.md and
doc/GPL.txt for details.
