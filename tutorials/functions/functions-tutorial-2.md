# Using Multiple functions

## Introduction @unplugged

In this tutorial you will write the functions turn_around and make_tower to further practice function use in python. The end goal is to make three towers of coins before reaching the goal tile.
![Coin Tower](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-robot-control-structures/main/docs/static/robot-cs-make-tower-2.gif "Make a tower of coins" )


## Step One

Now click the ``||functions:functions||`` category from the toolbox and drag in the ``||functions:def do_somthing||`` code to line 1.

```python
def do_something():
    pass

```

## Step Two

Change the name of the function from "do_something" to "turn_around".

```python
def turn_around():
    pass

```
## Step Three

Delete the "pass" code and make sure you don't delete the tab.  If you deleted the tab just hit the tab button on line to to start the cursor tabbed.  Next drag two ``||robot:turn-right||`` codes where the pass was. Each on a new line but tabbed over.

```python
def turn_around():
    robot.turn_right()
    robot.turn_right()
```

## Step Four

Either below of above the function you just made write or drag in the ``||robot:begin_screen||``.  Have the robot the turn right. Test your code to make sure it works.

```python
robot.begin_screen()
robot.turn_right()

def turn_around():
    robot.turn_right()
    robot.turn_right()
```

## Step Five

Now click the ``||functions:functions||`` category from the toolbox and drag in the ``||functions:def do_somthing||`` code to below the turn_around function.  Rename this function "make_tower". 

```python
robot.begin_screen()
robot.turn_right()

def turn_around():
    robot.turn_right()
    robot.turn_right()

def make_tower():
    pass
```

## Step Six
Your first tower will be on the 3rd column in the tilemap.  Write the code to get the robot ready to make the first tower.  The include the code to make the coin tower.
![Coin Tower](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-robot-control-structures/main/docs/static/robot-cs-make-tower-1.gif "Make a tower of coins" )


```python
robot.begin_screen()
robot.turn_right()

def turn_around():
    robot.turn_right()
    robot.turn_right()

def make_tower():
    robot.move_forward()
    robot.move_forward()
    robot.turn_left()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
```

## Step Seven
You can use turn_around within the make_tower function to help further reduce the code. Then return to the bottom so you can call the make_tower again two more times.
![Coin Tower](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-robot-control-structures/main/docs/static/robot-cs-make-tower-2.gif "Make a tower of coins" )


```python
robot.begin_screen()
robot.turn_right()

def turn_around():
    robot.turn_right()
    robot.turn_right()

def make_tower():
    robot.move_forward()
    robot.move_forward()
    robot.turn_left()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    turn_around()
    robot.move_forward()
    robot.move_forward()
    robot.move_forward()
    robot.move_forward()
    robot.turn_left()
```

## Step Seven
Now call the make_tower function three times to make the three towers.  Lastly, write the code to get to the goalTile.
![Coin Tower](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-robot-control-structures/main/docs/static/robot-cs-make-tower-2.gif "Make a tower of coins" )


```python
robot.begin_screen()
robot.turn_right()
make_tower()
make_tower()
make_tower()
#Finish the code to get the robot to the goal.

def turn_around():
    robot.turn_right()
    robot.turn_right()

def make_tower():
    robot.move_forward()
    robot.move_forward()
    robot.turn_left()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    robot.move_forward()
    robot.place_coin()
    turn_around()
    robot.move_forward()
    robot.move_forward()
    robot.move_forward()
    robot.move_forward()
    robot.turn_left()
```


