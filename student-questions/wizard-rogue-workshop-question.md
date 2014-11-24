> Hi Donal!

Hi Wizard Rogue!

> How do you modify the config and add an alias?

`git config --global alias.<alias_name> "<alias_command>"`

Please note that you don't put the `git` command in the `<alias_command>`
section above.

Then you can see that the alias has been added by examining the config
variables:

`git config -l`
