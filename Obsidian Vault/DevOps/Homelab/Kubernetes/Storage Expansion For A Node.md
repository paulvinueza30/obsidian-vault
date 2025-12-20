Here is the objective technical breakdown of the storage expansion process using **LVM (Logical Volume Management)**. This documentation tracks the transition from a raw disk to usable filesystem space.

### 1. Identify the Block Device

Before starting, use `lsblk` to identify the disk names and current partition sizes. This command displays the hierarchy of storage devices.

```bash
lsblk

```

* **Purpose:** Confirms the new disk (e.g., `/dev/sdb`) is detected by the kernel and shows the existing Logical Volume (LV) path.

### 2. Initialize the Physical Volume (PV)

Raw disks must be initialized for LVM before they can be added to a group.

```bash
sudo pvcreate /dev/sdb

```

* **Purpose:** Formats the device with LVM metadata so it can be recognized as a physical building block.
* **Verification:** `sudo pvdisplay /dev/sdb`

### 3. Extend the Volume Group (VG)

The new Physical Volume is added to the existing Volume Group pool.

```bash
sudo vgextend ubuntu-vg /dev/sdb

```

* **Purpose:** Increases the total capacity of the storage pool (`ubuntu-vg`) by merging the new disk's capacity into it.
* **Verification:** `sudo vgdisplay ubuntu-vg` (Check the `Free PE / Size` line).

### 4. Expand the Logical Volume (LV) and Resize the Filesystem

The final step allocates the free space in the Volume Group to the specific Logical Volume where the OS or application resides.

```bash
sudo lvextend -l +100%FREE -r /dev/ubuntu-vg/ubuntu-lv

```

* **Purpose:** * `lvextend -l +100%FREE`: Grows the Logical Volume to use all available space in the VG.
* `-r`: Triggers the filesystem-specific resize tool (like `resize2fs` for EXT4 or `xfs_growfs` for XFS) to make the space usable by the OS.



### 5. Final Space Verification

Confirm the changes are reflected at the filesystem level.

```bash
df -h /

```

* **Purpose:** Displays the total, used, and available space for the root directory.