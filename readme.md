mkninitcpio-unsquashtmpfs is a hook for the Arch Linux initramfs that decompresses a gzipped, squashfs image and mounts it to a tmpfs filesystem (i.e. memory).  It does so on the rootfs /mnt/tmpsquash.  It adds and requires these kernel parameters (kernel device name, LABEL, or UUID can be used):

   squashimgpath=[/device/...]:[/path/to/file.squashfs]
   squashtmpsize=[num. of bytes]

   HOOKS="... block unsquashtmpfs filesystems ..."
