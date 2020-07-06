**********
Governance
**********

.. Based on https://github.com/ThreeSixtyGiving/standard/blob/master/documentation/governance.md for an example.

As the Global Coffee Data Standard develops over time, with updated versions and new publishers, it is important that a diverse group of stakeholders are engaged in the process.
This document outlines the governance and revision processes for the Global Coffee Data Standard.

======================
Version 1.0 and Beyond
======================
The Global Coffee Data Standard was initially developed through an iterative process in 2017 & 2018, resulting in an initial draft version in November 2018.

During 2019, we have been working towards a first version of the standard, version 1.0.
Our work has focused on addressing some issues identified through wider adoption of the Standard during 2019 and 2020.

This document outlines a process for managing changes to the Global Coffee Data Standard during the move from a draft version to an officially agreed version, which will be numbered 1.0.

Currently the following new projects from the ISEAL Innovation Fund are upcoming:

#. The Delta Project with BCI, GCP, partnering with the International Coffee Organisation (ICO) and the International Cotton Advisory Committee (ICAC) to develop common cross-commodity sustainability indicators.

It is expected that the further development, adoption and elaboration of the data standard becomes an integral part of these projects.

==========================
Stewardship and Governance
==========================
Global Coffee Platform (GCP) acts as the lead steward of the Global Coffee Data Standard.
The organisation is led by an Executive Director. The organisation’s activities are overseen by a Board of Directors.

In the pursuit of openness and community-driven process, subscribers to the Global Coffee Data Standard and those engaging with the Global Coffee Data Standard GitHub repository will be kept informed at all stages about planned revisions to the Global Coffee Data Standard, and will be offered clear and timely opportunities to input and comment.

To ensure the relevance, quality and effective implementation of proposed updates to the Standard, new version releases will be subjected to a process of peer review with
invited reviewers from publisher and user communities, and an open review process.

A Standard Stewardship Committee, responsible for giving final approval to formal upgrades of the Standard and ensuring the processes in this document have been properly carried out will be set up in due course.

Intellectual property
---------------------
The Global Coffee Data Standard is the joint intellectual property of GCP and ISEAL.

.. raw:: html

   <a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a> The Global Coffee Data Standard is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.



Contributors to the Global Coffee Data Standard agree to transfer any copyright in their contributions to GCP and COSA, in order that it is held in trust as part of the Standard.
No content infringing upon third-party Intellectual Property Rights will be included in the Standard.

Governance principles
---------------------
We are committed to the `Open Standard principles <https://open-stand.org/about-us/principles/>`_ for standards development. The Global Coffee Data Standard has been developed with:

* **Due process**: Decisions will be made with equity and fairness among participants. Through an open process for submitting issues, extensions and requests for updates, no one party will dominate or guide standard development. All processes will be transparent and opportunities will exist to appeal decisions. Processes for periodic standards review and updating are well defined in this document.

* **Broad consensus**: The process will allow for all views to be considered and addressed, such that agreement can be found across a range of interests.

* **Transparency**: We will provide advance public notice of proposed standards development activities, the scope of work to be undertaken and conditions for participation. Easily accessible records of decisions and the materials used in reaching those decisions will be provided. Public comment periods will be provided before final standards approval and adoption.

* **Balance**: Standard activities will not be exclusively dominated by any particular person, company or interest group.

* **Openness**: The Global Coffee Data Standard processes are open to all interested and informed parties.

==============================
Versioning and Upgrade Process
==============================
Over time, changes will be needed to the Standard, including addition of new codes and fields, and occasionally involving changes to existing fields and structures.

The revision process will ensure:

* The consequences of any change for different stakeholders are identified and considered; It is clear why changes are needed, and that there is broad support for any proposed changes;

* Changes are easy to identify and are transparent, and publishers, users and intermediaries have clear documentation to allow them to update their data and tools;

* Changes to the Global Coffee Data Standard should be made periodically, with the version number of the standard incremented to indicate that changes have been made, and a change-log maintained.

* That backwards compatibility will be maintained wherever possible.

Versions
--------
**Distinct branches** of the Standard will be maintained within Github for each version. Branches can be in one of two states:

* Development. Both schema and documentation on a development branch can be updated and should only be implemented on an experimental basis.

