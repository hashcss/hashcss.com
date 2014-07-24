---
layout: bot
title:  "How to use the bot"
date: 
categories: bot
---

Commands are prefixed with the \` (backtick) character to indicate to Selvvir it is being addressed: \``somefactoid`

Anything not recognized as an explicit command is assumed to be a factoid. Factoids can have spaces.

The `@` character can be used to address a command's response or factoid output to another user: \``caniuse flex @ username`

However, all errors are reported back as notices to the original requestor and not the addressed user. Commands with longer output also send it as a notice, so as not to spam the channel.

Some commands have flags to modify their response. Those can be placed after the command name: \``caniuse/p flex`

Not all commands offer flags, and more than one flag can be used together in any order: \``caniuse/np flex`

Flags a command does not recognize will be ignored.

In addition to the flags below, each command has a flag causing it to list out information about it and its flags instead of returning its normal response. This page is built with the same information listed there.\``caniuse/?`