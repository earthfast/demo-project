# Armada Demo Project

This repository demonstrates how to bundle a basic web application for the Armada network by leveraging the [Armada GitHub Release Action](https://github.com/armada-network/armada-release-action).

## How It Works

The [armada.yml](.github/workflows/armada.yml) GitHub Workflow is triggered whenever a new [Release](https://github.com/armada-network/demo-project/releases) is published, which does the following:

- The application gets compiled into a static production build via `npm run build`.
- The production build gets bundled for use on Armada using the [armada-cli](https://github.com/armada-network/armada-cli).
- The bundle and its checksum get uploaded as binary assets to the GitHub Release that triggered the workflow.
