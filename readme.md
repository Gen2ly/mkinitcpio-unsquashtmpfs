**mkninitcpio-unsquashtmpfs** decompresses a root directory, squashfs image and mounts it to a tmpfs filesystem (i.e. memory).  Its motivation is for use on an install disk.  These kernel parameters are necessary (device name can be: kernel name, LABEL, or UUID):

        root=/new_root
        squashimgpath=[/device/...]:[/path/to/file.squashfs]
        squashtmpsize=[number of bytes]

 `HOOKS="... block unsquashtmpfs filesystems ...`