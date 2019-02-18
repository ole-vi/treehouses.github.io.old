<!-- Thank you for your contribution!

     Please file this form by replacing the Markdown comments
     with your text. If a section needs no action - remove it.

     Thank your for contributing to Treehouses

     See: treehouses.io for more info. -->

## Overview

<!-- Please give a short brief for the pull request,
     what problem it solves or how it makes things better. -->

## Testing recommendations

<!-- Describe how we can test your changes.
     Does it provides any behaviour that the end users
     could notice? -->
     
**Standard way**:

Prerequisites:
* [Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce)
* [`docker-compose`](https://docs.docker.com/compose/install/#install-compose)
* Virtualbox and Vagrant for Vagrant user (recommended if you're Windows)

Command:

Run the following command in you machine

```bash
docker-compose up
```

or (recommended for Windows user)

```bash
vagrant up
```

Then open `localhost:4000` on your browser.

## GitHub issue number

<!-- If this is a significant change, please file a separate issue at:
     https://github.com/treehouses/treehouses.github.io/issues
     and include the number here and in commit message(s) using
     syntax like "Fixes #472" or "Fixes treehouses/treehouses.github.io#472".  -->

## Related Pull Requests

<!-- If your changes affects multiple components in different
     repositories please put links to those pull requests here.  -->

## Checklist

- [ ] Code & Markdown is written and works correctly;
- [ ] Documentation reflects the changes;
