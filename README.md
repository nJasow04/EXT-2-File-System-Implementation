# Hey! I'm Filing Here

In this lab, a 1 MiB ext2 file system image was created, encompassing two directories, a regular file, and a symbolic link. The project involved a deep dive into the ext2 file system internals, providing practical experience with real file system structures and operations.

ext2-create.c: The core file where the ext2 file system is implemented.
Makefile: Facilitates the compilation of the project.
cs111-base.img: The generated ext2 file system image.

## Building

make — compile sthe ext2-create executable which will create the ext2 filesystem image

## Running

Running
Follow these steps to run the project:

Create File System Image: Generate the cs111-base.img file by executing:
./ext2-create

Inspect File System: To check the structure and integrity of the created filesystem, use:
dumpe2fs cs111-base.img
fsck.ext2 cs111-base.img

Mount File System:
- Create a mount point:
    mkdir mnt
- Mount the image:
    sudo mount -o loop cs111-base.img mnt


## Cleaning up

After you're done with the file system:

Unmount the File System:
sudo umount mnt

Remove the Mount Directory:
rmdir mnt

Clean Compiled Binaries:
make clean
