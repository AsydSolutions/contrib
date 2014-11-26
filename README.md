ASYD / contrib
=============

This repository is for 3rd party and contributed stuff for ASYD, like generic deploys or monitor files. You can contribute to the repository by issuing pull-requests with your own creations.

**deploys/**

On the deploys/ directory you can find user-contributed deploys for generic services/software. Inside this directory you will find directories named as the deploy (i.e. "deploys/LAMP/") containing the definitions and configuration of those deploys.

For installing a deploy in your local ASYD installation just move that directory to your data/deploys/ folder (i.e. deploys/LAMP/ on this repository to data/deploys/LAMP/ in your ASYD server).

When creating a deploy please read carefully the documentation and follow the guidelines. Remember to create conditional blocks if your deploys are meant for concrete systems (i.e. only for Debian or only for Solaris, etc), and describe what your deploy does as comments at the start of the "def" file. Also remember to add alerts (#alert: ...) if you deploy requires certain user variable to be set, or if you want to acknowledge the users about something before launching the deploy.

**monitors/**

On the monitors/ directory you will find Monit rules for different services. This are simple files named as the service to be monitored, including the Monit rules for it. They also take variables and conditionals as for any other configuration file.

For installing a monitor in your local ASYD installation just move that file to your dara/monitors/ folder (i.e. monitors/ssh on this repository to data/monitors/ssh in your ASYD server).

When creating a monitor please read carefully the documentation and also shortly describe what's for in a comment. As for the deploys, use conditional blocks if certain monitor file is only meant for certain systems.

Licenses
--------

All the code here is licensed with the same terms as ASYD itself (GPLv3), unless specified otherwise inside a file. In all cases the code shall have an OSI-compatible license. Asking for a pull-request implies that you agree with this fact.
