DIFFWINDOW_MOVEMENT
===============================================================================
_by Ingo Karkat_

DESCRIPTION
------------------------------------------------------------------------------

This plugin provides movement commands and text objects for windows in diff
mode.

USAGE
------------------------------------------------------------------------------

    ]C                      Go to [count] next end of a change.
    [C                      Go to [count] previous end of a change.
                            These complement the built-in ]c [c commands.

    ic                      "inner change" text object; in a diff window, select
                            [count] changes.
    id                      "inner difference" text object; difference is more
                            fine-granular than diff changes; in a diff window,
                            select a range of lines that have the same
                            DiffAdd/DiffChange/DiffDelete highlighting.

INSTALLATION
------------------------------------------------------------------------------

The code is hosted in a Git repo at
    https://github.com/inkarkat/vim-diffwindow_movement
You can use your favorite plugin manager, or "git clone" into a directory used
for Vim packages. Releases are on the "stable" branch, the latest unstable
development snapshot on "master".

This script is also packaged as a vimball. If you have the "gunzip"
decompressor in your PATH, simply edit the \*.vmb.gz package in Vim; otherwise,
decompress the archive first, e.g. using WinZip. Inside Vim, install by
sourcing the vimball or via the :UseVimball command.

    vim diffwindow_movement*.vmb.gz
    :so %

To uninstall, use the :RmVimball command.

### DEPENDENCIES

- Requires Vim 7.0 or higher.
- Requires the CountJump plugin ([vimscript #3130](http://www.vim.org/scripts/script.php?script_id=3130)), version 1.90 or higher.

CONFIGURATION
------------------------------------------------------------------------------

For a permanent configuration, put the following commands into your vimrc:

To change the default motion mapping, use:

    let g:diffwindow_movement_EndMapping = 'C'

To also change the [ / ] prefix to something else, follow the instructions for
CountJump-remap-motions.

To change the default text object mappings, use:

    let g:diffwindow_movement_ChangeTextObject = 'c'
    let g:diffwindow_movement_DifferenceTextObject = 'd'

To also change the i prefix to something else, follow the instructions for
CountJump-remap-text-objects.

CONTRIBUTING
------------------------------------------------------------------------------

Report any bugs, send patches, or suggest features via the issue tracker at
https://github.com/inkarkat/vim-diffwindow_movement/issues or email (address
below).

HISTORY
------------------------------------------------------------------------------

##### 1.03    14-Nov-2024
- CountJump 1.9 renames g:CountJump\_Context to g:CountJump\_TextObjectContext.

__You need to update to CountJump.vim ([vimscript #3130](http://www.vim.org/scripts/script.php?script_id=3130)) version 1.90!__

##### 1.02    22-Jul-2014
- Allow to reconfigure the mappings for the motion and text objects. Thanks to
  Enno Nagel for suggesting this.

##### 1.01    02-Mar-2012
- FIX: Vim 7.0/1 need preloading of functions referenced in Funcrefs.

##### 1.00    30-Aug-2011
- First published version.

------------------------------------------------------------------------------
Copyright: (C) 2011-2024 Ingo Karkat -
The [VIM LICENSE](http://vimdoc.sourceforge.net/htmldoc/uganda.html#license) applies to this plugin.

Maintainer:     Ingo Karkat &lt;ingo@karkat.de&gt;
