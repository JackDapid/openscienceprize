# Research dissemination, 21st century style

Tim Head (Europe lead)

Titus Brown (US lead)

et al.

## Abstract:

## Introduction:

The open source/open science community is rapidly converging around a
set of technologies that will enable highly reproducible
computer-aided research publications.  These technologies include
environments to encode and encapsulate dependencies, cloud compute to
execute workflows, collaboration technologies that enable remixing,
and text formats that enable comparison and merging.

We believe that the time is right to explore the problem space in a
focused way and find points of general technical agreement as well as
map areas where further work is needed.  A vertical spike through the
problem space, with tools to go from an empty directory to a fully
rendered paper that can be re-rendered and executed, reviewed, and
remixed, will provide a technical basis for demos and extension.
Engagement with a broad community, open discussion, and community
brainstorming will build consensus about "solved" problems as well as
discovering the hard knots of disagreement.  Finally, open community
building around this problem will inevitably yield serendipitous
long-term interactions.

## Background:

In recent years, a robust set of technologies have emerged that are
being applied to the problem of reproducible computational
publications and narrative data analysis.  These include widely used
languages with a robust ecosystem of libraries ([R] and [Python]),
distributed version control systems that support collaboration,
remixing, and forking ([git] and [Mercurial]), platforms to host
collaboration around digital objects ([GitHub], [BitBucket], and [GitLab]),
isolated execution platforms (virtual machines, cloud computing, and
containers), configuration and dependency specification ([Debian],
[conda], [Docker]), "notebook" technologies ([Jupyter], [RMarkdown]), DOI
minting, and many others (XXX more here).

Even more recently, these technologies have been combined
by open science enthusiasists to deliver components that support
highly reproducible open science.  For example, [mybinder], [everware] and [tmpnb]
enable the execution of Jupyter notebooks in highly configurable
remote containers; (XXX more here)..

Despite these advances, there are still many missing components of a
system for executable papers.

First and foremost, we need a compute-independent specification
describing the paper repository layout and requirements, along with
outputs; such a specification would permit introspection of the
repository to support execution and composition on compatible
platforms.

Second, we need close integration with at least one or two widely used
cloud providers so that people can "bring their own compute".  Current
execution systems (mybinder, everware, tmpnb) are tied to particular providers,
have no immediate system for scaling to larger compute, and do not
integrate with any authentication systems. We also need to provide
simple methods for local development and execution on laptops,
workstations, HPCs, and private clouds.

Third, we need to expand support and gain experience with additional
literate data analysis ecosystems - namely, [R] and [RMarkdown]. The
technologies mentioned above natively support [Jupyter], which is not as
widely used in the biomedical research environment as RMarkdown.

Fourth, there is as yet no simple and opinionated way to get started
writing an executable paper.  This leaves new users who are
enthusiastic about the concept of highly reproducible publishing with
no good starting point, and blocks the creation of training materials.

Fifth, we lack ready integration with many useful services such as
continuous integration (to run executable papers on pull requests with
e.g. [TravisCI]), DOI minting (with e.g. [Zenodo]), and authorship
tracking ([ORCID]).

Sixth, the current "notebook" style of execution supported by both
Jupyter and RMarkdown limits resuability, remixability, and
composibility of code segments.  The rich Jupyter Notebook format
specification also presents challenges for longevity of research
artifacts. Before we "bake" notebooks into computational
reproducibility, we should think more deeply about how these issues
should be addressed. (refs)

Seventh, there are several (perhaps many) missing technical components
of the publishing stack.  For one example, we lack good tools for
notebook/workflow comparison and "diffing" to support review and
editorial processes.  For another, we lack tools to integrate with
publishing and repository submission workflows.

Eighth and finally, there are many communities interested in this
question, and little centrality or cohesion in the online space.  We
hope we can help nucleate a community that grows beyond the "that's
neat!" tech-demo experience to tackle the core technical and cultural
aspects of building reproducibility into our publishing ecosystem.

## The proposal:

We therefore propose to use the award money to execute a "vertical
spike" through the problem space, focused on tackling common
challenges and integrating existing tools, to demonstrate as complete
a pipeline as possible.  Products from this would include:

* a repository specification laying out the location of the dependency
  specification, input data, output data, output paper, and workflow
  execution details;

* a Web app allowing users to discover, interact and experiment with
  publications integrating the tools and methods advocated here. We
  include a mock up of the user-interface for this in the OSP submission;

* [Docker]-based execution instructions for non-cloud based development and
  execution of papers;

* expanded support for [RMarkdown] and other components of the [R] ecosystem;

* an opinionated "green field" repository creation Web app and
  associated command line tool;

* demo integration with [TravisCI], [Zenodo], and [ORCID].

In addition to these specific products, we would brainstorm, experiment,
and build concept demos around workflow composition, notebook longevity,
paper repository diffing and merging, and production of publication-ready
XML.

The technical implementation, concept demos, and brainstorming would
be supported by a community nucleated by this project, which we would
support with social media channels, in-person hackathons, blog posts,
and potentially publications.

### A mockup

