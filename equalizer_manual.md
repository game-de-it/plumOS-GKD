# plumOS equalizer manual

# Requirements
- pipewire
- pipewire-pulse

# Configuration files
- Equalizer tone definition file  
`/storage/.config/pipewire/pipewire.conf.d/sink-eq6.conf`

- Equalizer volume adjustment file  
`/storage/bin/setvol.sh`

- Equalizer ON/OFF file  
`/storage/bin/Equalizer.sh`

--- 
# Details of each file

## sink-eq6.conf
Basically, the part you need to change is something like `control = { "Freq" = 100.0 "Q" = 1.0 "Gain" = 0.0 }`.
you will need to restart the pipewire and pipewire-pulse processes or restart the OS.

- Freq  
The frequency (Hz) to be changed.

- Q  
The value of how much frequency is involved around the frequency set by Freq.
The higher the Q value, the narrower the affected bandwidth.
For example, if you set the Q value to 4.3, the bandwidth will be very narrow and may sound unnatural.
(By increasing the Q value and lowering the Gain, you can pinpoint and reduce specific frequencies, making it like a noise filter.)
Setting it to a fairly gentle value between 0.6 and 1.0 sounds good.

- Gain  
Set the amplification value between -10 and 20.


## setvol.sh
Adjusts the volume of the equalizer sink (effect_input.eq6) when the OS starts.
The adjusted volume refers to the volume in the Emulationstation configuration file.
If you do not use this script, a loud sound may occur after pressing the volume button after the OS starts.
The `/storage/.config/autostart/custom_start.sh` file executes setvol.sh when the OS starts.


## Equalizer.sh
Turns the EQ function on or permanently turns it off.
The EQ function is turned on when the configuration file `sink-eq6.conf` is in the `/storage/.config/pipewire/pipewire.conf.d/` directory.
The EQ function is turned off by moving the `sink-eq6.conf` file to another location.
A symbolic link for the `Equalizer.sh` file is created in the `/storage/.config/modules/` directory so that it can be executed from the tools section of Emulationstation.

---
# Equalizer command reference
- `pactl get-default-sink`  
The currently applied sink name is displayed.

- `pactl list sinks`  
You can check the sink status.

- `pactl set-default-sink <sink name>`  
Applies the specified sink.
The default sink name for GKD StockOS is `alsa_output._sys_devices_platform_rk809-sound_sound_card0.stereo-fallback`.
The EQ sink name is `effect_input.eq6`.  
Even if the game program is running, you can use these commands to turn the sink on and off in real time.
However, to apply the contents of the EQ setting file `sink-eq6.conf`, you will need to restart the pipewire and pipewire-pulse processes or restart the OS.

- `pactl set-sink-volume <sink name> <volume value>%`  
Sets the volume of the specified sink.
When using an EQ sink, the volume of the `alsa_output._sys_devices_platform_rk809-sound_sound_card0.stereo-fallback` sink affects the overall volume, so it must always be set to 100%.
For example, if you enable the EQ sink name effect_input.eq6 while setting alsa_output._sys_devices to 50%, the sound will be quiet even if you set the volume of effect_input.eq6 to 100%.

That's it.

