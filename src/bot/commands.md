---
layout: bot
title:  "Commands"
date: 
categories: bot
---

##set &lt;name> = &lt;content>

####Add or update a factoid

(Admin only)

Flags:

* r: regexp: enables regexp mode; &lt;content> must be a sed-style (s///) substitution literal, conforming to Java regular expression syntax
* a: alias: alias mode; create an alias to an existing factoid: &lt;content> becomes a factoid name instead
* !: force: this flag must be set to overwrite an existing factoid; otherwise a warning will be issued

Notes:

* flags 'r' and 'a' are mutually exclusive

---

##del &lt;factoid-name>
###Delete a factoid

(Admin only)

Flags:

* !: force: enables deletion of factoids that have aliases leading to it; will also delete all aliases

---

##commands
###Display a list of special commands I support

Flags:

* v: verbose: also lists the description for each command

---

##info &lt;factoid-name>
###Display information about a factoid

---

##search &lt;text>
###Search the factoids store

Flags:

* o: original: only search 'original' factoids; that is, factoids that are not aliases
* a: aliases: only search factoid aliases
* n: names: only search factoid names
* c: content: only search factoid content

Notes:

* flags 'o' and 'a' are mutually exclusive
* flags 'n' and 'c' are mutually exclusive

---

##v [&lt;url>]
###Check a resource with the W3C markup and CSS validators.

Notes:

* If no URL is given, the last URL seen is checked

---

##g &lt;text>
###Perform a web search using Google.

---

##admins
###Display a list of my admins.

---

##short &lt;url>
###Turn a (long) URL into a short one using « goo.gl »

---

##caniuse &lt;text>
###Search caniuse.com's browser feature support data.

