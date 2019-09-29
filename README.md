random-sublime-text-plugin
==========================

Plugin for sublime text to generate random, ints, floats, strings and words.

It works in Sublime Text 2 *and* ST3

Example
=======

![Example](example.gif)


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
   wait few seconds until the installation finishes up
1. Go to the menu **`Tools -> Command Palette...
   (Ctrl+Shift+P)`**
1. Type **`Preferences:
   Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   add the following setting to your **`Package Control.sublime-settings`** file, if it is not already there
   ```js
   [
       ...
       "channels":
       [
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
           "https://packagecontrol.io/channel_v3.json",
       ],
       ...
   ]
   ```
   * Note,
     the **`https://raw...`** line must to be added before the **`https://packagecontrol...`**,
     otherwise you will not install this forked version of the package,
     but the original available on the Package Control default channel **`https://packagecontrol...`**
1. Now,
   go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
search for **`RandomEverything`** and press <kbd>Enter</kbd>

See also:
1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


Usage
=====

This plugin can only be accessed through the <kbd>Cmd</kbd>/<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> command.

Type *random* and you get the following choices:

* Random:Int - requires a range from a-b separated with a: *-*. Default: 1-100
* Random:Float - requires a range from a-b separated with a: *-*. Default: 1-100
* Random:Letters - generatates a random string of lower and upper -case letters with a length between 3 and 17
* Random:Letters and numbers - generatates a random string of lower and upper -case letters and numbers with a length between 3 and 17
* Random:Country - picks a random country
* Random:Word - picks a random word from /usr/share/dict/words
* Random:Text - picks 24 random words from /usr/share/dict/words
* Random:Date - picks a random ISO-8601 Date
* Random:First name - picks a random first name from the built-in datafile
* Random:Last name - picks a random last name from the built-in datafile
* Random:Full name - picks a random full name from the built-in datafiles
* Random:E-mail - picks a random E-mail address
* Random:Url - generates a URL using random words from /usr/share/dict/words
* Random:Hex Color - generates a random hex color formatted "#abc123"
* Random:IPv4 Address - generates a random ipv4 ip address
* Random:IPV6 Address - generates a random ivp6 ip address

Overridable Settings
====================

#Random: E-Mail
* random_email_top_level_domain_override - Allows overriding available email TLDs e.g. `["com","org"]`. Defaults are `["com", "net", "co.uk", "org", "edu"]`
* random_email_main_domain_override - Allows overriding of available email main domains e.g. `["gmail","yahoo", "hotmail"]`. If not specified, a random string will be used.

* `max_year` and `min_year` defines a date range

# Complete Settings Example

    {
        "random_email_top_level_domain_override": ["com", "net", "co.uk", "org", "edu"],
        "max_year": 2000,
        "min_year": 1999
    }

