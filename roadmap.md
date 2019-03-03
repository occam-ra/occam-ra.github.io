---
title: OCCAM Project Roadmap
layout: default
---
## OCCAM Project Roadmap
====================

### How should I use this document?

This document provides description of items that the project decided to prioritize. This should
serve as a reference point for OCCAM contributors to understand where the project is going, and
help determine if a contribution could be conflicting with some longer term plans.

The fact that a feature isn't listed here doesn't mean that a patch for it will automatically be
refused! We are always happy to receive patches for new cool features we haven't thought about,
or didn't judge to be a priority. Please however understand that such patches might take longer
for us to review.

### How can I help?

See the [issues page](https://github.com/occam-ra/occam/issues) at the main repo. Though we are still developing the roadmap and deciding on project priorities, any help is appreciated, even at this early phase. The issues page will give you a quick view of what is actively being worked on. Please comment on issues if you want to work on it to avoid duplicating effort! Similarly, if a maintainer is already assigned on an issue you'd like to participate in, pinging him on GitHub to offer your help is the best way to go.

### How can I add something to the roadmap?

The roadmap process is new to the OCCAM Project: we are only beginning to structure and document the
project objectives. Our immediate goal is to be more transparent, and work with our community to
focus our efforts on fewer prioritized topics.

We hope to offer in the near future a process allowing anyone to propose a topic to the roadmap, but
we are not quite there yet. For the time being, it is best to discuss with the maintainers on an
issue, or at the [OCCAM slack project](http://occam-dev.slack.com)

## 1. Structural upgrade

OCCAM is entering a new development phase after some dormancy. Perhaps the highest big-picture priority is a structural upgrade which decouples core functionality from interfaces, and rebalances the python and c++ layers. See the [OCCAM structure](https://occam.readthedocs.io/en/latest/occam-structure.html) documentation for a discussion of the issues involved (those docs are under active development).

### 1.1 Developing the python layer (capstone project)

Most of the RA functionality is currently implemented in the c++ classes. There are python bindings, and a utility class (ocUtils), and some high-level RA workflow is implemented in Python using objects returned by the interfaces exposed by the bindings. But most of the action is still happening in c++ (even including, for example, directly outputting HTML). We want to rebalance this so that only the core functionality remains in the c++, and the python layer provides well-developed, modular functionality that a python package can be built around.

We are fortunate to have a PSU capstone project team on board to help with this part of the development. That team is still getting oriented, and we are working on documentation to provide them a little bit of guidance for their project. They are responsible for the details, but we are responsible for providing them some high-level recommendations about the desired new OCCAM application structure. Their changes will go a long way towards the desired upgrade, but that structural redesign will involve further development beyond the capstone project.

## 1.2 Internal decoupling

We want to separate the core RA functionality from I/O and other interfaces. Currently a lot of stuff is mixed together in the c++ - we want to take out the non-essential parts and move those into python to boost programmer productivity, flexibility, and accessibility. We are currently working on organizing this process, alongside planning for the capstone project (which is obviously very closely related).

## 2. Documentation

We are actively working on developing documentation. The user manual has been converted to markdown and posted at the [https://occam.readthedocs.io](occam.readthedocs.io). The planned structural upgrades require some planning material, which is currently being developed. At this phase (through end of winter term 2019 - end of March), documentation development is in some ways more important than code development. It is important to organize our development efforts, which will quickly be ramping up and getting more complex as new developers come on board.

There are many documents that would be useful. Further developing this roadmap is helpful. More programming-related documents (particularly focusing on the python layer and bindings) are needed, and are in early development. See the [issues page](https://github.com/occam-ra/occam/issues) issues page for the current work.

Check back for changes to this roadmap. We will be updating it regularly as development efforts intensify.
