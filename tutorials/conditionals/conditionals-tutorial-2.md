# Multiple If Statements

## Introduction @unplugged

In this tutorial you will write a for loop which will repeat 11 times and as you loop you will check whether you can move right or LEFT. The end goal is to reach the goal tile all within one for loop besides the begin_screen.
![Can Move](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-robot-control-structures/main/docs/static/robot-cs-condition-can-move-2.gif "Can Move" )

## Step One

Using the ``||robot:begin_screen||`` code, get the robot started.

```python
robot.begin_screen()
```

## Step Two

Now click the ``||loops:loops||`` category from the toolbox and drag in the ``||loops:for||`` code to line 2. Change the 4 to a 11 in the parentheses.

```python
robot.begin_screen()
for i in range(11):
    pass
```


## Step Three

Delete the pass code in the for loop and click the ``||logic:logic||`` category and pull in an ``||logic:if||`` code to where line 3 inside the loop.

```python
robot.begin_screen()
for i in range(11):
    if True:
        pass
```

## Step Four

Delete the True next to the if.  Click and drag in a ``||robot:can move||`` code to the where the True had been. Make sure that the colon is still there.

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move(""):
        pass
```

## Step Five

The "" inside the parethenses is the direction you want to check if the robot can move.  The options are forward, backward, left, and right.  ALL LOWERCASE! Type right inside the quotation marks.

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        pass
```

## Step Six

You will notice that the pass is tabbed over twice. This is important as it signifies that the code where the pass will be is inside the if condition with itself is INSIDE the loop. 

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        #tabbed over twice
        pass
```

## Step Seven

Delete the pass and make sure you write the code exactly where the pass had been.  Drag in a ``||robot:turn right||`` code where the pass had been.

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
```

## Step Eight

Next drag  in an ``||logic:if||`` code to where line 5 inside the loop but not tabbed twice so it is outside of the if robot.can_move("right"):
```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
    if True:
        pass
```

## Step Nine

Delete the True next to the if.  Click and drag in a ``||robot:can move||`` code to the where the True had been. Make sure that the colon is still there.

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move(""):
        pass
```

## Step Ten

Write left inside the quotations for the second if statement. Run your code to see if there are no errors.  

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
```

## Step Eleven

The last step is to include a ``||robot:move forward||`` after the two if statements but only inside the loop so tabbed just once.

