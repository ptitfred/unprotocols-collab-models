Language
========

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT",
"RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described
in [RFC 2119][1].

Goals
=====

PC3 is meant to provide a reusable optimal collaboration model for open source software
projects. It has these specific goals:

*	To maximize the scale of the community around a project, by reducing the friction for
  new Contributors and creating a scaled participation model with strong positive feedbacks;

*	To relieve dependencies on key individuals by separating different skill sets so that
  there is a larger pool of competence in any required domain;

*	To allow the project to develop faster and more accurately, by increasing the diversity
  of the decision making process;

*	To support the natural life-cycle of project versions from experimental through to stable,
  by allowing safe experimentation, rapid failure, and isolation of stable code;

*	To reduce the internal complexity of project repositories, thus making it easier for
  Contributors to participate and reducing the scope for error;

*	To enforce collective ownership of the project, which increases economic incentive to
  Contributors and reduces the risk of hijack by hostile entities.


Design
======

Preliminaries
-------------

*	The project SHALL use the git distributed revision control system.
*	The project SHALL be hosted on github.com or equivalent, herein called the "Platform".
*	The project SHALL use the Platform issue tracker.
*	The project SHOULD have clearly documented guidelines for code style.
*	A "Contributor" is a person who wishes to provide a patch, being a set of commits
  that solve some clearly identified problem.
*	A "Maintainer" is a person who merge patches to the project. Maintainers are not
  developers; their job is to enforce process.
*	Contributors SHALL NOT have commit access to the repository unless they are also
  Maintainers.
*	Maintainers SHALL have commit access to the repository.
*	Everyone, without distinction or discrimination, SHALL have an equal right to become
  a Contributor under the terms of this contract.

Licensing and Ownership
-----------------------

*	The project SHALL use the GPLv3 or a variant thereof (LGPL, AGPL).
*	All contributions to the project source code ("patches") SHALL use the same license
  as the project.
*	All patches are owned by their authors. There SHALL NOT be any copyright assignment
  process.
*	The project SHALL be owned collectively by all its Contributors.
*	Each Contributor SHALL be responsible for identifying themselves in the project
  Contributor list.

Patch Requirements
------------------

*	Maintainers and Contributors MUST have a Platform account and SHOULD use their real
  names or a well-known alias.
*	A patch SHOULD be a minimal and accurate answer to exactly one identified and agreed
  problem.
*	A patch MUST adhere to the code style guidelines of the project if these are defined.
*	A patch MUST adhere to the "Evolution of Public Contracts" guidelines defined below.
*	A patch SHALL NOT include non-trivial code from other projects unless the Contributor
  is the original author of that code.
*	A patch MUST compile cleanly on at least the most important target Platforms.
*	A "Correct Patch" is one that satisfies the above requirements.

Development Process
-------------------

*	Change on the project SHALL be governed by the pattern of accurately identifying
  problems and applying minimal, accurate solutions to these problems.
*	To initiate changes, a user SHALL log an issue on the project Platform issue tracker.
*	The user SHOULD write the issue by describing the problem they face or observe.
*	The user SHOULD seek consensus on the accuracy of their observation, and the value
  of solving the problem.
*	Users SHALL NOT log feature requests, ideas, suggestions, or any solutions to problems
  that are not explicitly documented and provable.
*	Thus, the release history of the project SHALL be a list of meaningful issues logged
  and solved.
*	To work on an issue, a Contributor SHALL fork the project repository and then work
  on their forked repository.
*	To submit a patch, a Contributor SHALL create a Platform pull request back to the
  project.
*	A Contributor SHALL NOT commit changes directly to the project.
*	To discuss a patch, people MAY comment on the Platform pull request, on the commit,
  or elsewhere.
*	To accept or reject a patch, a Maintainer SHALL use the Platform interface to merge
  the patch.
*	Maintainers SHALL NOT accept their own patches.
*	Maintainers SHALL NOT make value judgments on correct patches.
*	Maintainers SHALL merge correct patches rapidly.
*	Maintainers SHOULD ask for improvements to incorrect patches and SHOULD reject incorrect
  patches if the Contributor does not respond constructively.
*	Any Contributor who has value judgments on a correct patch SHOULD express these via
  their own patches.
*	Maintainers MAY commit changes to non-source documentation directly to the project.

Creating Stable Releases
------------------------

*	The project SHALL have one branch ("master") that always holds the latest in-progress
  version and SHOULD always build.
*	The project SHALL NOT use topic branches for any reason. Personal forks MAY use topic
  branches.
*	To make a stable release someone SHALL fork the repository by copying it and thus become
  maintainer of this repository.
*	Forking a project for stabilization MAY be done unilaterally and without agreement of
  project maintainers.
*	Maintainers of the stabilization project SHALL maintain it through pull requests which
  MAY cherry-pick patches from the forked project.
*	A patch to a repository declared "stable" SHALL be accompanied by a reproducible test case.
*	A stabilization repository SHOULD progress through these phases: "unstable", "candidate",
  "stable", and then "legacy". That is, the default behavior of stabilization repositories
  is to die.

Evolution of Public Contracts
-----------------------------

*	All Public Contracts (APIs or protocols) SHOULD be documented.
*	All Public Contracts SHALL use [Semantic Versioning][4].
*	All Public Contracts SHOULD have space for extensibility and experimentation.
*	A patch that modifies a Public Contract SHOULD not break existing applications
  unless there is prior consensus on the value of doing this.
*	A patch that introduces new features to a Public Contract SHOULD do so using new names.
*	Old names SHOULD be deprecated in a systematic fashion by marking new names as "experimental"
  until they are stable, then marking the old names as "deprecated".
*	When sufficient time has passed, old deprecated names SHOULD be marked "legacy" and eventually removed.
*	Old names SHALL NOT be reused by new features.
*	When old names are removed, their implementations MUST provoke an exception (assertion) if used by applications.

References
==========

Bibliography
------------

[1]: "Key words for use in RFCs to Indicate Requirement Levels" - ietf.org

[2]: "Definition of a Free and Open Standard" - digistan.org

[3]: "Consensus Oriented Specification System" - digistan.org

[4]: "Semantic Versioning 2.0.0-rc.1" - semver.org

[1]: ietf.org "Key words for use in RFCs to Indicate Requirement Levels"
[2]: digistan.org "Definition of a Free and Open Standard"
[3]: digistan.org "Consensus Oriented Specification System"
[4]: semver.org "Semantic Versioning 2.0.0-rc.1"