![Executable paper UI mock up (animated version at http://bit.ly/osp_ui_mockup)](https://cloud.githubusercontent.com/assets/1448859/13301888/7217ff8a-db47-11e5-9c5a-51da4527821d.gif "Executable paper UI mock up (animated version at http://bit.ly/osp_ui_mockup)")

## Budget

The project will be run like an open-source project: anyone can join
and become a contributor to the software, documentation and
specifications we create. Building a community around these projects
is a focus. The prize will be used to cover out of pocket expenses to
achieve this goal:

* Travel and fees for team members to attend workshops, sprints, and
  community events to build contacts and recruit new contributors.

* Organising hackathons to engage with the community and
  build consensus on the specification and use-cases.

Cloud services for a live demonstrator. We will avoid buying physical
objects as it is not clear what should happen with them at the end of
the project.

TH will commit a significant amount of his time (60-80% FTE) to this
project in the next six months. A large part of the budget will go
towards paying for his time.

## Openness first

The proponents (and contributors to this [everpub proposal]) will form the first
members of a community we will build around this proposal.

The [R³ proposal] was written in
the open on GitHub. A total of 16 people chose to subscribe to the
repository and be informed about all activity, twelve people decided
to show their support by starring the repository, and N people
actively contributed to the creation of this proposal. No financial
incentives were offered for participation.

This project will build on top of an existing ecosystem of open-source
tools. We will contribute to existing open-source projects under their
license. All newly created material and projects will be licensed
under [BSD3] for code and [CC BY 4.0] for other material.

## Related efforts

Several efforts exist to create interactive and reusable scientific
articles. A non exhaustive list: [gitxiv], [Open Science Framework],
[Galaxy], [OpenML], [IPOL], and [Exec and share companion sites]. To
our knowledge, none provides what we propose. They either lack
executability or generality, create lock in, require additional human
effort after publication, or focus on workflow management.

## Who we are and why that matters

e.g. Active Papers and Konrad Hinsen.

invite SWC folk?

## Expressions of interest

We contacted the following journals and received an expression of interest
in seeing a working prototype implementing the ideas of this proposal:

<https://github.com/betatim/openscienceprize/issues/22#issuecomment-189144172> (place holder)

* [Giga] - Laurie Goodman
* [F1000] - Michael Markie
* [Research Ideas and outcomes] - Lyubomir Penev
* [ReScience] - Konrad Hinsen and Nicolas P. Rougier


## Summary

## Additional information

### Short term user story

The use of executable papers provides a benefit to researchers from
day one. Each of their projects exists in a separate, customisable
environment. They can not interact with each other. No outsiders can
modify the environment. This prevents the "This worked four weeks ago
and I changed nothing!" scenario, enables rapid sharing with
colleagues, and dramatically reduces the time and effort until new
team members can make contributions to a project. It increases
reproducibility and

### Long term user story

Code is to data analysis what maths is to the laws of nature, the most
precise description. Only the publication of code and environment
together allows post hoc analysis for flawed methodology or whether a
result was affected by a certain bug in a computer program used.

## Resource feasibility

The proponents are researchers in data intensive fields. They have
vast technical experience with the individual components required to
construct a working prototype. They have a track record of
contributing to open-source projects and growing communities around
projects. One of the proponents ([CTB]) is experienced in teaching
highly technical tools to novices via his involvedment with Software
Carpentry. One of the proponents ([TH]) has built a
[demonstrator](http://everware.xyz) that allows people to jump right
in to other's research code.

## Conclusion

Reproducibility is a main principle of the scientific method. We
propose to make reproducibility a first-class citizen in computer
aided research by enabling the publication of dynamic and interactive
scientific narratives that can be verified, altered, reused, and
cited from a web browser. This new interactive reusability will increase the
transparency, quality and educational value of published scientific
work.

There is a large interest in a project like this in the scientific and
open-source communities as demonstrated by the interest in the
preparation of this proposal and the expressions of interest from
publishers.

Concretely we propose to: build a web application for the publication
of dynamic and interactive scientific narratives, create tools and
educational material to accelerate the adoption of existing solutions
for reusable science, and finally to build a community around these
ideas.

This will be amazing!


[everpub proposal]: https://github.com/betatim/openscienceprize
[RMarkdown]: http://rmarkdown.rstudio.com
[R]:         https://www.r-project.org
[Python]:    https://www.python.org
[git]:       https://git-scm.com
[Mercurial]: https://www.mercurial-scm.org
[GitHub]:    https://www.github.com
[BitBucket]: https://bitbucket.org
[GitLab]:    https://gitlab.com/
[Debian]:    https://www.debian.org/
[Conda]:     https://www.continuum.io/why-anaconda
[Docker]:    https://www.docker.com
[Jupyter]:   http://jupyter.org
[TravisCI]:  https://travis-ci.org
[Zenodo]:    https://zenodo.org
[ORCID]:     http://orcid.org
[mybinder]:  http://mybinder.org
[tmpnb]:     https://tmpnb.org
[everware]:  http://everware.xyz
[gitxiv]:    http://gitxiv.com/
[Galaxy]:    https://galaxyproject.org/
[OpenML]:    http://www.openml.org/
[IPOL]:      http://www.ipol.im/
[BSD3]:      http://choosealicense.com/licenses/bsd-3-clause/
[CC BY 4.0]: http://creativecommons.org/licenses/by/4.0/
[Open Science Framework]: https://osf.io
[Exec and share companion sites]: http://www.execandshare.org/CompanionSite/
[Giga]: http://gigascience.biomedcentral.com/
[F1000]: http://F1000.com
[Research Ideas and outcomes]: http://riojournal.com/
[ReScience]: https://rescience.github.io
[CTB]: https://github.com/ctb
[TH]:  https://github.com/betatim