* Master. Only documentation updates are permitted on a master branch. All documentation changes must be reviewed to ensure they do not make any changes to the meaning of the Standard.

**Semantic Versioning** practices will be used to distinguish between:

* Major versions which make backwards-incompatible API changes; and

* Minor versions which add functionality in a backwards-compatible manner.

These are captured by a version number in the format MAJOR.MINOR

Revision process
----------------
To release a new minor or major version upgrade will involve a number of stages outlined in the flowchart below, and described in more depth in the following sections.

.. image:: _static/images/upgrade_process_march_2019.png
   :alt: Revision process

.. Can/will we adopt the above revision process?

The revision process will follow these general principles:

* **Publicity**: All stages of the revision process will be announced via the GCP website. This is the formal channel for notification during the process.

* **Consensus**: The process should act in the interest of the data standard, with particular consideration given to what the changes will mean for current publishers. All processes should aim towards gaining community consensus for changes. In cases where consensus cannot be reached, the process will be put to a final majority vote by the Stewardship Committee. The GCP technical team are responsible for generating key documentation during the process, but should always be guided by community consensus, submitting all decisions for public discussion.

* **Appeal**: Any party may appeal against decisions made during the process by writing to the Standard Stewardship Committee via the GCP discussion forum. The Stewardship Committee has the authority to reject proposed revisions on the Standard in response to appeals

Proposals
---------
Changes to the Standard can be proposed by anyone at any point via the GCP discussion forum either as issues for discussion, or `pull requests <https://help.github.com/articles/about-pull-requests/>`_ with a clear description of the proposed change.
Contributors are encouraged to raise discussions in order to seek consensus on proposed changes.
Changes may be proposed as updated field definitions or code list entries, or as new features to the Standard.

==============
Prioritisation
==============
The technical team, with reference to community views, identify change proposals and extensions which should be considered for adoption in the next version of the Standard, assigning these to milestones in the issue tracker on GitHub where they are open for discussion.

Periodically, at the start of a revision process a cut-off date for proposals will be announced with at least two weeks’ notice. After that date, a prioritised list of updates is produced. Any new proposed changes received after this period may not be considered until the next prioritisation phase.

Prioritisation review
---------------------
The list is shared on the GCP website, with at least a two-week window for discussion.

Based on discussions, a final list is then proposed by the technical team with all the issues that will be taken forward into the rest of the process. A proposal that has made it this far may or may not make it into the final upgrade. As the proposal is worked into final concrete examples and schema changes, further issues may arise that mean the original proposal cannot be implemented.


All reviews and the judgement made will be published. Community members may also submit their own reviews of the whole revision, or specific elements. The minimum period for Committee review is one month.

Revisions
---------
The GCP technical team, with reference to the Standard Stewardship Committee as appropriate, should evaluate reviews and decide whether the whole upgrade, or specific features of it, need to be revised, rejected or postponed to future processes.

If only minor changes are suggested, then the revised Standard can be submitted back to reviewers for a brief review period of at least two weeks. If major changes are required, then a longer follow up review process of at least one month should be allowed for.

Release
-------
Once all reviewer comments have been addressed to the satisfaction of the reviewer in question, then the updated version of the Standard should be submitted to the Standard Stewardship Committee for final approval, along with a short report of the process.

Following Stewardship Committee approval, the revision branch can be set to live.

==================
Deprecation Policy
==================
If a term (an indicator or property) is scheduled to be renamed or removed from the specification as a result of the revision process, the next release of the specification must deprecate the term within the schema, and the following major release must rename or remove the term from the schema, making the term obsolete. Implementations may use deprecated terms, but will receive warnings from the GCP Data Quality tool described below. Implementations may not use obsolete terms, and will receive errors from the Data Quality tool.

==============
Support Policy
==============
Support will be offered for one prior version of the Standard. Support for any earlier versions than this will be ended when a new version is released. For example, when 1.1 is the latest release, 1.0 will be supported in the Data Quality tool and other relevant tools and platforms managed by GCP. When 1.2 is released, support for 1.0 will no longer be guaranteed.

Publishers are encouraged to review each new version when released, and to consider how they might adopt new features. Publishers should aim to move to a new major version within 18 months of its release.

.. Should we add a privacy page like http://standard.threesixtygiving.org/en/latest/privacy-notice/