```python
robot.begin_screen()
for i in range(11):
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    robot.move_forward()
```
```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"></block></xml>",
  "main.py": "",
  "main.ts": "\n",
  "pxt.json": "{\n    \"name\": \"Non Git Hub Robot Assets CS Skillmap Conditionals 2\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n        \"tilemaps\": \"github:microsoft/pxt-tilemaps#v1.12.0\",\n        \"Robot Extension\": \"github:MrDGuy/robot-extension#78515172c0af9925b021b75d9267df02d989c749\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\",\n        \"main.py\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.13.31\",\n        \"tag\": \"v1.13.31\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/ef3aad740700f5159eebccf721fa35d32683fcaa\",\n        \"target\": \"1.13.31\",\n        \"pxt\": \"9.1.6\"\n    },\n    \"preferredEditor\": \"pyprj\"\n}\n",
  "tilemap.g.jres": "{\n    \"tile1\": {\n        \"data\": \"hwQQABAAAAD//////////09ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPT//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"startTile\"\n    },\n    \"tile2\": {\n        \"data\": \"hwQQABAAAAD//////////4+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPj//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"goalTile\"\n    },\n    \"tile3\": {\n        \"data\": \"hwQQABAAAAD//////////x8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfH//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"floorTile\"\n    },\n    \"tile4\": {\n        \"data\": \"hwQQABAAAAD//////////393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/f//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"coinTile\"\n    },\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"tile5\": {\n        \"data\": \"hwQQABAAAAD//////////7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/v//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"wallTile\"\n    },\n    \"level1\": {\n        \"id\": \"level1\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAwYTAwMDcwMDAzMDQwNDBiMDQwNDBiMDQwNDA1MDkwZjBmMGYwZjAyMDIwMjEwMDYwOTBmMGYwZjAyMDIwZjBmMGYwNjBlMGYwZjAyMDIwZjBmMGYwZjBkMDkwZjAyMDIwZjBmMGYwZjBmMDYwOTAxMDIwZjBmMGYwZjBmMGYwNjA4MGEwYTBjMGEwYTBjMGEwYTA3MjIyMjIyMjIyMjIyMjIwMjAwMjAyMjIyMDAyMjIyMjIwMjIwMjIyMjIyMDAyMjIyMjIwMjIwMjIyMjIyMjIyMjIyMjIyMg==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"myTiles.tile1\",\n            \"myTiles.tile3\",\n            \"sprites.dungeon.greenOuterNorthWest\",\n            \"sprites.dungeon.greenOuterNorth0\",\n            \"sprites.dungeon.greenOuterNorthEast\",\n            \"sprites.dungeon.greenOuterEast0\",\n            \"sprites.dungeon.greenOuterSouthWest\",\n            \"sprites.dungeon.greenOuterSouthEast\",\n            \"sprites.dungeon.greenOuterWest0\",\n            \"sprites.dungeon.greenOuterSouth1\",\n            \"sprites.dungeon.greenOuterNorth2\",\n            \"sprites.dungeon.greenOuterSouth2\",\n            \"sprites.dungeon.greenOuterEast2\",\n            \"sprites.dungeon.greenOuterWest2\",\n            \"myTiles.tile5\",\n            \"myTiles.tile2\"\n        ],\n        \"displayName\": \"level1\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile2 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile3 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile4 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile5 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tilemap\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"level1\":\n            case \"level1\":return tiles.createTilemap(hex`0a0007000304040b04040b040405090f0f0f0f0202021006090f0f0f02020f0f0f060e0f0f02020f0f0f0f0d090f02020f0f0f0f0f060901020f0f0f0f0f0f06080a0a0c0a0a0c0a0a07`, img`\n2 2 2 2 2 2 2 2 2 2 \n2 2 2 2 2 . . . . 2 \n2 2 2 2 . . 2 2 2 2 \n2 2 2 . . 2 2 2 2 2 \n2 2 . . 2 2 2 2 2 2 \n2 . . 2 2 2 2 2 2 2 \n2 2 2 2 2 2 2 2 2 2 \n`, [myTiles.transparency16,myTiles.tile1,myTiles.tile3,sprites.dungeon.greenOuterNorthWest,sprites.dungeon.greenOuterNorth0,sprites.dungeon.greenOuterNorthEast,sprites.dungeon.greenOuterEast0,sprites.dungeon.greenOuterSouthWest,sprites.dungeon.greenOuterSouthEast,sprites.dungeon.greenOuterWest0,sprites.dungeon.greenOuterSouth1,sprites.dungeon.greenOuterNorth2,sprites.dungeon.greenOuterSouth2,sprites.dungeon.greenOuterEast2,sprites.dungeon.greenOuterWest2,myTiles.tile5,myTiles.tile2], TileScale.Sixteen);\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"startTile\":\n            case \"tile1\":return tile1;\n            case \"goalTile\":\n            case \"tile2\":return tile2;\n            case \"floorTile\":\n            case \"tile3\":return tile3;\n            case \"coinTile\":\n            case \"tile4\":return tile4;\n            case \"transparency16\":return transparency16;\n            case \"wallTile\":\n            case \"tile5\":return tile5;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
}
```

```customts
    tiles.loadMap(tiles.createMap(tilemap`level1`))
    robot.beginScreen()
    game.onUpdate(function () {
        if (robot.goalReached()) {
            music.play(music.melodyPlayable(music.powerUp), music.PlaybackMode.UntilDone)
            game.splash("You reached the goal!")
            game.reset()
        }
    })
```
