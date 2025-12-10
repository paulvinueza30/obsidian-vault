

Packages: collections of files: executables, libs, configs, and docs bundled together for easy distribution and installation

Package managers: cli/gui tool that automates the process of installing, updating , and removing packages

Low level package managers don't automatically handle deps installation

Flow:
High Level manager figure out required software -> download -> use low level manager to install in order
## List of Package Managers

1. apt (advanced packaging tool) : debian based default package manger
2. pacman : arch-based package manager
3. dnf :fedora based distro default package manager
4. dpkg (debian package manager) : low-level package manager used with apt
5. rpm (fedora) : low level package manger used with dnf