fish_vcs_prompt - output vcs information for use in a prompt
============================================================

Description
-----------

The fish_vcs_prompt function can be used to display information about the current vcs repository, if any.

It calls out to vcs-specific functions. The currently supported ones are:

- fish_git_prompt
- fish_hg_prompt
- fish_svn_prompt

If a vcs isn't installed, the respective function does nothing.

For more information, see their documentation.

\subsection fish_vcs_prompt-example Example

A simple prompt that displays vcs info::

    function fish_prompt
        ...
        set -g __fish_git_prompt_showupstream auto
        printf '%s %s$' $PWD (fish_vcs_prompt)
    end
