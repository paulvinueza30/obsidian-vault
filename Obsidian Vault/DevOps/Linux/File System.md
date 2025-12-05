### Sub Directories
- **`/` (Root)**: The starting point of the filesystem. All other directories and files branch off from here.
- **`/bin`**: Essential command binaries needed for the system to function in single-user mode (e.g., `ls`, `cp`, `mv`). These are available to all users.
- **`/sbin`**: System binaries, similar to `/bin`, but typically reserved for the root user for administrative tasks.
- **`/boot`**: Bootloader files, including the Linux kernel itself.
- **`/dev`**: Device files that represent hardware components. These act as interfaces for the system to interact with hardware.
- **`/etc`**: The nerve center for system configuration. Nearly every service or application stores its configuration files here.
- **`/home`**: Personal directories for each user. This is where regular users store their documents and personal files.
- **`/lib`**: Essential shared libraries required by the binaries in `/bin` and `/sbin`.
- **`/mnt`**: Temporary mount points used to mount filesystems (like USB drives) temporarily.
- **`/opt`**: Optional software packages. Often used for third-party software that doesn't split its files across the standard hierarchy.
- **`/proc`**: A virtual filesystem that provides an interface to kernel data structures. It is used to access live process information and kernel parameters.
- **`/root`**: The home directory specifically for the root user (separate from `/home` to ensure access even if the `/home` partition fails).
- **`/tmp`**: Temporary files. Content here is often cleared automatically upon system reboot.
- **`/usr`**: A secondary hierarchy for user programs, libraries, and documentation. It contains subdirectories like `/usr/bin` and `/usr/lib`.
- **`/var`**: Variable data files that are expected to grow over time, such as system logs, databases, print spools, and email.

### Filesytem Types

- **Ext4**: The most widely used filesystem in Linux, known for its balance of performance, reliability, and features.
- **XFS**: High-performance filesystem with robust scalability, often used in enterprise environments.
- **Btrfs**: A newer filesystem designed for fault tolerance, repair, and easy administration.
- **ZFS**: Known for data integrity and scalability, commonly used in storage solutions.
- **vfat**: Compatibility layer for FAT filesystems, often used in USB drives and external devices.
- **NFS**: Network File System, used to share files over a network.

Inodes are data structures that store metadata about files i.e. (file size, permission, ownership ,etc.)

