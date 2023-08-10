# GitHub Actions installer for Scalable Git Branching Tools

This action adds the [git branching tools](https://github.com/PrincipleStudios/scalable-git-branching-tools)
to your GitHub actions job.

By default, this installs the latest version of the tools, as indicated by the `main` branch.

If you intend to make changes (such as adding upstream branches), do not forget to set the author name and email address.

```sh
git config --local user.email "${INPUT_AUTHOR_EMAIL}"
git config --local user.name "${INPUT_AUTHOR_NAME}"
```

# Usage

```yaml
- uses: PrincipleStudios/scalable-git-branching-tools-installer-action@v1
  with:

    # Directory in which to checkout the git tools
    # default: '${{ runner.temp }}/git-tools'
    tools_path: ''

    # Repository containing the git tools
    # default: PrincipleStudios/scalable-git-branching-tools
    repository: ''

    # Version of the git tools repository to install. Must be a commitish from the repository.
    # default: main
    version: ''

    # Directory with a git project in which to install the git tools
    # default: '${{ github.workspace }}'
    repo_path: ''
```

# Scenarios

TBD
