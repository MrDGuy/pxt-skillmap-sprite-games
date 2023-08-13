# Write a single while loop to move the robot across two tilemaps.

```template
let tile_map1 = tiles.createMap(tilemap`level1`)
let tile_map2 = tiles.createMap(tilemap`level2`)
tiles.loadMap(tile_map1)
robot.beginScreen()
tiles.connectMapById(tile_map1, tile_map2, ConnectionKind.Door1)
scene.onOverlapTile(SpriteKind.Player, assets.tile`door1`, function on_overlap_tile(sprite: Sprite, location: tiles.Location) {
    tiles.loadMap(tile_map2)
    robot.beginScreen()
})
//begin writing your code here:
```

## Introduction @unplugged

In this tutorial you will create a single while loop to give the robot all the necessary conditions to navigate any pathway to the goalTile across two tilemaps.
![While Loop](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-robot-conditional-loops/main/docs/static/while-loop-4.gif "While Loop" )

## Step One

Bring in a ``||robot:begin screen||`` code to start your code.

```python
robot.begin_screen()
```

## Step Two

Now click the ``||loops:loops||`` category from the toolbox and drag in the ``||loops:while||`` code. Make sure your tabbing is correct.

```python
robot.begin_screen()
while True:
    pass
```

## Step Three

Delete the True next to the while and drag in a ``||robot:goal reached||``.

```python
robot.begin_screen()
while robot.goal_reached():
    pass
```

## Step Four

After the ``||robot:goal reached||`` code write == False.  Notice that there are TWO EQUALS SIGNS. Make sure that the F is capitalized in False.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    pass
```
## Step Five

Delete the pass. Click in the ``||logic:logic||`` category and drag in the ``||logic:if||`` inside the while loop where the pass had been.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if True:
        pass
```

## Step Six

Delete the True next to the if.  Click and drag in a ``||robot:detect coin||`` code to the where the True had been. Make sure that the colon is still there.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        pass
```

## Step Eight

Delete the pass and make sure you write the code exactly where the pass had been.  Drag in a ``||robot:collect coin||`` code where the pass had been.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
```
## Step Nine

Delete the pass. Click in the ``||logic:logic||`` category and drag in the ``||logic:if||`` inside the while loop where the pass had been.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if True:
        pass
```

## Step Ten

Delete the True next to the if.  Click and drag in a ``||robot:can move||`` code to the where the True had been. Make sure that the colon is still there.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move(""):
        pass
```

## Step Eleven

The "" inside the parethenses is the direction you want to check if the robot can move.  The options are forward, backward, left, and right.  ALL LOWERCASE! Type right inside the quotation marks.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        pass
```

## Step Twelve

Delete the pass and make sure you write the code exactly where the pass had been.  Drag in a ``||robot:turn right||`` code where the pass had been.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        robot.turn_right()
```

## Step Thirteen

Next drag  in an ``||logic:if||`` code to where line 8 inside the loop but not tabbed twice so it is outside of the if robot.can_move("right"):

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        robot.turn_right()
    if True:
        pass
```

## Step Fourteen

Delete the True next to the if.  Click and drag in a ``||robot:can move||`` code to the where the True had been. Make sure that the colon is still there.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move(""):
        pass
```

## Step Fifteen

Write left inside the quotations for the second if statement. Include a ``||robot:turn left||`` instead of the pass. 

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
```

## Step Sixteen

Next drag  in an ``||logic:if else||`` code to where line 8 inside the loop but not tabbed twice so it is outside of the if robot.can_move("left"):

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    if True:
        pass
    else:
        pass
```

## Step Seventeen

Delete the True next to the if.  Click and drag in a ``||robot:can move||`` code to the where the True had been. Make sure that the colon is still there.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    if robot.can_move(""):
        pass
    else:
        pass
```

## Step Eighteen

Write forward inside the quotations for the second if statement. Include a ``||robot:move forward||`` instead of the pass.  

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    if robot.can_move("forward"):
        robot.move_forward()
    else:
        pass
```

## Step Nineteen

In the else, write ``||robot: turn_left||`` two times to turn the robot around.  This is the case when the robot is blocked from the front, left and right so it needs to turn back.  Run your code a watch the robot navigate on it's own.

