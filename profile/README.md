# SEAPATH - (S)oftware (E)nabled (A)utomation (P)latform and (A)rtifacts (TH)erein
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/5398/badge)](https://bestpractices.coreinfrastructure.org/projects/5398)

[![SonarCloud on VM Manager](https://sonarcloud.io/api/project_badges/measure?project=seapath_vm_manager&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=seapath_vm_manager)
[![SonarCloud on python3-setup-ovs](https://sonarcloud.io/api/project_badges/measure?project=seapath_python3-setup-ovs&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=seapath_python3-setup-ovs)

[![ShellCheck on build_debian_iso](https://github.com/seapath/build_debian_iso/actions/workflows/shellcheck.yml/badge.svg)](https://github.com/seapath/build_debian_iso/actions/workflows/shellcheck.yml)
[![Ansible-lint on Ansible repository](https://github.com/seapath/ansible/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/seapath/ansible/actions/workflows/ansible-lint.yml)
[![Complete CI on Debian Ansible repository](https://github.com/seapath/ansible/actions/workflows/ci-debian.yml/badge.svg)](https://github.com/seapath/ansible/actions/workflows/ci-debian.yml)

## Mission

The mission of the **SEAPATH** project is to **develop a “reference design” and “industrial grade” open source
real-time platform** that can run virtualized automation and protection applications (for the power grid industry
in the first place and potentially beyond). This platform is intended to host multi-provider applications.

The project will encompass the following activities:
- Specifying the requirements to be fulfilled by the reference platform
- Specifying the test procedures needed to assess the fulfillment of the requirements
- Building the appropriate system(s) architecture(s) for the software platform and specifying requirements for
hardware architecture
- Developing code for the specific functions and services to be delivered by the platform
- Defining and implementing APIs to external applications
- Performing the integration of the software platform
- Testing the fulfillment of the requirements after the implementation, as a proof-of-concept, of a realistic protection and
automation system on top of the integrated software platform
- Defining guidelines and best practices to integrate, test (including interoperability tests) deploy, and maintain
the applications on such platform


*The project will take benefit from standardization activities that define requirement references for the use cases
targeted by the virtualization platform. Relevant standards could for instance include IEC 60255, IEC 60870, IEC 61850
and IEC 61869. In the case where the requirements and guidance from the standards are not appropriate or still work in
progress,the project may have to take different choices. In such case the project will strive to provide feedback to the
relevant standardization activities.*

## Want to give it a try ?

 You can start from [here](https://github.com/seapath/seapath-architecture)

## Background

Due to the Energy Transition the use of power transmission and distribution grids is changing. The control architecture of
power grids needs to be swiftly adapted to take account of infeed at lower grid levels, higher dynamics in flow patterns and
more distributed controls (both internal controls and grid flexibility services from third parties).

In this context TSOs and DSOs require a new generation of Digital Substation Automation Systems (DSAS) providing more
dynamic protection settings and adaptive automation functions. Moreover, data management gets significant, both for the
remote administration of deployed automation and protection functions, as well as for the communication with central or
local systems and processes. Thus the design of the new DSAS will have to allow for a drastically higher level of modularity,
interoperability and scalability compared to the previous generations.

Virtualization and open source collaborations will be key features in order to fulfill the needs above. They are expected
to boost substantially (see motivations in the initial roadmap document):
-	time and cost-efficiency,
-	scalability and flexibility,
-	innovation,
- vendor-agnostic implementations and convergence of utility practices.

## Discussion

You can connect with the community in a variety of ways...

- [LINK TO MAILING LIST](https://lists.lfenergy.org/g/SEAPATH-TSC)
- [SEAPATH channel on LF Energy Slack](https://lfenergy.slack.com/archives/C01EH8ZLJTC)

## [Roadmap](/ROADMAP.md)


## Contributing

Interested in contributing? Please read carefully the [CONTRIBUTING guidelines](/CONTRIBUTING.md).

# Governance

SEAPATH is a project hosted by the [LF Energy Foundation](https://lfenergy.org). This project's techincal charter is located at [https://github.com/lf-energy/foundation/blob/main/project_charters/seapath_charter.pdf](https://github.com/lf-energy/foundation/blob/main/project_charters/seapath_charter.pdf) and has established it's own processes for managing day-to-day processes in the project at [Project Governance](https://github.com/seapath/contributing/blob/master/CONTRIBUTING.md#project-governance).
