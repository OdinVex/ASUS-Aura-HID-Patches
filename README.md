# ASUS-HID-Fixes

I have not yet patched the other files. I would pretty-much have to patch EVERYTHING to make it all work. ASUS did some really stupid work regarding HID handling with ASUS Aura. They assumed that all calls to HID always succeed and that EVERY device supports reporting their capabilities AND that there is always some kind of extra capability. They did NOT handle HID API correctly. I may bother patching more DLLs but for now, only the following have been patched:

%ProgramFiles%\ASUS\Aac_Mouse\AacMouseHal_x86.dll
