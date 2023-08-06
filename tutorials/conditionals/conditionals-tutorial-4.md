# Customize Goal Music and Splash Screen

## Introduction @unplugged

In this lesson you will include detecting whether the robot is on a coin and collecting it as the robot moves across the tilemap.
![Logic If](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-robot-control-structures/main/docs/static/robot-cs-condition-coin-2.png "Logic If" )

## Step One

Rewrite the code or copy and paste it from the prior activity.

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    robot.move_forward()

def on_update():
    if robot.goal_reached():
        music.play(music.melody_playable(music.magic_wand), music.PlaybackMode.UNTIL_DONE)
        game.splash("Your Text Here.")
        game.reset()
game.on_update(on_update)
```

## Step Two

Click in the ``||logic:logic||`` category and drag in the ``||logic:if||`` below the robot.turn_left() but only tabbed over once.
![Logic If](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-robot-control-structures/main/docs/static/robot-cs-condition-coin-1.gif "Logic If" )

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    if True:
        pass
    robot.move_forward()

def on_update():
    if robot.goal_reached():
        music.play(music.melody_playable(music.magic_wand), music.PlaybackMode.UNTIL_DONE)
        game.splash("Your Text Here.")
        game.reset()
game.on_update(on_update)
```
## Step Three

Replace the True with ``||robot:detect coin||`` code to check whether there is a coin currently where the robot is located.

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    if robot.detect_coin():
        pass
    robot.move_forward()

def on_update():
    if robot.goal_reached():
        music.play(music.melody_playable(music.magic_wand), music.PlaybackMode.UNTIL_DONE)
        game.splash("Your Text Here.")
        game.reset()
game.on_update(on_update)
```

## Step Four

Drag in the code ``||robot:collect coin||`` to where the pass is.  Now run the code to see if the robot collects the coins as it makes its way to the goal.

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    if robot.detect_coin():
        robot.collect_coin()
    robot.move_forward()

def on_update():
    if robot.goal_reached():
        music.play(music.melody_playable(music.magic_wand), music.PlaybackMode.UNTIL_DONE)
        game.splash("Your Text Here.")
        game.reset()
game.on_update(on_update)
```

## Step Five

It looks like the robot may fall short of the goal.  Think about what part of your code needs to change.  Is the code repeating enough times?

    

```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"></block></xml>",
  "main.py": "",
  "main.ts": "\n",
  "pxt.json": "{\n    \"name\": \"Non Git Hub Robot Assets CS Skillmap Conditionals 2\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n        \"tilemaps\": \"github:microsoft/pxt-tilemaps#v1.12.0\",\n        \"Robot Extension\": \"github:MrDGuy/robot-extension#78515172c0af9925b021b75d9267df02d989c749\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\",\n        \"main.py\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.13.31\",\n        \"tag\": \"v1.13.31\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/ef3aad740700f5159eebccf721fa35d32683fcaa\",\n        \"target\": \"1.13.31\",\n        \"pxt\": \"9.1.6\"\n    },\n    \"preferredEditor\": \"pyprj\"\n}\n",
  "tilemap.g.jres": "{\n    \"tile1\": {\n        \"data\": \"hwQQABAAAAD//////////09ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPT//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"startTile\"\n    },\n    \"tile2\": {\n        \"data\": \"hwQQABAAAAD//////////4+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPj//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"goalTile\"\n    },\n    \"tile3\": {\n        \"data\": \"hwQQABAAAAD//////////x8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfH//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"floorTile\"\n    },\n    \"tile4\": {\n        \"data\": \"hwQQABAAAAD//////////393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/f//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"coinTile\"\n    },\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"tile5\": {\n        \"data\": \"hwQQABAAAAD//////////7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/v//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"wallTile\"\n    },\n    \"level1\": {\n        \"id\": \"level1\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAwYTAwMDcwMDAzMDQwNDBiMDQwNDBiMDQwNDA1MDkwZjBmMGYwZjBmMGYwMjEwMDYwOTBmMGYwZjBmMGYwZjExMDIwNjBlMGYwMjExMDIwZjAyMDIwZjBkMDkwMjAyMGYwMjExMDIwZjBmMDYwOTAxMGYwZjBmMGYwZjBmMDAwNjA4MGEwYTBjMGEwYTBjMGEwYTA3MjIyMjIyMjIyMjIyMjIyMjAyMjAyMjIyMjIwMjIwMjIwMDIwMDAyMjAyMjAwMDIwMjIwMjIyMjIyMjIyMjIyMjIyMjIyMg==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"myTiles.tile1\",\n            \"myTiles.tile3\",\n            \"sprites.dungeon.greenOuterNorthWest\",\n            \"sprites.dungeon.greenOuterNorth0\",\n            \"sprites.dungeon.greenOuterNorthEast\",\n            \"sprites.dungeon.greenOuterEast0\",\n            \"sprites.dungeon.greenOuterSouthWest\",\n            \"sprites.dungeon.greenOuterSouthEast\",\n            \"sprites.dungeon.greenOuterWest0\",\n            \"sprites.dungeon.greenOuterSouth1\",\n            \"sprites.dungeon.greenOuterNorth2\",\n            \"sprites.dungeon.greenOuterSouth2\",\n            \"sprites.dungeon.greenOuterEast2\",\n            \"sprites.dungeon.greenOuterWest2\",\n            \"myTiles.tile5\",\n            \"myTiles.tile2\",\n            \"myTiles.tile4\"\n        ],\n        \"displayName\": \"level1\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile2 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile3 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile4 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile5 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tilemap\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"level1\":\n            case \"level1\":return tiles.createTilemap(hex`0a0007000304040b04040b040405090f0f0f0f0f0f021006090f0f0f0f0f0f1102060e0f0211020f02020f0d0902020f0211020f0f0609010f0f0f0f0f0f0006080a0a0c0a0a0c0a0a07`, img`\n2 2 2 2 2 2 2 2 2 2 \n2 2 2 2 2 2 2 . . 2 \n2 2 2 2 2 2 2 . . 2 \n2 2 . . . 2 . . 2 2 \n2 . . 2 . . . 2 2 2 \n2 . 2 2 2 2 2 2 2 2 \n2 2 2 2 2 2 2 2 2 2 \n`, [myTiles.transparency16,myTiles.tile1,myTiles.tile3,sprites.dungeon.greenOuterNorthWest,sprites.dungeon.greenOuterNorth0,sprites.dungeon.greenOuterNorthEast,sprites.dungeon.greenOuterEast0,sprites.dungeon.greenOuterSouthWest,sprites.dungeon.greenOuterSouthEast,sprites.dungeon.greenOuterWest0,sprites.dungeon.greenOuterSouth1,sprites.dungeon.greenOuterNorth2,sprites.dungeon.greenOuterSouth2,sprites.dungeon.greenOuterEast2,sprites.dungeon.greenOuterWest2,myTiles.tile5,myTiles.tile2,myTiles.tile4], TileScale.Sixteen);\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"startTile\":\n            case \"tile1\":return tile1;\n            case \"goalTile\":\n            case \"tile2\":return tile2;\n            case \"floorTile\":\n            case \"tile3\":return tile3;\n            case \"coinTile\":\n            case \"tile4\":return tile4;\n            case \"transparency16\":return transparency16;\n            case \"wallTile\":\n            case \"tile5\":return tile5;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
}
```

```customts
    tiles.loadMap(tiles.createMap(tilemap`level1`))
    robot.beginScreen()
```
