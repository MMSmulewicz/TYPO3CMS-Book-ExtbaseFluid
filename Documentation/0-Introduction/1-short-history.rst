.. include:: ../Includes.txt

A short history of Extbase and Fluid
====================================

.. ============================================
.. Meta-Information for this chapter
.. ---------------------------------
.. Author: Sebastian Kurfürst
.. Updated for 1.0 beta1: YES, by Sebastian Kurfürst
.. ============================================



After the implementation of NEOS (formerly TYPO3 v5) and FLOW (formerly FLOW3)
as the basis framework started, the development of TYPO3 v4 and NEOS was happening
almost completely independent from each other. In October 2008, the core developers
of both branches met for the *TYPO3 Transition Days* in
Berlin. There, the developers wanted to work on a common vision and strategy
for the transition from TYPO3 version 4 to the coming version 5.
The core points of this strategy were communicated as a manifesto (see the
box "The Berlin Manifesto").

.. sidebar:: The Berlin Manifesto

   We, the participants of the TYPO3 Transition Days 2008 state that
   …

   * TYPO3 v4 continues to be actively developed
   * v4 development will continue after the release of v5
   * Future releases of v4 will see its features converge with those in TYPO3 v5
   * TYPO3 v5 will be the successor of TYPO3 v4
   * Migration of content from TYPO3 v4 to TYPO3 v5 will be easily possible
   * TYPO3 v5 will introduce many new concepts and ideas. Learning
     never stops and we'll help with adequate resources to ensure a smooth
     transition.

   Signed by:

   *Patrick Broens, Karsten Dambekalns, Dmitry Dulepov,
   Andreas Förthner, Oliver Hader, Martin Herr, Christian Jul Jensen,
   Thorsten Kahler, Steffen Kamper, Christian Kuhn, Sebastian Kurfürst,
   Martin Kutschker, Robert Lemke, Tobias Liebig, Benjamin Mack, Peter
   Niederlag, Jochen Rau, Ingo Renner, Ingmar Schlecht, Jeff Segars, Michael
   Stucki, Bastian Waidelich*

With the background of this manifesto, the decision was made to
re-implement two parts of TYPO3 v4:

* A modern successor for the base class
  :php:`tslib_piBase`, on which by now the majority of the
  3600 extensions for TYPO3 builds on. From there, Extbase emerged.
* A new template engine for outputting data, which connects
  flexibility, ease of use and extensibility: Fluid.

Discussions about the new template engine started already on the
Transition Days, where Bastian Waidelich and Sebastian Kurfürst discussed
how such a new template engine should work and behave. Shortly after, a
prototype was implemented. The development of Extbase began two months
later, when a few core members met in Karlsruhe. There, they agreed on
staying as close as possible to the concepts, the architecture and the APIs
of FLOW.

After that followed an intensive development phase, where Jochen Rau
developed the biggest part of Extbase, while Sebastian Kurfürst did code
reviews and gave feedback. Additionally, Fluid has reached the beta stage in
that time.

The first public presentation of Extbase happened in March 2009 at the
*T3BOARD09* in Laax (CH). With stormy weather, 2228 m
over sea level, core developers and interested people could see the current
state of Extbase. In a stimulating discussion, the last open topics like naming conventions and the name
of the framework, were decided upon. Additionally, the decision was made to
include Fluid in version 4.3, instead in version 4.4 as planned
before.

In the following days, the Fluid team developed a small program (named
*Backporter*) which could take the code of Fluid for
FLOW, and transform it to code for TYPO3 v4. That's how the first working
version of Fluid for TYPO3 v4 came into being at the end of the T3BOARD09.
Additionally, it was now pretty easy to keep Fluid for FLOW in sync with
Fluid for TYPO3 v4.

The first real presentation of Extbase and Fluid happened in April
2009 on the american *TYPO3 Conference* in Dallas, and a
month later on the *TYPO3 Developer Days* in Elmshorn
near Hamburg. After that, a lot of positive feedback and constructive
criticism emerged from the community.

During the next months, a lot of work was done to clean up the
details: The syntax of Fluid was improved, ViewHelpers were written, and the
persistence layer of Extbase was improved and refactored multiple times.
Functionalities for the security of the framework were implemented, the MVC
framework was cleaned up, and more functionalities were implemented which
were needed for practical usage.

At the *T3CON09* in autumn 2009, Extbase and Fluid
could be presented as a beta version. Afterwards, only errors were
corrected, but no new functionalities were implemented. With the release of
TYPO3 4.3.0 in November 2009, Extbase and Fluid were included in the TYPO3
core and are thus available in every TYPO3 installation.

After a well-deserved break for the development team after the release,
work started again with smaller bugfixes and a roadmap for upcoming
functionalities. That's how many details of the framework were improved, and
the persistence layer was once again streamlined and cleaned up.
