# Enabling shared folders on ElementaryOS VM

1. Download GuestAdditions iso from VirtualBox
2. Attach iso to VM (Settings -> Storage -> Controller:IDE
3. On guest VM, view in Files (for some reason it wasn't visible in terminal before this)
4. In terminal, navigation to /media/michael/<VBOX_ADDITIONS_FOLDER>/
5. sudo sh ./VBoxLinuxAdditions.run


# Mounting a shared folder

1. Settings > Shared Folders
2. Add folder to share on host machine
3. On guest VM, create the folder to mount to
4. sudo mount -t vboxsf -o uid=$UID,gid=$(id -g) <share folder> <path on guest>
  - where:
    + <share folder> is the name given in host VirtualBox settings
    + <path on guest> path the folder created in step 3


## References

https://help.ubuntu.com/community/VirtualBox/SharedFolders
