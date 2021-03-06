---
layout: default
title: Administrators Command
permalink: /xf8bot/commands/administration/level_4/administrators/
---

# Administrators Command

## Info

The `administrators` command allows you to set the permissions of different roles in your server. 
This command uses a level system which correlates to certain permissions - as seen below.

**This is a level four command.**

---

## Permission Levels

* Level 4 Perms - Level Four allows you to preform all the commands for level three and below,
  alongside `administrators`, and `prefix`. 
  This is intended for admin/owner roles!
* Level 3 Perms - Level Three allows you to perform all the commands for level two and below, 
  alongside `ban` and `unban`.
* Level 2 Perms - Level Two allows you to perform all the commands for level one, alongside `kick` and `clear`.
* Level 1 Perms - Level One allows you to perform the commands `warn`, `removewarn`, `warns`, `mute` and `nickname`.
* Level 0 Perms - Level Zero allows you use to all the commands that do not require permissions, 
  such as `info` or `ping`.

---

## Functions & Usage

* NOTE: All flags will begin with a `-` if using the short name, and `--` if using the long name.
* NOTE: Required Parameters = <> and Optional Parameters = []

`addRole` - adds a role to the list of administrators.

* Usage: `{prefix}administators addRole -r <role mention/rolename/roleid> -l <1/2/3/4>`
* Flags: role - `--role` & `-r` , level - `-l` & `--level`
* Aliases: `add`, `addRole`

`removeRole` - removes a role from the list of administrators.

* Usage: `{prefix}administrators removeRole -r <role mention/rolename/roleId>`
* Flags: role - `--role` & `-r`
* Aliases `remove`, `removeRole`, `rm`

`getRoles` - gets the roles from the list of administrators.

* Usage: `{prefix}administrators getRoles`
* Flags: none
* Aliases: `ls`, `list`, `listroles`, `get`, `getroles`

---

## Aliases

* `admins`

---

### **Author: AG6**

<b> <a rel="cc:attributionURL" property="dct:title" href="https://xf8b.github.io/documentation/xf8bot/">xf8bot Documentation</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/xf8b/">xf8b</a> is licensed under <a rel="license" href="https://creativecommons.org/licenses/by-sa/4.0">CC BY-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" /><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" /><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" /></a> </b> 