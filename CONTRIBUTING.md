# Contributing to SEAPATH

First off, thanks for taking the time to contribute!

The following is a set of guidelines for contributing to the SEAPATH project. These are mostly guidelines, sometimes rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

#### Table Of Contents

[Code of Conduct](#code-of-conduct)

[License and Developer Certificate of Origin](#license-and-developer-certificate-of-origin)

[How Can I Contribute?](#how-can-i-contribute)
  * [Contributing Code](#contributing-code)
  * [Styleguides](#styleguides)
  * [Git workflow guidelines](#git-workflow-guidelines)
  * [Testing](#testing)
  * [Documentation](#documentation)
  * [English language convention](#english-language-convention)

[Project Governance](#project-governance)
  * [Project Owner](#project-owner)
  * [Technical Charter](#technical-charter)
  * [Committers](#committers)
  * [Technical Steering Committee](#technical-steering-committee)
  * [Contributors](#contributors)

## Code of Conduct

This project applies the [LF Energy Code of Conduct](https://wiki.lfenergy.org/display/HOME/Code+of+Conduct). By participating, you are expected to uphold this code. Please report unacceptable behavior to the project's Technical Steering Committee [SEAPATH-TSC@lists.lfenergy.org](mailto:SEAPATH-TSC@lists.lfenergy.org).

## License and Developer Certificate of Origin

By contributing to the SEAPATH project, you accept and agree to the following terms and conditions for your present and future contributions submitted to SEAPATH.

All contributions to this project are licensed under the license stipulated at the corresponding sub-repository. Except where otherwise explicitely indicated, SEAPATH is an open source project licensed under the [Apache License, version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

The project requires the use of the [Developer Certificate of Origin (DCO)](https://developercertificate.org/). The DCO is a legally binding statement asserting that you have the right to submit your contribution and to license it under the project's applicable license.

Contributors sign-off that they adhere to the term of the DCO by adding a ``Signed-off-by`` line to commit messages. The DCO sign-off must be attached to every contribution made by every contributor.

Here is an example ``Signed-off-by`` line, that indicates the contributor accepts the DCO:

````
This is my commit message.

Signed-off-by: Name Surname <name.surname@entity.com>
````
You can write it manually but Git even has a -s command line option to append this automatically to your commit message:
````
$ git commit -s -m 'This is my commit message'
````

Note that checks will be performed during the integration in order to require that commits in a Pull Request contain valid ``Signed-off-by`` lines.

## How Can I Contribute?

There are many ways to contribute:

- By participating in the TSC meeting passively and/or actively so that you can provide technical advice, understand what the project priorities are, and identify contributions you could make ( you can know when the next TSC meeting take place and eventually suscribe to the mailing list [here](https://lists.lfenergy.org/g/SEAPATH)
- By promoting the project
- By proposing new features or improvements/corrections to the project directly on [github.com](https://github.com/seapath) following the best practices detailed below

### Contributing code

The code of the project is available [here](https://github.com/seapath)

#### Styleguides

* Follow the code style of the project, including indentation

#### Git workflow guidelines

* Create a personal fork of the project on Github
* Clone the fork on your local machine
* Make sure to pull upstream changes into your local repository
* Implement/fix your feature, comment your code if needed
* Make sure to split your commit
* Squash intermediary commits (fixes, WIP, …) with git's interactive rebase
* Each commit should only add one feature
* Use two separate commits when adding a package and enabling it
* Make sure that your commit message is consistent with the git history
* Prefix the commit title by the area touch  ex: images/seapath-host-common.inc: add STONITH plugins
* Separate subject from body with a blank line
* Limit the subject line to 50 characters
* Use the imperative mood in the subject line
* Wrap the body at 72 characters
* Use the body to explain what and why vs. how
* Sign off your commit
* Push your branch to your fork on Github
* From your fork open a pull request

More details can be found [there](https://www.git-scm.com/book/en/v2/Distributed-Git-Contributing-to-a-Project#_commit_guidelines).

#### Testing

* Run tests on the hardware you want to install the distribution and ensure that no regression are seen (ex: cukinia)
* Provide the hardware specification
* Write or adapt tests as needed
* When possible a cukinia test must be provided for each new functionnality

#### Documentation

* Add or change the documentation as needed.

#### English language convention

The convention for all the project's documents, including code documentation, website, is to write American English.
A list of spelling differences between British and American English is available
[here](https://www.britishcouncilfoundation.id/en/english/articles/british-and-american-english) for example.
