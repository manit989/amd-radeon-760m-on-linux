# GUIDE TO SETUP DELL G15 5535 's AMD 760M IGPU ON LINUX
- if your distro is using radeon driver and have blacklisted amdgpu in /etc/modprobe.d/ directory first edit blacklist file the modprobe.d/ directory and change it to
``blacklist radeon``
- now download amdgpu-install script from amd's website and run it.
`` amdgpu-install ``
- NOTE: If you are using popos 22.04 run script with --no-dkms flag otherwise many errors will be thrown
`` amdgpu-install --no-dkms ``
- Use envycontrol to switch between nvidia,radeon or hybrid graphics mode

# FOR VOID LINUX USERS
- blacklisting radeon won't work
- add radeon.si_support=0 and amdgpu.si_support=1 acpi_backlight=native to GRUB_CMDLINE_LINUX_DEFAULT in /etc/default/grub
- note you don't have to use amdgpu-install script
- you just have to install linux-firmware and linux-firmware-amd package
