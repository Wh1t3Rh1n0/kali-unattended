kali-unattended
===============
A simple unattended install setup that installs Kali Linux with the default
configuration.


Configuration Options Set By Default
------------------------------------
* Root password: toor
* Grub is installed to the MBR of /dev/sda.
* All files are installed to a single partition that uses the entire disk.


Instructions
------------
1. Boot to your choice of Kali Linux install media.

2. At the boot menu, select "Install" and press the Tab key on your keyboard
to edit the boot options.

3. Add the following options to the end of the line:

        url=http://[your-server]/preseed.cfg local=en_US hostname=kali domain=locale.lan

4. Press Enter. Once the install starts, you'll have to select your language,
but after that everything else will be automatic. 


Notes
-----
* Your preseed.cfg file must be accessible via HTTP. The wget command included
in the initial boot image does not seem to support HTTPS. Unfortunately this
means you can't just use the URL of my preseed.cfg file hosted on github.

* To save a little typing you can omit the locale, hostname, and domain options
in step 3, but you'll have to choose them at the beginning of the install if
you don't type them in at boot time.

* You can safely omit the 'http://' at the beginning of the preseed file URL
as long as your file is accessible over HTTP.

