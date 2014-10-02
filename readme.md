**mkninitcpio-unsquashtmpfs** is a hook for the Arch Linux initramfs that decompresses a root directory, gzipped, squashfs image and mounts it to a tmpfs filesystem (i.e. memory).  This is really only useful for an install disk.  It adds and requires these kernel parameters (for device: kernel device name, LABEL, or UUID can be used):

        root=/new_root
        squashimgpath=[/device/...]:[/path/to/file.squashfs]
        squashtmpsize=[number of bytes]

`HOOKS="... block unsquashtmpfs filesystems ..."`
