# M4KC

![Grass block icon](icon.png)

*Minecraft 4K - C Rewrite*

For those who don't know, Minecraft 4K was a stripped down version of Minecraft submitted by Notch to the [Java 4K Game Programming Contest](https://en.wikipedia.org/wiki/Java_4K_Game_Programming_Contest), where each submission had to be under 4 kilobytes in size. Its wiki page can be found [here](https://minecraft.fandom.com/wiki/Minecraft_4k).

Being so small, the game proved somewhat easy to de-compile and edit. [Multiple people have given this a go, including me](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/minecraft-mods/1290821-minecraft-4k-improved-by-crunchycat-download-now).

This project is an attempt to translate the game into C in order to increase its performance, and to provide a platform upon which to add new features.

## Bug list

* "Sticky" block collision - this behavior is present in the original version and I have been trying to work out ways to fix it for a while.
* Block outline cuts off at mouse x position.

## Goals for this project

* Maintaining the original look and feel as closely as possible.
* Keeping the final executable under 10 KB (on Linux, with the system I have set up in the makefile)
* More blocks
* Perlin noise terrain generation (water, caves, etc)
* Infinite worlds, possibly vertically too
* Mobs and multiplayer (this would require changing the rendering engine to some degree)
* Day/night??? I don't know whether or not this would change the look or feel too much.

## Dependencies

### Bare minimum to make this code run
* SDL2
* A C compiler

### To get it down to a small size, you need
* gcc (have not tried the flags with other compilers)
* gzexe

## Places

There is a forum thread for this project [here](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/minecraft-mods/3081789-minecraft-4k-c-rewrite)

I will be uploading binaries [here](https://holanet.xyz/soft/m4kc/)

## Game info

Some extra info about the game.

### All blocks by ID
 ID | Block  | Planned 
----|--------|---------
  0 | Air    | Air
  1 | Grass  | Grass
  2 | Dirt   | Stone
  3 | Dirt   | Dirt
  4 | Stone  | Cobblestone
  5 | Bricks | Planks
  6 | Dirt   | Sapling
  7 | Wood   | Bedrock
  8 | Leaves | Water
  9 | Dirt   | Stationary water
 10 | Dirt   | Lava
 11 | Dirt   | Stationary lava
 12 | Dirt   | Sand
 13 | Dirt   | Gravel
 14 | Dirt   | Gold ore
 15 | Dirt   | Iron ore
 16 |        | Coal ore
 17 |        | Wood
 18 |        | Leaves
 19 |        | Sponge
 20 |        | Glass
 21 - 36 |   | Wool
 37 |        | Dandelion
 38 |        | Rose
 39 |        | Brown mushroom
 40 |        | Red mushroom
 41 |        | Gold block

See [this list](https://www.minecraftforum.net/forums/minecraft-java-edition/discussion/114963-all-item-block-ids-in-one-place) for all planned items.

### Controls
How to play the game.

#### Keyboard
  Key  |    Action
:-----:|---------------
   W   | Move forward
   S   | Move backward
   A   | Strafe left
   D   | Strafe right
 Space | Jump
  ESC  | Pause

#### Mouse
* Move mouse: Look around
* Right click: Place block
* Left click: Break block