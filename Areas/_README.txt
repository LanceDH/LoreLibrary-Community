
## Get a feel of the the Areas module
Before you start adding files, please get a feeling of how the new Areas module works.
You can do this by updating your Lore Library to one of the 7.0.03 alpha builds.
These builds might include a debug window. If you close it you can reopen it by typing /lolib debug.

## Getting started
Start by having a look at the _Zone List file. Any of the zones marked with [X] have been completed.
Don't let that stop you from checking other people's work and even improving it (by adding lore, areas or just spell checking) and getting an idea on how to format you work.
To start a new zone, copy paste the _Template file, rename it to the name of the zone you're working on and change the zone name in the header.

## Adding areas
I'll try to make some guidelines of what should/shouldn't be an area;
- The goal is to either teach people about an area, or guide them to something interesting they likely missed during questing (if for example the lore was in a book)
- I mostly base areas on subzones (e.g. "The Dead Scar" in Eversong). If it has lore, add it, if it doens't, skip it.
- Aim for 7-9 areas per zone. If a zone has more, add more, if it has less, don't force it. Try staying below 15, but at least 4.
- Avoid this as much as possible, but if you are low on areas and there's something interesting that simply has no lore, leaving the lore to "" default it to "Not much is known about this area."
- Not bing a big lore person myself, I get my lore from Wowpedia pages of the subzones. Feel free to use your own writing skills and lore knowledge.
- Always keep lore in character (don't break the 4th wall) and wrtie in 3rd person.

## Getting coordinates
Area's are based on a radius around a point on the map, this has a default size but can be scaled.
If the player enters the radius while on the ground, they will 'trigger' the area (shows on the debug menu) and unlock the lore.
Because the point and radius is based on the coordinates of the map, smaller zones will have a bigger default radius (because a step suddenly covers more area on the map).
Don't worry about the scale when adding points, I will go trough every point myself to test them out and add the needed scale.
If you insist and can figure out how to add your points to you addon files, feel free to test them out yourself. I don't advise it because it will mess with your saved variablesin the future.
If you want to add an area, find the center of it and get your current coordinates by typing: /run print(GetPlayerMapPosition("player"))
This will print an x and y coordinate (from 0 to 1) in chat. just multiply them by 100 and format them as xx.xx (so 0.123456 becomes 12.34).