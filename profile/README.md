# SEAPATH - (S)oftware (E)nabled (A)utomation (P)latform and (A)rtifacts (TH)erein

[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/5398/badge)](https://bestpractices.coreinfrastructure.org/projects/5398)

[![CI Yocto Weekly](https://github.com/seapath/ansible/actions/workflows/ci-yocto-weekly.yml/badge.svg)](https://github.com/seapath/ansible/actions/workflows/ci-yocto-weekly.yml)
[![CI Debian Weekly](https://github.com/seapath/ansible/actions/workflows/ci-debian-weekly.yml/badge.svg)](https://github.com/seapath/ansible/actions/workflows/ci-debian-weekly.yml)
[![CI SLES Weekly](https://github.com/seapath/ansible/actions/workflows/ci-sles-weekly.yml/badge.svg)](https://github.com/seapath/ansible/actions/workflows/ci-sles-weekly.yml)

[![SonarCloud on VM Manager](https://sonarcloud.io/api/project_badges/measure?project=seapath_vm_manager&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=seapath_vm_manager)
[![SonarCloud on python3-setup-ovs](https://sonarcloud.io/api/project_badges/measure?project=seapath_python3-setup-ovs&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=seapath_python3-setup-ovs)

[![ShellCheck on build_debian_iso](https://github.com/seapath/build_debian_iso/actions/workflows/shellcheck-weekly.yml/badge.svg)](https://github.com/seapath/build_debian_iso/actions/workflows/shellcheck-weekly.yml)

[![LFX Health Score](https://insights.linuxfoundation.org/api/badge/health-score?project=seapath)](https://insights.linuxfoundation.org/project/seapath)

[![LFX Contributors](https://insights.linuxfoundation.org/api/badge/contributors?project=seapath)](https://insights.linuxfoundation.org/project/seapath)

[![LFX Active Contributors](https://insights.linuxfoundation.org/api/badge/active-contributors?project=seapath)](https://insights.linuxfoundation.org/project/seapath)

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

Transmission system operators (TSOs) operate and develop the high-voltage transmission networks that transport electricity
over long distances. Distribution system operators (DSOs) operate the networks that deliver electricity from the transmission
system to consumers and distributed generation. Their responsibilities and network structures vary by country, but both need
reliable ways to monitor and control substations and the equipment connected to them.

Due to the Energy Transition, power flows are changing: generation is more distributed, infeed can occur at lower voltage
levels, and flow patterns can change more quickly. Grid control therefore needs to support more dynamic protection settings,
adaptive automation, faster extension, and coordination with central and local systems, while remaining dependable and interoperable.

Digital Substation Automation Systems (DSAS) bring together protection, automation and control (PAC) functions, like 
protection relays that detect faults and initiate circuit-breaker trips, and bay controllers that coordinate and monitor 
substation equipment. These functions can have strict, bounded response-time requirements: for example, a protection 
function may need to detect a fault and issue a trip without delay (not more than 50ms for most critical electrical network) 
that would compromise protection of equipment or grid stability. This is real-time in the control-system sense: predictable, 
bounded latency and low jitter matter, and missing a deadline can affect physical equipment and the power system. It is not 
simply the general-purpose IT meaning of a responsive service or high average throughput. Consequently, virtualization must be 
assessed for the timing and isolation guarantees of the complete system, including its hardware, network, configuration and 
workload.

Standards are part of this context. The IEC 61850 series specifies communication networks and systems for power utility
automation, including data models and communication services used in substation automation. The IEC 62351 series addresses
cybersecurity for power system communications, including security considerations for IEC 61850-based systems. SEAPATH is
intended to host PAC applications used in such environments; deployments must select and validate the applicable standards
and requirements for their equipment, applications and system configuration.

Remote administration and communication with central or local systems also make data management increasingly important.
DSAS therefore need greater modularity, interoperability and scalability than previous generations.

Virtualization is seen as a key innovation in order to fulfill these needs.

## Start with SEAPATH

The wiki section [Getting Started](https://lf-energy.atlassian.net/wiki/spaces/SEAP/pages/426377387/Starting+with+SEAPATH?atlOrigin=eyJpIjoiMTNhNjk2OTJlNjAzNDYzYzk2Yjk3ZTZmNzI4YWEyZWIiLCJwIjoiYyJ9) describes SEAPATH prerequisites and provide a step-by-step guide for beginners.

Below is a quick overview of the installation steps of SEAPATH and a link to relevant pages or repository.

- First, SEAPATH comes with two main distributions, Yocto and Debian. Choose your preferred version by reading the wiki page [SEAPATH-Debian or SEAPATH-Yocto](https://lf-energy.atlassian.net/wiki/x/7I7lAQ).
- Then, source your hardware following the wiki section [Prerequisites](https://lf-energy.atlassian.net/wiki/spaces/SEAP/pages/421527633/SEAPATH+prerequisites?atlOrigin=eyJpIjoiYjU0N2RkNGRiZDM0NGQxYmJhYjBhN2M3ZTQ1NzMyNDkiLCJwIjoiYyJ9).
- Install SEAPATH using the [installer](https://lf-energy.atlassian.net/wiki/spaces/SEAP/pages/537722925/Install+SEAPATH?atlOrigin=eyJpIjoiNTllM2YyYzM0OGRhNDMzZGJhNjQxYTcyZmQ4NGY4MWIiLCJwIjoiYyJ9)
- If you go for a cluster configuration, wire your machine following [Cluster machine wiring](https://lf-energy.atlassian.net/wiki/spaces/SEAP/pages/427622474/Cluster+setup+and+deployment#Machine-wiring).
- Finally, configure your machines using the [Ansible](https://github.com/seapath/ansible) repository.

More information on the [SEAPATH wiki](https://lf-energy.atlassian.net/wiki/x/C4DlAQ).

## Discussion

You can connect with the community in a variety of ways...

- [LINK TO MAILING LIST](https://lists.lfenergy.org/g/SEAPATH)
- [SEAPATH channel on LF Energy Slack](https://lfenergy.slack.com/archives/C01EH8ZLJTC)

## Contributing

Interested in contributing? Please read carefully the [CONTRIBUTING guidelines](/CONTRIBUTING.md).

## Security

For any security related questions or submissions, please review the [security policies](https://github.com/seapath/.github/blob/main/SECURITY.md).

## Governance

SEAPATH is a project hosted by the [LF Energy Foundation](https://lfenergy.org). This project's techincal charter is located in [https://github.com/lf-energy/foundation/blob/main/project_charters/seapath_charter.pdf](https://github.com/lf-energy/foundation/blob/main/project_charters/seapath_charter.pdf) and has established it's own processes for managing day-to-day processes in the project at [Project Governance](https://github.com/seapath/.github/blob/main/seapath_governance.md)