```python
robot.begin_screen()
while robot.goal_reached() == False:
    if robot.detect_coin():
        robot.collect_coin()
    if robot.can_move("right"):
        robot.turn_right()
    if robot.can_move("left"):
        robot.turn_left()
    if robot.can_move("forward"):
        robot.move_forward()
    else:
        robot.turn_left()
        robot.turn_left()
```


```assetjson
{
  "README.md": " ",
  "assets.json": "",
  "main.blocks": "<xml xmlns=\"https://developers.google.com/blockly/xml\"><block type=\"pxt-on-start\" x=\"0\" y=\"0\"></block></xml>",
  "main.py": "tile_map1 = tiles.create_map(tilemap(\"\"\"level1\"\"\"))\ntile_map2 = tiles.create_map(tilemap(\"\"\"level2\"\"\"))\ntiles.load_map(tile_map1)\nrobot.begin_screen()\ntiles.connect_map_by_id(tile_map1, tile_map2, ConnectionKind.door1)\n\ndef on_overlap_tile(sprite, location):\n    tiles.load_map(tile_map2)\n    robot.begin_screen()\nscene.on_overlap_tile(SpriteKind.player, assets.tile(\"\"\"door1\"\"\"), on_overlap_tile)\n\nrobot.begin_screen()\nwhile robot.goal_reached() == False:\n    if robot.detect_coin():\n        robot.collect_coin()\n    if robot.can_move(\"right\"):\n        robot.turn_right()\n    if robot.can_move(\"left\"):\n        robot.turn_left()\n    if robot.can_move(\"forward\"):\n        robot.move_forward()\n    else:\n        robot.turn_left()\n        robot.turn_left()\n\ndef on_on_update():\n    if robot.goal_reached():\n        music.play(music.melody_playable(music.power_up),\n            music.PlaybackMode.UNTIL_DONE)\n        game.splash(\"You reached the goal!\")\n        game.reset()\ngame.on_update(on_on_update)\n",
  "main.ts": "let tile_map1 = tiles.createMap(tilemap`level1`)\nlet tile_map2 = tiles.createMap(tilemap`level2`)\ntiles.loadMap(tile_map1)\nrobot.beginScreen()\ntiles.connectMapById(tile_map1, tile_map2, ConnectionKind.Door1)\nscene.onOverlapTile(SpriteKind.Player, assets.tile`door1`, function on_overlap_tile(sprite: Sprite, location: tiles.Location) {\n    tiles.loadMap(tile_map2)\n    robot.beginScreen()\n})\nrobot.beginScreen()\nwhile (robot.goalReached() == false) {\n    if (robot.detectCoin()) {\n        robot.collectCoin()\n    }\n    \n    if (robot.canMove(\"right\")) {\n        robot.turnRight()\n    }\n    \n    if (robot.canMove(\"left\")) {\n        robot.turnLeft()\n    }\n    \n    if (robot.canMove(\"forward\")) {\n        robot.moveForward()\n    } else {\n        robot.turnLeft()\n        robot.turnLeft()\n    }\n    \n}\ngame.onUpdate(function on_on_update() {\n    if (robot.goalReached()) {\n        music.play(music.melodyPlayable(music.powerUp), music.PlaybackMode.UntilDone)\n        game.splash(\"You reached the goal!\")\n        game.reset()\n    }\n    \n})\n",
  "pxt.json": "{\n    \"name\": \"Non Git Hub Robot While Loops 5\",\n    \"description\": \"\",\n    \"dependencies\": {\n        \"device\": \"*\",\n        \"tilemaps\": \"github:microsoft/pxt-tilemaps#v1.12.0\",\n        \"Sprite Grid\": \"github:microsoft/arcade-grid#v1.3.0\",\n        \"Robot Extension\": \"github:MrDGuy/robot-extension#64fbb69d15070ccc00f00226305a636bbd4b9ec2\"\n    },\n    \"files\": [\n        \"main.blocks\",\n        \"main.ts\",\n        \"README.md\",\n        \"assets.json\",\n        \"tilemap.g.jres\",\n        \"tilemap.g.ts\",\n        \"main.py\"\n    ],\n    \"targetVersions\": {\n        \"branch\": \"v1.13.34\",\n        \"tag\": \"v1.13.34\",\n        \"commits\": \"https://github.com/microsoft/pxt-arcade/commits/e71dac8f868571e88292e0425471636294d16b32\",\n        \"target\": \"1.13.34\",\n        \"pxt\": \"9.1.8\"\n    },\n    \"preferredEditor\": \"pyprj\",\n    \"palette\": [\n        \"#000000\",\n        \"#FFFFFF\",\n        \"#FF2121\",\n        \"#FF93C4\",\n        \"#FF8135\",\n        \"#FFF609\",\n        \"#249CA3\",\n        \"#78DC52\",\n        \"#003FAD\",\n        \"#87F2FF\",\n        \"#8E2EC4\",\n        \"#A4839F\",\n        \"#5C406c\",\n        \"#E5CDC4\",\n        \"#91463d\",\n        \"#000000\"\n    ]\n}\n",
  "tilemap.g.jres": "{\n    \"tile1\": {\n        \"data\": \"hwQQABAAAAD//////////09ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPRPRERERERE9E9ERERERET0T0RERERERPT//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"startTile\"\n    },\n    \"tile2\": {\n        \"data\": \"hwQQABAAAAD//////////4+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPiPiIiIiIiI+I+IiIiIiIj4j4iIiIiIiPj//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"goalTile\"\n    },\n    \"tile3\": {\n        \"data\": \"hwQQABAAAAD//////////x8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfEfERERERER8R8RERERERHxHxEREREREfH//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"floorTile\"\n    },\n    \"tile4\": {\n        \"data\": \"hwQQABAAAAD//////////393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/d/d3d3d3d39393d3d3d3f3f3d3d3d3d/f//////////w==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"coinTile\"\n    },\n    \"transparency16\": {\n        \"data\": \"hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true\n    },\n    \"tile5\": {\n        \"data\": \"hwQQABAAAAB3d3fMd3d3d3d3Z8fMfHd3d3dsx3x8d3d3Z2xnd3x3d8fMx2ZmzHd+x8ZnbGZ35n7HfHfHdsfvd2xVd2xm9u7uXFV3Zmb/7u7HfHVnd8fud2fHZ2Z3d+x+Z2bHd2fMd353Z8x3d3x3d3d3Zmd8fHd3d3dnZ8Z8d3d3d3dmd3d3dw==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"myTile\"\n    },\n    \"tile6\": {\n        \"data\": \"hwQQABAAAAB3d3fMfHd3d3d3zMbMfHd3d8dmZszMd3d3x2ZnbMZ3d3dsdmdm9nx3d2x3dmf8T3fHZndnZ2b8fsdnV3fGZvzux3d3Z2fM/O7HVWdmZ/bPd2dVd2dn/Hznd3Z1Z2bG73R3xnZWZ8Z/d3fHbHbG/Hd3d3fMZsZ8d3d3d8fMzHd3dw==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"myTile0\"\n    },\n    \"tile7\": {\n        \"data\": \"hwQQABAAAAB3d2ZnZnx3d3d3Zsx2xmx3d2d2bHfMZnZ3Z3Vsd1x3ZnfMdWZnVnVmx8ZVZmx3ZcZmZ3ZnzGZmfHZVZ8bMfFdmdld1xsx8V2dmZ1ZlzGZmZsfGVWdsd2V8d8x1ZmdWdcZ3Z3dsd1x3Zndndmx3zGZ2d3d2xnbGbHd3d2ZnZnx3dw==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"myTile1\"\n    },\n    \"tile8\": {\n        \"data\": \"hwQQABAAAAB3d3d3zMx3d3d3d8zLy3x3d3d33Lu8zHd3d8zcvbzMd8fMu7zdzMx3vN27y93LzHfc3d2728vMfNvd3bvby7x8293du9u7vMvb3d2929u8y7fd3b3b27zLd9vdvb3bvMt32927vb27fHe3u7u7zbt8d3d3293My3d3d3e3y7x7dw==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"myTile2\"\n    },\n    \"tile9\": {\n        \"data\": \"hwQQABAAAABERERERER0d0QUEUFERER3RBREQURERHRERBFEREREdERERERERER0REQRQURERHREREFBREREdEREEUFEQUF0RERERBQRQXRERBFBRERBdEREQUFERER0REQRQURERHREREREREREdEREEUFERER0RERBRERERHdERERERER0dw==\",\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"tilemapTile\": true,\n        \"displayName\": \"door1\"\n    },\n    \"level3\": {\n        \"id\": \"level3\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAxMDAwMTAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMA==\",\n        \"tileset\": [\n            \"myTiles.transparency16\"\n        ],\n        \"displayName\": \"level3\"\n    },\n    \"level1\": {\n        \"id\": \"level1\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAwYTAwMDcwMDEyMDYwNjA2MDYwNjA2MDYwNjA1MDgxMDBlMTUwOTEwMGUxMTBiMDcwODBjMTQwYzBhMGMwYjE1MTEwNzA4MGMwYTBjMDkwYzBiMGEwYzA3MDgwYzE0MGYxNTBkMGEwOTBjMDcwODAxMDkwYjBhMDkwYjBiMTMwNzAyMDMwMzAzMDMwMzAzMDMwMzA0MjIyMjIyMjIyMjAyMDAwMjAwMjIwMjAyMDIwMjIwMDIwMjAyMjIyMDAyMDIwMDIyMjAwMjIyMjIyMjIwMjIyMjIyMjIyMg==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"myTiles.tile1\",\n            \"sprites.skillmap.islandTile6\",\n            \"sprites.skillmap.islandTile7\",\n            \"sprites.skillmap.islandTile8\",\n            \"sprites.skillmap.islandTile2\",\n            \"sprites.skillmap.islandTile1\",\n            \"sprites.skillmap.islandTile5\",\n            \"sprites.skillmap.islandTile3\",\n            \"myTiles.tile5\",\n            \"myTiles.tile6\",\n            \"myTiles.tile7\",\n            \"sprites.vehicle.roadVertical\",\n            \"sprites.vehicle.roadTurn4\",\n            \"sprites.vehicle.roadHorizontal\",\n            \"sprites.vehicle.roadTurn3\",\n            \"sprites.vehicle.roadTurn1\",\n            \"sprites.vehicle.roadTurn2\",\n            \"sprites.skillmap.islandTile0\",\n            \"myTiles.tile9\",\n            \"myTiles.tile8\",\n            \"myTiles.tile4\"\n        ],\n        \"displayName\": \"level1\"\n    },\n    \"level2\": {\n        \"id\": \"level2\",\n        \"mimeType\": \"application/mkcd-tilemap\",\n        \"data\": \"MTAwYTAwMDcwMDBhMGMwYzBjMGMwYzBjMGMwYzBiMGQwNDA1MDQwMzA0MTAwZjE0MGUwZDA2MDUwNjA0MDMxMTA1MTEwZTBkMTAwZjBmMDEwNjE1MDMxNTBlMGQxNTAzMDYwNTEwMTMwNjExMGUwZDEyMGYwZjBmMTMwNDAzMDIwZTA3MDgwODA4MDgwODA4MDgwODA5MjIyMjIyMjIyMjIyMjIyMjAwMjAyMjIyMjIyMDIwMDIwMDIwMjAyMDAyMjIwMjIwMjAwMjAwMDAyMjIwMjIyMjIyMjIyMg==\",\n        \"tileset\": [\n            \"myTiles.transparency16\",\n            \"myTiles.tile1\",\n            \"myTiles.tile2\",\n            \"myTiles.tile5\",\n            \"myTiles.tile6\",\n            \"myTiles.tile7\",\n            \"myTiles.tile8\",\n            \"sprites.skillmap.islandTile6\",\n            \"sprites.skillmap.islandTile7\",\n            \"sprites.skillmap.islandTile8\",\n            \"sprites.skillmap.islandTile0\",\n            \"sprites.skillmap.islandTile2\",\n            \"sprites.skillmap.islandTile1\",\n            \"sprites.skillmap.islandTile3\",\n            \"sprites.skillmap.islandTile5\",\n            \"sprites.vehicle.roadHorizontal\",\n            \"sprites.vehicle.roadTurn1\",\n            \"sprites.vehicle.roadVertical\",\n            \"sprites.vehicle.roadTurn3\",\n            \"sprites.vehicle.roadTurn4\",\n            \"sprites.vehicle.roadTurn2\",\n            \"myTiles.tile4\"\n        ],\n        \"displayName\": \"level2\"\n    },\n    \"*\": {\n        \"mimeType\": \"image/x-mkcd-f4\",\n        \"dataEncoding\": \"base64\",\n        \"namespace\": \"myTiles\"\n    }\n}",
  "tilemap.g.ts": "// Auto-generated code. Do not edit.\nnamespace myTiles {\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile1 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile2 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile3 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile4 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const transparency16 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile5 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile6 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile7 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile8 = image.ofBuffer(hex``);\n    //% fixedInstance jres blockIdentity=images._tile\n    export const tile9 = image.ofBuffer(hex``);\n\n    helpers._registerFactory(\"tilemap\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"level3\":\n            case \"level3\":return tiles.createTilemap(hex`1000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000`, img`\n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n. . . . . . . . . . . . . . . . \n`, [myTiles.transparency16], TileScale.Sixteen);\n            case \"level1\":\n            case \"level1\":return tiles.createTilemap(hex`0a0007001206060606060606060508100e1509100e110b07080c140c0a0c0b151107080c0a0c090c0b0a0c07080c140f150d0a090c070801090b0a090b0b130702030303030303030304`, img`\n2 2 2 2 2 2 2 2 2 2 \n2 . . . 2 . . . 2 2 \n2 . 2 . 2 . 2 . . 2 \n2 . 2 . 2 . 2 2 . 2 \n2 . 2 . . . 2 2 . 2 \n2 . 2 2 2 2 2 2 . 2 \n2 2 2 2 2 2 2 2 2 2 \n`, [myTiles.transparency16,myTiles.tile1,sprites.skillmap.islandTile6,sprites.skillmap.islandTile7,sprites.skillmap.islandTile8,sprites.skillmap.islandTile2,sprites.skillmap.islandTile1,sprites.skillmap.islandTile5,sprites.skillmap.islandTile3,myTiles.tile5,myTiles.tile6,myTiles.tile7,sprites.vehicle.roadVertical,sprites.vehicle.roadTurn4,sprites.vehicle.roadHorizontal,sprites.vehicle.roadTurn3,sprites.vehicle.roadTurn1,sprites.vehicle.roadTurn2,sprites.skillmap.islandTile0,myTiles.tile9,myTiles.tile8,myTiles.tile4], TileScale.Sixteen);\n            case \"level2\":\n            case \"level2\":return tiles.createTilemap(hex`0a0007000a0c0c0c0c0c0c0c0c0b0d0405040304100f140e0d06050604031105110e0d100f0f01061503150e0d15030605101306110e0d120f0f0f130403020e07080808080808080809`, img`\n2 2 2 2 2 2 2 2 2 2 \n2 2 2 2 2 2 . . . 2 \n2 2 2 2 2 2 . 2 . 2 \n2 . . . . 2 . 2 . 2 \n2 . 2 2 2 . . 2 . 2 \n2 . . . . . 2 2 . 2 \n2 2 2 2 2 2 2 2 2 2 \n`, [myTiles.transparency16,myTiles.tile1,myTiles.tile2,myTiles.tile5,myTiles.tile6,myTiles.tile7,myTiles.tile8,sprites.skillmap.islandTile6,sprites.skillmap.islandTile7,sprites.skillmap.islandTile8,sprites.skillmap.islandTile0,sprites.skillmap.islandTile2,sprites.skillmap.islandTile1,sprites.skillmap.islandTile3,sprites.skillmap.islandTile5,sprites.vehicle.roadHorizontal,sprites.vehicle.roadTurn1,sprites.vehicle.roadVertical,sprites.vehicle.roadTurn3,sprites.vehicle.roadTurn4,sprites.vehicle.roadTurn2,myTiles.tile4], TileScale.Sixteen);\n        }\n        return null;\n    })\n\n    helpers._registerFactory(\"tile\", function(name: string) {\n        switch(helpers.stringTrim(name)) {\n            case \"startTile\":\n            case \"tile1\":return tile1;\n            case \"goalTile\":\n            case \"tile2\":return tile2;\n            case \"floorTile\":\n            case \"tile3\":return tile3;\n            case \"coinTile\":\n            case \"tile4\":return tile4;\n            case \"transparency16\":return transparency16;\n            case \"myTile\":\n            case \"tile5\":return tile5;\n            case \"myTile0\":\n            case \"tile6\":return tile6;\n            case \"myTile1\":\n            case \"tile7\":return tile7;\n            case \"myTile2\":\n            case \"tile8\":return tile8;\n            case \"door1\":\n            case \"tile9\":return tile9;\n        }\n        return null;\n    })\n\n}\n// Auto-generated code. Do not edit.\n"
}
```

```customts
    game.onUpdate(function () {
        if (robot.goalReached()) {
            music.play(music.melodyPlayable(music.powerUp), music.PlaybackMode.UntilDone)
            game.splash("You reached the goal!")
            game.reset()
        }
    })
```
