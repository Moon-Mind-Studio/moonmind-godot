# moonmind-godot
A custom godot build (based on this godot branch: https://github.com/godotengine/godot/tree/3.5) + dragonbones (based on this rep: https://github.com/mauville-technologies/godot_dragonbones) + SteamGodot (based on this rep: https://github.com/Gramps/GodotSteam) + mono


```C#
# Build temporary binary
scons p=windows tools=yes module_mono_enabled=yes mono_glue=no
# Generate glue sources
bin\godot.windows.tools.64.mono --generate-mono-glue modules/mono/glue

### Build binaries normally
# Editor
scons p=windows target=release_debug tools=yes module_mono_enabled=yes
# Export templates
scons p=windows target=release_debug tools=no module_mono_enabled=yes
scons p=windows target=release tools=no module_mono_enabled=yes
```