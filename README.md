# PROJECT *PWB_SAMPLES*

This project is a collection of scripts that demonstrate
the usefulness of the Bash builtin commands [pwb][git_pwb] and
[ate][git_ate], and how quickly these tools can help one develop
useful command line applications that solve unique problems.

Secondarily, these scripts are here because they solve my
particular problems.  I have made sym-links in `/usr/bin` to many of
these scripts so because I use them frequently.

## BRIEF DESCRIPTIONS

Most of the scripts are works-in-progress, but I'll try to give
some hints as the purpose and/or strategy of each of the scripts.

### SIMPLE SCRIPTS

These scripts are suitable for learning more about techniques of
using **pwb** and **ate**.

#### pwb_template

This is a minimal implementation of using **pwb** and **ate** in
a script.  This might be a good place to start seeing how they
work in an application.

#### ps_scan

Another minimalist implementation showing the output of `ps` in
a **pwb** script

#### pwb_gh

Using **github**'s `gh` API, show a list of all repositories in your
Github account, with a description in the header.  This was a test
case for developing methods for showing line information in another
pane.  In this case, the page head displays the date and description
of the repository.

#### pwb_git_log

The main display shows commit events.  The header shows several details
about the commit

#### COLOR SCRIPTS

I edit my LS_COLORS variable to make some colors more visible against
the black console screen in which I usually work.  These tools aspire
to make that easier

#### pwb_dircolors

Named after the `dircolors` command because it shows the same
information as that command.  This script shows every LS_COLOR value
with an example 'swatch' of color.  What distinguishes this is that
if you press ENTER, you can edit the color.  The color editor is
really lame, but I reverted to this simple-minded implementation after
speding entirely too much time trying to design a color editor that
could handle all the methods of describing color on a console.

This is the first script that uses my messaging and dialog tools.

#### pwb_showrgb

Just shows the output of `showrgb` in a **pwb** display.


### DIRECTORY SCRIPTS

I'm not really excited about any of the available TUI directory
browsers I've found.  These scripts are chances to roll-my-own with
launching document viewers for various file types like markdown and
groff (man) files.  I don't need copy or move, so these common
features are missing from my file browsers.

#### pwb_ls

This is my first effort.  It works for opening a browser to view a
markdown file, but fails for man files.  A point of interest with
this script is how it helped me get recursion in Bash working, which
involved learning better Bash practices, and some Builtin coding
practices to make sure any generated variables are created in the
current scope.

#### ate_ls

This is a re-thinking of pwb_ls, with a thorough collecting and
cataloging of mime and file type information (using **ate** to apply
to all the files in a given directory.  This is a work-in-progress
which I set aside temporarily to develop some messaging and
dialog utilities.

### APT SCRIPTS

I sometimes want to know if I've installed some utility, or I may
have forgotten the exact spelling.  These apt scripts are little
experiments in collecting and displaying information about installed
packages.

#### apt_log_scan

Shows a list of apt operations.  Clicking ENTER on one shows details
about the operation, like a list of dependent downloads

#### apt_scan

Shows a list of all installed packages with the included
description.  Pressing ENTER has no effect.

#### apt_scanner

Early effort of little value.  Keeping around because I can't be
bothered to see if it contains anything of value.




[git_ate]:    https://www.github.com/cjungmann/pwb.git
[git_pwb]:    https://www.github.com/cjungmann/pwb.git
