# GUIDE TO SETUP DELL G15 5535 's AMD 760M IGPU ON LINUX
- if your distro is using radeon driver and have blacklisted amdgpu in /etc/modprobe.d/ directory first edit blacklist file the modprobe.d/ directory and change it to
``blacklist radeon``
- now download amdgpu-install script from amd's website and run it.
`` amdgpu-install ``
- NOTE: If you are using popos 22.04 run script with --no-dkms flag otherwise many errors will be thrown
`` amdgpu-install --no-dkms ``
- Use envycontrol to switch between nvidia,radeon or hybrid graphics mode
