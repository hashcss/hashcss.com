---
title: "Using #CSS"
layout: plain
---

<a name="help"></a>
# Using #CSS Effectively

In addition to [the #CSS rules](/rules), here are some tips which will
make it easier to get help.

<a name="live"></a>
## Live URLs

Please provide a live URL of the problem site. Screenshots are difficult
to debug. Only providing the CSS for a site doesn't help us see the
problem: CSS does not work without HTML.

<a name="paste"></a>
## Pastebins

For our purposes, [JSFiddle](http://jsfiddle.net) is the site most
people use.

* [JSFiddle](http://jsfiddle.net)
* [Codepen](http://codepen.io)
* [Tinkerbin](http://tinkerbin.heroku.com)
* [JSBin](http://jsbin.com)
* [Selvvir's Pastebin](http://paste.asmcbain.net)
* [Webdevout](http://webdevout.net)

<a name="testcase"></a>
## Test Cases

A test case is the minimal amount of HTML, CSS, and JavaScript needed to
reproduce your problem. By making it easy to see exactly what and where
the problem is, the people in the channel will be more inclined to help.

In the course of making the test case, you may even figure out the
solution to your problem yourself!

## Pitfalls

Avoid these behaviors to make your time in the channel go smoothly:

### Don't be a Help Vampire

[Help Vampires](http://slash7.com/2006/12/22/vampires/) are people who
wholly rely on the knowledge of others to do their work. Instead of
trying to learn, the help vampire asks for an example, and copies the
result into their own code.

What distinguishes the help vampire is:

* Asking the same question multiple times, despite getting answers
    * Instead of asking the same question, if you do not understand the
      answers, ask followup questions for clarification
* Appearing to lack initiative
    * Tell us about everything you tried before you joined the channel.
      This will also help us to help you.
    * Before asking for clarification on a term, try asking Google
    * Don't be afraid to try things while asking for help. Tell us what
      you tried and what happened!
* Being rude and demanding
    * The people in the channel are volunteers. Rude behavior is against
      [the #CSS rules](/rules).

<a name="bot"></a>
# Bots

Selvvir is an IRC bot for the #css channel on freenode. It replaces the
previous bot, rivvles, created by Colin Aarts (aka riven or lilmonkey on
freenode) which the author still provides but chose to remove from #css.

Originally, Selvvir started as an attempt to reverse engineer rivvles
(for no real reason). Shortly after its inception, the source code
powering rivvles was made available on github as irc-js-bot. rivvles is
presumably a custom configured irc-js-bot.

Selvvir is not exactly the cleanest code, and as such is closed-source.
If you want Selvvir-like functionality, see the irc-js-bot project
github repository and run that instead. irc-js-bot does not offer the
caniuse.com functionality of Selvvir, but it is not hard to add.

Why neon green? rivvles' favorite color was hotpink. Ask Selvvir about
`hotpink.

## Commands

Commands are prefixed with the \` (backtick) character to indicate to
Selvvir it is being addressed: \``somefactoid`

Anything not recognized as an explicit command is assumed to be a
factoid. Factoids can have spaces.

The `@` character can be used to address a command's response or factoid
output to another user: \``caniuse flex @ username`

However, all errors are reported back as notices to the original
requestor and not the addressed user. Commands with longer output also
send it as a notice, so as not to spam the channel.

Some commands have flags to modify their response. Those can be placed
after the command name: \``caniuse/p flex`

Not all commands offer flags, and more than one flag can be used
together in any order: \``caniuse/np flex`

Flags a command does not recognize will be ignored.

In addition to the flags below, each command has a flag causing it to
list out information about it and its flags instead of returning its
normal response. This page is built with the same information listed
there.\``caniuse/?`

###set &lt;name> = &lt;content>

####Add or update a factoid

(Admin only)

Flags:

* r: regexp: enables regexp mode; &lt;content> must be a sed-style (s///) substitution literal, conforming to Java regular expression syntax
* a: alias: alias mode; create an alias to an existing factoid: &lt;content> becomes a factoid name instead
* !: force: this flag must be set to overwrite an existing factoid; otherwise a warning will be issued

Notes:

* flags 'r' and 'a' are mutually exclusive

---

###del &lt;factoid-name>
####Delete a factoid

(Admin only)

Flags:

* !: force: enables deletion of factoids that have aliases leading to it; will also delete all aliases

---

###commands
####Display a list of special commands I support

Flags:

* v: verbose: also lists the description for each command

---

###info &lt;factoid-name>
####Display information about a factoid

---

###search &lt;text>
####Search the factoids store

Flags:

* o: original: only search 'original' factoids; that is, factoids that are not aliases
* a: aliases: only search factoid aliases
* n: names: only search factoid names
* c: content: only search factoid content

Notes:

* flags 'o' and 'a' are mutually exclusive
* flags 'n' and 'c' are mutually exclusive

---

###v [&lt;url>]
####Check a resource with the W3C markup and CSS validators.

Notes:

* If no URL is given, the last URL seen is checked

---

###g &lt;text>
####Perform a web search using Google.

---

###admins
####Display a list of my admins.

---

###short &lt;url>
####Turn a (long) URL into a short one using « goo.gl »

---

###caniuse &lt;text>
####Search caniuse.com's browser feature support data.

---

## Admins

Current admins are:

* AMcBain (owner/hoster)
* drej
* oksushi
* preaction
* GarethAdams
* doc|mobile
* reisio
* Munter
