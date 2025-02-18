---
title: MISP 2.4.78 released
date: 2017-08-06
layout: post
banner: /img/blog/misp-small.png
---

A new version of MISP [2.4.78](https://github.com/MISP/MISP/tree/v2.4.77) has been released including an important security fix (if you use sharing groups), multiple bug fixes and some new functionalities.

A security fix in in the attribute lookup in the UI to correctly adhere to the sharing group restrictions. Thanks to Helge Aksdal for pointing this out. 

MISP roles can now be managed via the API. Role functions such as add, delete, index, list and set_default are now accessible via the API. The current HEAD of PyMISP includes the roles support.

Multiple bugs in the UI and API were fixed in this release.

A new attribute type 'cookie' has been added. A more complex [MISP object cookie](https://github.com/MISP/misp-objects/blob/master/objects/cookie/definition.json) is now available in the templates and will be accessible in the next release which will include the MISP objects. For the curious, the branch `objects_wip` is the current development activities to support the MISP objects. This also a last-call for the contributors who need some additional objects (before a first release is done) to review the [current MISP object templates](https://github.com/MISP/misp-objects).

Various improvements have been made to make lookups, export and API lookups of attribute level data.

MISP taxonomies, galaxies and PyMISP updated to the latest version.

The full change log is available [here](https://www.misp.software/Changelog.txt).

Don't hesitate to [open an issue](https://github.com/MISP/MISP/issues) if you have any feedback, found a bug or want to propose new features.

Don't forget our [MISP summit 0x3](https://2017.hack.lu/misp-summit/) before the [hack.lu](https://2017.hack.lu/) 2017 conference which will take place from 14:00 to 18:00, Monday 16 October 2017. The core team of MISP will also join the [hack.lu open source security software hackathon 0x2 ](https://hackathon.hack.lu/) which will take place the 19-20 October 2017.

A new MISP training will take place in Luxembourg the 21st November 2017, [registration is now open](https://www.eventbrite.com/e/misp-training-november-edition-tickets-36347289722).
