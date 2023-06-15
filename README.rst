==========
 Timecard
==========

Timecard is a program to assist with tracking time in a csv.

Installation and usage
======================
Clone this repo somewhere on your computer and create a file called timecard.csv
in the same directory. Edit timecard.csv as shown in the next section, and
run the timecard program with the ``--help`` option to see usage instructions.

CSV Format
==========
The expected format for the entries is very simple. Each line has a date,
hourly range, and description like so.

::

    1993/05/06,16.5-24.0,"Waiting out a thunder storm with tornado."
    1993/05/07,00.0-06.5,"Tornado finishes."

Dates must be in Y/m/d format, times must match 24 hour clock, and the entry is
a string with no limit. The CSV must also not have a heading line.

If entries match this format, then timecard can calculate hours spent on
lines matching dates and patterns. Otherwise you'll get weird errors.

Gotchas
=======
Timecard doesn't validate entries. This means it's possible to double count
hours if entries overlap. Be accurate.

Maintenance
===========
Update the version in CHANGELOG.md and in the timecard script when cutting a
new release.
