# docs.projectatomic.io

This specification for the site is currently evolving.

## Goals

docs.projectatomic.io will either host or link to current documentation for all
of the projects under the ProjectAtomic umbrella.  For hosted documentation,
it will include automated builds of current documentation via continuous
integration.

## Project

The docs.projectatomic.io project will host the automation code for building
the docs site, and documentation on that code as well as policies around
the docs website.

Tracking of all docs tasks will happen via Github issue and pull request on that
project or other source project.

## Automation and Build

Docs will be automatically built and pushed to the public website based on
custom code to be developed.  This custom code is liable to involve some or
all of the following:

* Middleman
* Docker
* Jenkins
* Travis
* Github

Specific design is currently being worked out by members of the docs site team.

Each project is expected to author their own docs, either in their main
repository or in a separate docs repo for their specific project.  
docs.projectatomic.io only handles publication of the docs to the public site.

Using ReadTheDocs.org was considered, but did not meet our needs.

## Accepted Formats

docs.projectatomic.io will accept documentation in 2 formats:

* MarkDown
* ASCIIDoc

It is possible that we will also accept RestructuredText as well; that depends
partly on whether Middleman is required for the automation.

Additionally, all docs need to be under a single master directory (possibly with
one or more subdirectories) in your repository, one which contains only
documentation files.

## Design

Each project will have a directory under docs.projectatomic.io, named after that
project.  For example, Atomic Registry will be at
`http://docs.projectatomic.io/atomicregistry`. There will be one or more
additional "projects" which represent general documentation, such as our
getting started guide for Atomic Host.

The landing page at docs.projectatomic.io/ will have a "switchboard" consisting
of an icon and name for each project under the Atomic umbrella.  For projects with
externally hosted documentation (such as OpenShift Origin), the entry will link
to that documentation.

## Moving Old Docs

All documentation currently living at projectatomic.io/docs will eventually be
moved over to docs.projectatomic.io.  In order to avoid breaking links and losing
search rank, hand-produced .htaccess redirects will be added to redirect from
old pages to new ones.

## Licensing

Documentation which is under a separate license needs to be under [one of the
"good" documentation
licenses](https://fedoraproject.org/wiki/Licensing:Main?rd=Licensing#Documentation_Licenses)
as accepted by the Fedora project.  Documentation can also be under the upstream
project's main license.

## Team

The current docs.projectatomic.io team is:

* [Josh Berkus](https://github.com/orgs/projectatomic/people/jberkus)
* [Michael Scherer](https://github.com/orgs/projectatomic/people/mscherer)
* [Jonathan Lebon](https://github.com/orgs/projectatomic/people/jlebon)
* [Tuomas Kuosmanen](https://github.com/orgs/projectatomic/people/tigert)
* [Brian Exelbierd](https://github.com/orgs/projectatomic/people/bexelbie)
* [Joe Brockmeier](https://github.com/orgs/projectatomic/people/jzb)

If you want to help us build out the docs site, please contact a member of the
team to join in.
