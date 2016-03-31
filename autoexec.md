If you want the magic buttons to work (1, 2, 3, and home server buttons, as well as the timer swap button) open up your ...tf/cfg/autoexec.cfg file and put the following in it:

```
alias JoinBookmark1 "connect 63.215.74.192:27015; password "  //Connects to Ubercharged.net #1
alias JoinBookmark2 "connect 217.163.27.214:27015; password "  //Connects to Ubercharged.net #2
alias JoinBookmark3 "connect ; password "  //Connects to nowhere
alias JoinHomeServer "connect ; password ; rcon_password "  //Put your match server info here

alias ToggleMinmode ""
alias ToggleMinmodeSmall "cl_hud_minmode 1;alias ToggleMinmode ToggleMinmodeBig" 
alias ToggleMinmodeBig "cl_hud_minmode 0;alias ToggleMinmode ToggleMinmodeSmall"    

ToggleMinmodeBig  //Change to ToggleMinmodeSmall if you prefer the small timers
```

The point is to make the buttons point to your favorite servers in the easiest way possible so you don't have to dig through a bunch of code in the HUD files.  Thanks to G-Mang for coming up with the idea of aliasing the connect functions in the autoexec.cfg file.  So long as you _**do not alter the alias names**_ and only **edit the IPs and passwords** to your liking, you should have no issues.

If you want the optional Mapper's toolbar to work properly, open up your ...tf/cfg/autoexec.cfg file and add the following:

```
alias HDRtoggle "HDRoff"
alias HDRon "mat_hdr_level 2; alias HDRtoggle HDRoff; echo HDR Enabled"
alias HDRoff "mat_hdr_level 0; alias HDRtoggle HDRon; echo HDR Disabled"

alias SpecToggle "SpecOff"
alias SpecOn "mat_specular 1; alias SpecToggle SpecOff; echo Specularity Enabled"
alias SpecOff "mat_specular 0; alias SpecToggle SpecOn; echo Specularity Disabled"

alias FogToggle "FogOff"
alias FogOn	"sv_cheats 1;fog_override 0;fog_enable 1; alias FogToggle FogOff; echo Fog Enabled"
alias FogOff "sv_cheats 1;fog_override 1;fog_enable 0; alias FogToggle FogOn; echo Fog Disabled"
```