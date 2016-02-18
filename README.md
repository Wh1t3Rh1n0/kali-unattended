kali-unattended
===============
A simple unattended install setup that installs Kali Linux with the default
configuration.


Configuration Options Set By Default
------------------------------------
* Root password: toor
* Grub is installed to the MBR of the first hard disk.
* All files are installed to a single partition that uses the entire disk.


Instructions
------------
1. Boot to your choice of Kali Linux install media.

2. At the boot menu, select "Install" and press the Tab key on your keyboard
to edit the boot options.

3. Add the following options to the end of the line:

        url=http://[your-server]/preseed.cfg local=en_US hostname=kali domain=locale.lan

4. Press Enter. Once the install starts, you'll have to select your language,
but after that *almost* everything else will be automatic. At the moment


Notes
-----
* If you really to, you can omit the locale, hostname, and domain options in
step 3, but you'll have to choose them at the beginning of the install if you
don't type them in at boot time.

* Your preseed.cfg file must be accessible via HTTP. The wget command included
in the initial boot image does not seem to support HTTPS.