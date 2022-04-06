# Dispersed Network Demo Project

This repository demonstrates how to integrate the Dispersed Network into a basic web application by leveraging the [Dispersed Network GitHub Release Action](https://github.com/dispersed-labs/dispersed-release-action).

## How It Works
The [dispersed.yml](.github/workflows/dispersed.yml) GitHub Workflow is triggered whenever a new [Release](https://github.com/dispersed-labs/demo-project/releases) is published, which does the following:
- The application gets built into a static production build via `npm run build`.
- The production build gets bundled for use on the Dispersed Network using the [dispersed-cli](https://github.com/dispersed-labs/dispersed-cli).
- The bundle gets uploaded as a binary asset to the GitHub Release that triggered the workflow.
- A GitHub Issue gets created with instructions for publishing the bundle on the Dispersed Network. This is currently a manual step because it involves signing transactions and spending gas.
