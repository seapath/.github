# SEAPATH - (S)oftware (E)nabled (A)utomation (P)latform and (A)rtifacts (TH)erein

[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/5398/badge)](https://bestpractices.coreinfrastructure.org/projects/5398)

[![CI Yocto Weekly](https://github.com/seapath/ansible/actions/workflows/ci-yocto-weekly.yml/badge.svg)](https://github.com/seapath/ansible/actions/workflows/ci-yocto-weekly.yml)
[![CI Debian Weekly](https://github.com/seapath/ansible/actions/workflows/ci-debian-weekly.yml/badge.svg)](https://github.com/seapath/ansible/actions/workflows/ci-debian-weekly.yml)

[![SonarCloud on VM Manager](https://sonarcloud.io/api/project_badges/measure?project=seapath_vm_manager&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=seapath_vm_manager)
[![SonarCloud on python3-setup-ovs](https://sonarcloud.io/api/project_badges/measure?project=seapath_python3-setup-ovs&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=seapath_python3-setup-ovs)


[![ShellCheck on build_debian_iso](https://github.com/seapath/build_debian_iso/actions/workflows/shellcheck-weekly.yml/badge.svg)](https://github.com/seapath/build_debian_iso/actions/workflows/shellcheck-weekly.yml)

## The project

LF Energy SEAPATH is an open source software hypervisor designed for IEC61850 Digital Substation Automation Systems. It has been designed and built as an industrial-grade solution dedicated to the critical context of digital stations, meeting the challenges of interoperability, standards compliance and [cybersecurity constraints](https://lfenergy.org/lf-energy-seapath-project-completes-security-audit-and-threat-model/).

SEAPATH aims to host and run VPAC (Virtualized Protection, Automation and Control) applications for the power grid industry (and potentially beyond).

SEAPATH is a best-of-breed technology that combines open source components to create a robust, hardware- and software-agnostic solution that meets deterministic expectations (Real-Time) of its use-cases. The project has been developed according to OpenSSF best practices, and utilizes state-of-the-art continuous integration with over 700 daily tests to ensure, for example, that a VIED meets the desired criteria in terms of latency, determinism, and robustness.

SEAPATH is a collaborative project, bringing together a diverse community of experts spanning embedded Linux, IT, electrical engineering backgrounds, fostering IT/OT convergence.

SEAPATH is an acronym for Software Enabled Automation Platform and Artifacts (Therein). It is under the governance of the LF Energy and part of the LF Energy Digital Substations Special Interest Group.

## Features

SEAPATH currently or will include the following features:

- **Ecosystem agnostic**, easily used and extended by third parties
  - Hardware agnostic: can be installed on different types of servers and architectures (x86, ARM, etc.)
  - Vendor agnostic: a heterogeneous variety of virtual machines can be deployed and managed on the platform.
  - Open source: released under a permissive open source license (Apache-2.0), enabling effortless adoption, customization, integration into existing projects, and commercialization opportunities for users.
  - On-going integration with other LF Energy Projects from Digital Substations Automation Systems (DSAS) such as LF Energy CoMPAS, LF Energy FledgePOWER, and OpenSCD.

- **High performance**, ready for IEC 61850 applications
  - Real-time capabilities: can host applications with determinism and performance needs.
  - Time synchronization: natively support NTP and PTP (IEEE 1588) synchronizations.

- **Resilience**, robust for mission-critical systems
  - High availability and clustering: offers cluster functionalities to guarantee availability in case of hardware or software failures.
  - Distributed storage: data and disk images of the virtual machines are replicated and synchronized to guarantee its integrity and availability on the cluster.
  - Automatic updates: The system can be automatically updated from a remote server.

- **Infrastructure as code**, allowing automated and remote system management
  - Configuration: initial configuration is done using scripted tasks, ensuring exact replication of desired operations and avoiding manual errors.
  - Administration: can be easily managed from a remote machine connected to the network as well as by an administrator on site.

- **Intensive testing**, guaranteeing capabilities and avoiding regression
  - Continuous integration: Every development on the platform must pass more than 700 unit tests, real time tests and latency tests.
  - Testing-driven cybersecurity approach: each requirement is ensured through extensive unit tests.

## Background

Due to the Energy Transition the use of power transmission and distribution grids is changing. The control architecture of
power grids needs to be swiftly adapted to take account of infeed at lower grid levels, higher dynamics in flow patterns and
more distributed controls (both internal controls and grid flexibility services from third parties).

In this context TSOs and DSOs require a new generation of Digital Substation Automation Systems (DSAS) providing more
dynamic protection settings and adaptive automation functions. Moreover, data management gets significant, both for the
remote administration of deployed automation and protection functions, as well as for the communication with central or
local systems and processes. Thus the design of the new DSAS will have to allow for a drastically higher level of modularity,
interoperability and scalability compared to the previous generations.

Virtualization is seen as a key innovation in order to fulfill these needs.

## Start with SEAPAPTH

SEAPATH comes with two main distributions, Yocto or Debian. You can find a comparison of both versions on the wiki [SEAPATH-Debian or SEAPATH-Yocto](https://lf-energy.atlassian.net/wiki/x/7I7lAQ)

Once you have chosen your SEAPATH distribution, you can build your iso file
- [yocto_bsp](https://github.com/seapath/yocto-bsp) for Yocto
- [build_debian_iso](https://github.com/seapath/build_debian_iso) for Debian

Then, you have to configure your machines with the [ansible](https://github.com/seapath/ansible) repository.
Both distributions are configured using the main branch.

More information on the [SEAPATH wiki](https://lf-energy.atlassian.net/wiki/x/C4DlAQ)

## Discussion

You can connect with the community in a variety of ways...

- [LINK TO MAILING LIST](https://lists.lfenergy.org/g/SEAPATH-TSC)
- [SEAPATH channel on LF Energy Slack](https://lfenergy.slack.com/archives/C01EH8ZLJTC)

## Contributing

Interested in contributing? Please read carefully the [CONTRIBUTING guidelines](/CONTRIBUTING.md).

## Security

For any security related questions or submissions, please review the [security policies](https://github.com/seapath/.github/blob/main/SECURITY.md).

## Governance

SEAPATH is a project hosted by the [LF Energy Foundation](https://lfenergy.org). This project's techincal charter is located in [https://github.com/lf-energy/foundation/blob/main/project_charters/seapath_charter.pdf](https://github.com/lf-energy/foundation/blob/main/project_charters/seapath_charter.pdf) and has established it's own processes for managing day-to-day processes in the project at [Project Governance](https://github.com/seapath/.github/blob/main/seapath_governance.md)
