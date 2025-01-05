Sandbox for Testing Packages
============================

A one-off disposable environment to test packages for the **`latest ubuntu`** release of our SW distros.

To get started, simply click on the badge below:

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/icub-tech-iit/test-packages-sandbox)

Instead, if you aim to test against different **`distros/releases`**, do:
1. 📝 Edit the file [`Dockerfile`](/.devcontainer/Dockerfile) and create a **`new branch`**. In detail, you have to fiddle with these [sections](/.devcontainer/Dockerfile#L7-L11).
1. 🚀 Launch the corresponding GitHub Codespace from within the new branch. Don't click on the main badge but rather use the green <kbd><> Code</kbd> button up here (switch to the tab `Codespaces`).
1. 🧹 Finish up by wiping out the branch.

### ⚠ How to flush the docker cache
As Docker relies on cached sections, you may still be using an old image when you've just updated a package to test. To invalidate the cache forcing Docker to build the relevant sections entirely again, apply the following workarounds:
- If you aim to build the whole image again, increase the variable [`INVALIDATE_DOCKER_CACHE_ALL`](/.devcontainer/Dockerfile#L5).
- If you've just fixed up the packages and aim to download and install them again, increase the variable [`INVALIDATE_DOCKER_CACHE_DL`](/.devcontainer/Dockerfile#L95).

