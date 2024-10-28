# Features
- **Filesystem Support**: Format devices with ext4, NTFS, XFS, VFAT, Btrfs, or exFAT filesystems.
- **Unmount Check**: Automatically checks if the device is mounted and unmounts it if necessary.
- **Labeling**: Option to assign a label to the formatted filesystem.
- **Quick Format**: Option for a quick format (where supported).
# Prerequisites
- `mkfs` utilities for the desired filesystem types (e.g., `mkfs.ext4`, `mkfs.ntfs`, etc.)
- `findmnt` utility (for checking mounted devices)
# Arguments
- `<device>`: The device to format (e.g., /dev/sdX1).
- `-f`, `--filesystem`: The filesystem type to use (options: ext4, ntfs, xfs, vfat, btrfs, exfat).
- `-l`, `--label`: Optional label for the filesystem.
- `-q`, `--quick`: Perform a quick format (where applicable).
## Example
- Format a device `/dev/sdb1` to `NTFS` with a label "MyUSB" and perform a quick format:
```bash
./4Matter.py /dev/sdb1 -f ntfs -l MyUSB -q
```
> [!CAUTION]
>- Data Loss Warning: Formatting a device will erase all data on it. Ensure you have backups before proceeding.
>- Permissions: You may need to run the script with sudo depending on your system permissions.
# Contributing
Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.
