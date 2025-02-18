---
title: MISP 2.4.110 released (aka local-tags and new MISP modules supporting MISP standard format)
date: 2019-07-08
layout: post
banner: /img/blog/modules-expand.gif
---

# MISP 2.4.110 released

A new version of MISP ([2.4.110](https://github.com/MISP/MISP/tree/v2.4.110)) has been released with a host of new features, improvements, many bugs fixed and one security fix. Even under the searing summer sun, the MISP-project team is hard at work, whilst enjoying some cocktails (with or without booze).

# New main features

## MISP modules extended to support the full MISP standard format

[misp-modules](https://github.com/MISP/misp-modules) now support MISP objects and relationships. The revamped system is still compatible with the old modules, whilst the new modules bolster up the complete MISP standard format. New modules such as [url-haus](https://github.com/MISP/misp-modules/blob/52dadd2df32b19241fdd978e50b717f1967e264b/misp_modules/modules/expansion/urlhaus.py), [joe sandbox query](https://github.com/MISP/misp-modules/blob/be61613da4f5dc8f082a7c1a9e1ec07fdb872560/misp_modules/modules/expansion/joesandbox_query.py) and many others support the new MISP standard format. This new feature allows module developers to create more advanced modules, generating MISP objects and associated relationships from any type of expansion, import or export modules in one click.

![](/img/blog/misp-modules-new.png)
![](/img/blog/misp-modules-2.png)

## Local tags introduced

![](/img/blog/local-tags.png)

The long awaited feature "local tags" is now finally available. You can create tags locally if you are a member of the given MISP instance's host organisation, enabling "in-place" tagging for synchronisation and export filtering. MISP events are not modified while using the local tags and are in turn always stripped before being synchronised with other MISP instances and sharing communities. Local tags allow users to avoid violating the ownership model of MISP, but still be able to tag any event or attribute for further dissemination and data contextualisation. Local tagging works for tags, tag collections, galaxies and matrix-like galaxies such as ATT&CK.


## New Norwegian translation

Thanks to the contribution from [Kortho](https://github.com/Kortho), the MISP user-interface now includes a Norwegian translation in addition to the previously contributed Japanese, French translations along with multiple work in progress translation efforts getting closer to full coverage, such as Russian, German and Chinese. If you wish to contribute, feel free to join the [crowdin page for MISP](https://crowdin.com/project/misp). It's simple and efficient, translations can be easily done via the web interface.

# Various updates and improvements

- [Following SANS courses feedback](https://twitter.com/speshulted/status/1141711388617904128), physics can be enabled/disabled on demand.
- [UI] Filter has been added in the template object index.
- [API] On-demand inclusion of attribute relations via the event view endpoint. Thanks to Siemens for the ideas and feedback.
- [security] Made certain settings modifiable via the CLI only. Some settings are too risky to be exposed, even to site admins, so made them CLI accessible only.
- [API] New option to excludeLocalTags to events/restSearch.
- [UI] Many improvements in the event view regarding related events. In case of multiple correlations, the related events are now in a scrollable box.
- [Doc] Installation guides and scripts were improved.
- [Bug] Fix an old hard-coded path for the temp directory.
- [API] Simple worker management added.

# Security fix (CVE-2019-12868)

[CVE-2019-12868](https://cve.circl.lu/cve/CVE-2019-12868) has been fixed in MISP 2.4.110. MISP 2.4.109 had remote command execution by a super administrator because the PHP file_exists function is used with user-controlled entries, and phar:// URLs trigger deserialisation. This vulnerability can only be triggered by the site admin. Thanks to Dawid Czarnecki for reporting it.

# STIX improvements

- Parsing observable compositions from external STIX files.
- Fixing issues with 'parse' being called on bundles containing custom objects.
- Fixed user account pattern and user account observable extension in STIX 2.0 export.
- Fixed socket extension parsing.
- Fixed registry-key keys and values parsing for patterns.

[MISP galaxy](/galaxy.html), [MISP object templates](/objects.html) and [MISP warning-lists](https://github.com/MISP/misp-warninglists/) have been updated to the latest version.

We would like to thank all the contributors, reporters and users who have helped us in the past months to improve MISP and information sharing at large.

As always, a detailed and [complete changelog is available](/Changelog.txt) with all the fixes, changes and improvements.

