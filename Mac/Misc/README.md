# No MacOS administrator account

5/30/2018

 **Problem:** __No Administrator accounts available on MacOS__

It seems that deleting the last administrator account does not even throw up a warning. Here's how to fix it.

 **Solution:**

You may need to hit **Enter** to call up the prompt (This might happen after more than one command. There will be a blank line at the end of the wall of text. Hit **Enter** in that case)

- **Reboot your Mac**. As soon as it starts, press and hold **⌘ + S** until you see a black screen with white lettering((If you end up back on the login screen after a flash of the black screen, enter your password and it should return to the black screen))
- **Check and repair the drive** by entering the command: `/sbin/fsck -fy`
- **Mount the drive as read-write** by using the command: `/sbin/mount -uw /`
- **Remove the Apple Setup Done file** by using the command: `rm /var/db/.AppleSetupDone`
- Use the **reboot** command: `reboot`
- Complete the setup process, and create a new admin account
- Promote your old account to an Admin, then delete the create admin account
