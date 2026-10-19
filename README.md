# Specdriven App

*UI Demo: https://specdrivenapp-demo.up.railway.app/*

- Pragmatic specifications tool the whole team will love -- PM, UX, Dev, and Test.
- Low ceremony and multi-modal by design.
- Each spec (scenario) has a unique deep link.
- Promotes iterative and incremental development.
- Supports bi-directional traceability to automated tests written with the test framework of your choice.
- Integrates with Aha!, Jira, Linear, Figma, GitHub, and all major AI code agents. [future]
- Specs are stored separately from code -- ready for long term maintenance where technical implementation may change dramatically.
- AI agents see specs as files in the ‘specs’ folder and can propose additional specifications by writing into this folder.
- Fast local search.
- Only need Git repo to start -- uses automerge.org as a peer-to-peer DB. Server will be developed for larger projects in the future.

## Install on Mac or Linux

```bash
curl -fsSL https://raw.githubusercontent.com/SpecDriven/specdriven-app-release/main/install.sh | sh
```

On Mac, you should now have a SpecDriven App in your Applications on Mac.

For sample data, fork https://github.com/SpecDriven/specs-insurance and clone it locally.

## Install on Windows

In PowerShell (not as Administrator):

```powershell
irm https://raw.githubusercontent.com/SpecDriven/specdriven-app-release/main/install.ps1 | iex
```

It verifies and unpacks the source under `%USERPROFILE%\.specdriven\app`,
offers to install [Bun](https://bun.sh) if it is missing, builds the desktop
app, adds SpecDriven to the Start menu and starts it. SpecDriven keeps its data
in git, so install [Git for Windows](https://git-scm.com/download/win) too.

## License

Copyright (c) 2026 David Vydra (https://specdriven.app)

specdriven.app is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License, version 3 only (SPDX: AGPL-3.0-only), as published by the Free Software Foundation. LICENSE.md holds the full text.

It is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for details.

If you run a modified copy as a network service, the license asks you to offer its users the source of your version; set SPECDRIVEN_SOURCE_URL so the app's "Source code" link points at it.

No trademark rights are granted. "SpecDriven" and "specdriven.app" are not licensed under the AGPL.
