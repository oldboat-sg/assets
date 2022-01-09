# assets
A collection of assets that were used during the Oldboat project's development. You can find each package's use
below.

Got questions? Join our Discord.
https://oldlbsg.net

## arenas
Each arena has unique properties required for the game to properly function. These properties are stored in the
`arenas` package. The specification is as follows:
- `display_name`: The display name of the arena, as shown to the client. e.g. `Origins`.
- `numeric_id`: The numeric ID of the arena. It is not used internally, instead preferring the arena properties' name,
   however with its extension trimmed, e.g. `origins`.
- `sign_positions`: The block position(s) of the sign(s) that allow the users to join the arenas.
- `death_match_position`: The position that the death match arena is created at. This is always the center of the map,
   as it was in Lifeboat 2014.
- `save`: The save file (excluding the `.zip` extension) in the `saves` package.
- `pedestal_positions`: The block positions at which the pedestals are located, used for adding players to the arena.
- `chest_positions`: The block positions at which the chests are located, used for filling chests.

## saves
The worlds used for each arena. The format is the vanilla `mcworld` format, however only up to date to `v1.17.0`. The
name of each save is the one referenced in the arena properties, under the `save` key.

All worlds are public domain, scattered on various sites, however in different formats. Each world was manually converted
to the `mcworld` format mostly using `chunker.app` and sometimes my `pmf` implementation, for extremely legacy worlds
such as Origins.

## structures
Various `mcstructure` files, used for various purposes.

Most notably, the `deathmatch_arena.mcstructure` is used for enerating death match arenas, as they're generated in the
same world being played in, and only at the end of the match. The position it is generated at is reliant on the arena
properties, under the `death_match_position` key.
