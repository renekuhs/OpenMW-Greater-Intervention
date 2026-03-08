# (OpenMW) Greater Intervention
An OpenMW mod that adds Greater versions of Almsivi and Divine Intervention that allow you to select which previously discovered temple or shrine to teleport to. Highly compatible since it discovers Temple and Divine markers dynamically as the world loads. Also enhances standard Intervention spells by showing the closest discovered marker.

## Description
Adds Greater versions of Almsivi and Divine Intervention that allow you to select which previously discovered temple or shrine (respectively) to teleport to. They can be purchased from the highest ranking spell sellers of the Temple and Imperial Cult from the base game: Dileno Lloran in Vivec, High Fane for Greater Almsivi Intervention and Lalatia Varian in Ebonheart, Imperial Chapel for Greater Divine Intervention through corresponding dialog topics.

The mod is highly compatible. OpenMW and the base game are the only dependencies and, as far as I remember, nothing has been changed. The actual spell functionality has been implemented in Lua which enables the ability to find Temple and Divine markers as the world loads.
This all means that any mod should be compatible. Yes, Project Tamriel Rebuilt mods have been tested.

The list of discovered markers are saved on a save file basis so should be consistent per character.

There is now also functionality added that shows a message upon selecting a standard Intervention spell that shows the location of the nearest previously discovered marker, if the player is in an exterior cell. If using Magic Window Extender, the closest destination shows in the spell tooltip itself. Needless to say, this can be inaccurate if an undiscovered marker is actually closer. Can be disabled.

## Balancing
Since the spells provide an extremely powerful function, they have been balanced through the following means:
You must be a member of the respective faction and minimum rank Adept to purchase them. They cost 7,000 gold each.
The spells are very intense -- to realistically have a chance of casting them successfully, a Mysticism skill of ~50 is required, and a large Magicka pool. At ~65+, they can be cast reliably.

## Install
Like any other OpenMW mod:
Extract the mod and add the mod folder to the "Data Directories" tab of the OpenMW Launcher (by pressing the "Append" button on the right).
In the "Content Files" tab, enable "GreaterIntervention.omwaddon" and "GreaterIntervention.omwscripts".

## Configuration
See General Intervention Settings page in the main/pause menu under Options -> Scripts.

The following console command lists all entries in a specific list:
'''
luaGreaterInterventionList <list type (almsivi or divine)>
'''
The following command allows you to hide or unhide specific entries by specifying the index as shown by the previous command:
'''
luaGreaterInterventionHide <list type (almsivi or divine)> <index> <true or false>
'''

## Limitations
Does not work in multiplayer.
Since Magic Effects cannot be amended or added in OpenMW yet, the listed effect of the spell shows as Detect Key. Since v1.01, proper spell tooltips are now supported using Magic Window Extender﻿. The values of the effect are such that the desired cost of the cast is achieved. Note that the magic effect is removed from the player in the exact frame that the spell is cast.
Unable to find all Almsivi/Divine markers in the world in the current versions of OpenMW Lua. Hence why the standard Intervention destination functionality can only show the nearest discovered marker. This is in the works, though, and will be possible in the near future.
Standard Intervention enhancement doesn't work for interior cells that don't have direct access to an exterior cell. You will see "Unknown" in this case.

## Bugs
None that I have found. Let me know if you find any...
The most challenging part of this endeavour was definitely the UI. I haven't tested different scaling factors and font sizes, but the OpenMW docs assure me that those are taken in to account. Or I misunderstood :)

## Feedback
Feedback and suggestions are very welcome.

## Future
If there is interest shown, here are a few ideas I have.
Provide alternative version without balancing for those who want a more relaxed experience obtaining and using the spells. Could be in the form of wearables?
Currently, if the player was unaware of the mod, or forgot about it, there is no indication to the player of the existence of these spells apart from stumbling on the dialog topics by accident by talking to the two NPCs. Maybe the player could be informed through latest rumours?
I've tried to make the dialog fit in, and it works well enough, but perhaps the "lore" around the spells and how they came about could be expanded. Maybe even obtained through quests? I'm not a creative person at all so very much open to ideas...
Currently the locations are saved in the order of discovery. Maybe having an alphabetically sorted list would be more useful?
Localisation?
