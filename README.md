# B3 micronomy

A middleware and alternative web GUI to access Maconomy. It is mainly
intended as a programming exercise but is actually somewhat easier to
work with than the main Maconomy GUI.

# Usage

## Connecting

Point you browser at https://micronomy.jonaseel.se/ and log in with
your B3 Maconomy credentials.

To run it locally you can either install Rakudo and the required
modules or make sure you have a working Docker installation and build
and run the Dockerfile. You might want to change the port number from
443 to be able to run docker without sudo. The browser will complain
about the fake certificate in use when running locally but that's
expected.

Technically there's nothing stopping you from connecting the micronomy
service to some other Maconomy backend but only the B3 Maconomy has
been tested.

## Hours

Time is expected to be filled in as decimal hours; eg. "an hour and a
half" should be entered as `1.5`. The sums shown beneath the time
records are read from the API; no time calculations are done in
Micronomy.

## Weeks

To directly switch to a specific week you can add `?date=YYYY-MM-DD`
in the browsers address field. Note that weeks on month borders will
be divided into `A` and `B` as in Maconomy.

## Projects

Adding or removing the projects shown currently has to be done in
Maconomy. Note though, that you can specify in Maconomy that the same
records should be shown on consecutive weeks too.

## Keyboard shortcuts

Hitting enter while entering times is equivalent to pressing the
"Spara" button; ie. it saves the entered times into the database. To
switch to next or previous week you can press the appropriate buttons
or `Ctrl-Right` or `Ctrl-Left` respectively. The arrow keys can be
used to navigate between the time fields. Hitting `Escape` will
unfocus any time field and `Ctrl-Down` will re-focus the same field.

## Submitting

When a week is completely filled in, it should be submitted by
pressing the "Avlämna" button. As in Maconomy, there's nothing
stopping you from re-submitting an already submitted week but if you
change an already billed week, the changes will probably be ignored by
the billing system. So don't do that without consulting with you
manager first.

# Contributing

If you find any bugs or even want to fix one you can go to
https://github.com/krakan/micronomy/issues/. If the bug you've found
isn't there already, please report a new issue. To contribute code
you'll have to fork the code to you own Github account and commit your
code there and then make a pull request against the main repository.

You're also welcome to add some of the missing features already
reported as issues. Follow the same procedure as for bugs.
