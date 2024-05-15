<!---
  SPDX-FileCopyrightText: 2023 SAP SE

  SPDX-License-Identifier: Apache-2.0

  This file is part of FEDEM - https://openfedem.org
--->

![](https://img.shields.io/badge/STATUS-NOT%20CURRENTLY%20MAINTAINED-red.svg?longCache=true&style=flat) 

This public repository is read-only and no longer maintained.

[![REUSE status](https://api.reuse.software/badge/github.com/SAP/fedem-docs)](https://api.reuse.software/info/github.com/SAP/fedem-docs)

# FEDEM end user documention

![Fedem Logo](https://github.com/SAP/fedem-foundation/blob/main/cfg/FedemLogo.png)

## About this project

This project contains all end user documentation for FEDEM.
It consists of the following:

- LaTeX source files for the [Theory guide](src/TheoryGuide/)
- LaTeX source files for the [User's guide](src/UsersGuide/)
- HTML source and image files as well as build script for the [Reference Guide](src/ReferenceGuide/)

## Requirements and Setup

To compile the PDF-version of the Theory and User's Guides,
you need to have a [LaTeX](https://www.latex-project.org/) installation on your local computer.
On Windows, for instance, the [MiKTex](https://miktex.org/) package can be used.
Most Linux distributions can install a LaTeX compiler through their package management system.

To compile the CHM-file containing the Reference guide (on Windows only), you need to intall the
[Microsoft HTML Help Workshop](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-downloads) tool.

On Windows, you can then build the three documents by executing the bat-file
[make-docs.bat](make-docs.bat). To build and install the documentation in your
local installation of the [Fedem GUI](https://github.com/SAP/fedem-gui), execute

    make-docs.bat -install

It will assume you have cloned the [fedem-gui](https://github.com/SAP/fedem-gui)
repository under `%USERPROFILE%\Fedem-src` and built it. If any other location,
you need to edit line 19 in the bat script defining the `gui_dir` variable,
or specify the desired installation folder as command-line argument:

    make-docs.bat -install <doc_dir>

where `<doc_dir>` needs to be an existing directory.

## Contributing

This project is open to feature requests/suggestions, bug reports etc. via [GitHub issues](https://github.com/SAP/fedem-docs/issues). Contribution and feedback are encouraged and always welcome. For more information about how to contribute, the project structure, as well as additional contribution information, see our [Contribution Guidelines](CONTRIBUTING.md).

## Security / Disclosure

If you find any bug that may be a security problem, please follow our instructions at [in our security policy](https://github.com/SAP/fedem-docs/security/policy) on how to report it. Please do not create GitHub issues for security-related doubts or problems.

## Code of Conduct

We as members, contributors, and leaders pledge to make participation in our community a harassment-free experience for everyone. By participating in this project, you agree to abide by its [Code of Conduct](https://github.com/SAP/.github/blob/main/CODE_OF_CONDUCT.md) at all times.

## Licensing

Copyright 2023 SAP SE or an SAP affiliate company and fedem-docs contributors. Please see our [LICENSE](LICENSE) for copyright and license information. Detailed information including third-party components and their licensing/copyright information is available [via the REUSE tool](https://api.reuse.software/info/github.com/SAP/fedem-docs).