```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"></block></xml>",
  "main.py": "",
  "main.ts": "\n",
  "pxt.json": "{\n    \"name\": \"Non Git Hub Robot Assets CS Skillmap Functions 3\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n        \"tilemaps\": \"github:microsoft/pxt-tilemaps#v1.12.0\",\n        \"Robot Extension\": \"github:MrDGuy/robot-extension#78515172c0af9925b021b75d9267df02d989c749\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\",\n        \"main.py\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.13.31\",\n        \"tag\": \"v1.13.31\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/ef3aad740700f5159eebccf721fa35d32683fcaa\",\n        \"target\": \"1.13.31\",\n        \"pxt\": \"9.1.6\"\n    },\n    \"preferredEditor\": \"pyprj\"\n}\n",
  "tilemap.g.jres": "{\n    \"tile1\": {\n        \"data\": \"hwQQABAAAAD//////////09ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPT//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"startTile\"\n    },\n    \"tile2\": {\n        \"data\": \"hwQQABAAAAD//////////4+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPj//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"goalTile\"\n    },\n    \"tile3\": {\n        \"data\": \"hwQQABAAAAD//////////x8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfH//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"floorTile\"\n    },\n    \"tile4\": {\n        \"data\": \"hwQQABAAAAD//////////393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/f//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"coinTile\"\n    },\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"tile5\": {\n        \"data\": \"hwQQABAAAAD//////////7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/u/u7u7u7u7+7+7u7u7u7v7v7u7u7u7u/v//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"wallTile\"\n    },\n    \"level1\": {\n        \"id\": \"level1\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAwYTAwMDcwMDAzMDQwNDBiMDQwNDBiMDQwNDA1MDkwMjAyMDIwMjAyMDIwMjBmMDYwOTAyMDIwMjAyMDIwMjAyMDIwNjBlMDIwMjAyMDIwMjAyMDIwMjBkMDkwMjAyMDIwMjAyMDIwMjAyMDYwOTAxMDIwMjAyMDIwMjAyMDIwNjA4MGEwYTBjMGEwYTBjMGEwYTA3MjIyMjIyMjIyMjAyMDAwMDAwMjAwMjAwMDAwMDIwMDIwMDAwMDAyMDAyMDAwMDAwMjAwMjAwMDAwMDIwMjIyMjIyMjIyMg==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"myTiles.tile1\",\n            \"myTiles.tile3\",\n            \"sprites.dungeon.greenOuterNorthWest\",\n            \"sprites.dungeon.greenOuterNorth0\",\n            \"sprites.dungeon.greenOuterNorthEast\",\n            \"sprites.dungeon.greenOuterEast0\",\n            \"sprites.dungeon.greenOuterSouthWest\",\n            \"sprites.dungeon.greenOuterSouthEast\",\n            \"sprites.dungeon.greenOuterWest0\",\n            \"sprites.dungeon.greenOuterSouth1\",\n            \"sprites.dungeon.greenOuterNorth2\",\n            \"sprites.dungeon.greenOuterSouth2\",\n            \"sprites.dungeon.greenOuterEast2\",\n            \"sprites.dungeon.greenOuterWest2\",\n            \"myTiles.tile2\"\n        ],\n        \"displayName\": \"level1\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile2 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile3 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile4 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile5 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tilemap\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"level1\":\n            case \"level1\":return tiles.createTilemap(hex`0a0007000304040b04040b04040509020202020202020f06090202020202020202060e02020202020202020d0902020202020202020609010202020202020206080a0a0c0a0a0c0a0a07`, img`\n2 2 2 2 2 2 2 2 2 2 \n2 . . . . . . . . 2 \n2 . . . . . . . . 2 \n2 . . . . . . . . 2 \n2 . . . . . . . . 2 \n2 . . . . . . . . 2 \n2 2 2 2 2 2 2 2 2 2 \n`, [myTiles.transparency16,myTiles.tile1,myTiles.tile3,sprites.dungeon.greenOuterNorthWest,sprites.dungeon.greenOuterNorth0,sprites.dungeon.greenOuterNorthEast,sprites.dungeon.greenOuterEast0,sprites.dungeon.greenOuterSouthWest,sprites.dungeon.greenOuterSouthEast,sprites.dungeon.greenOuterWest0,sprites.dungeon.greenOuterSouth1,sprites.dungeon.greenOuterNorth2,sprites.dungeon.greenOuterSouth2,sprites.dungeon.greenOuterEast2,sprites.dungeon.greenOuterWest2,myTiles.tile2], TileScale.Sixteen);\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"startTile\":\n            case \"tile1\":return tile1;\n            case \"goalTile\":\n            case \"tile2\":return tile2;\n            case \"floorTile\":\n            case \"tile3\":return tile3;\n            case \"coinTile\":\n            case \"tile4\":return tile4;\n            case \"transparency16\":return transparency16;\n            case \"wallTile\":\n            case \"tile5\":return tile5;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
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
