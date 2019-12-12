# ASUS-Aura-HID-Patches

I have not yet patched the other files. I would pretty-much have to patch EVERYTHING to make it all work. ASUS did some really stupid work regarding HID handling with ASUS Aura. They assumed that all calls to HID always succeed and that EVERY device supports reporting their capabilities AND that there is always some kind of extra capability. They did NOT handle HID API correctly. I may bother patching more DLLs but for now, only the following have been patched:

Patched:
%ProgramFiles%\ASUS\Aac_Mouse\AacMouseHal_x86.dll

The following need to be patched (someday) but I haven't gotten around to it:
%ProgramFiles%\ASUS\Aac_Mouse\AacMouseHal_x64.dll

I manually re-write the software after resizing the code section. Because the DLLs are compiled by ASUS with code-relocation enabled, I manually resize the relocation table and add manual entries into it to adjust new pointers to proper API calls. Eg I make my patches correctly.

If you still get crashes then another DLL is responsible but you should still use these too because any non-patched DLL WILL be a problem anyway! Create an Issue and attach any log you can. (Best to try to start the LightingService, attach a debugger and capture all DebugString output while then starting ASUS Aura! This would be a golden logging capture.)

Currently patching for: 1.07.71.

Quite frankly, ASUS needs to rewrite the entire AURA software and interfaces. I might go through the effort myself...
