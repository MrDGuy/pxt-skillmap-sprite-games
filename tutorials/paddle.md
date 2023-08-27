# Paddle!

## {Introduction @unplugged}

**Paddle** is a 2 player variation of the famous pong game!

![A ball bouncing on paddles](https://raw.githubusercontent.com/MrDGuy/pxt-skillmap-sprite-games/main/docs/static/tutorials/paddle.gif)

## {Step 1}

Begin by creating two new Sprite Kind classes.  Begin by typing @namespace followed by class SpriteKind:

Tab over the LeftPaddles = SpriteKind.create() and RightPaddles = SpriteKind.create()

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()
```


## {Step 3}

Grab a ``||function: do something||`` code and name the function create_ball()

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
```

## {Step 3}

Grab a ``||sprites:create the sprite||``` code  and drag it into the create_ball() function.  Change my_sprite to ball.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(img("""
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
"""), SpriteKind.player)
```

## {Step 4}

Click the pant palette next to the sprite create code and then click ``||assets||`` and then click on the ball asset image.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
```

## {Step 5}

Put in code to make the ``||variables(noclick):ball||`` ``||sprites:bounce on walls||``
and ``||sprites:set the velocity||`` to ``vx`` of ``100`` and ``vy`` of ``100``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
```


## {Step 6}

Use some more code to set the ``y`` of ``||variables(noclick):ball||`` to a ``||math:random||``
value between ``0`` and ``120``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)
```

## {Step 7}

Let's work on the left paddle. Create a new function, ``create_left_paddle`` Add code to ``||sprites:create a sprite||`` for
``||variables(noclick):left_paddle||`` and change the kind to ``LeftPaddles``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(img("""
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
"""), SpriteKind.LeftPaddles)
```

## {Step 8}

Click the pant palette next to the sprite create code and then click ``||assets||`` and then click on the leftPaddle asset image.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
```

## {Step 9}

Make the ``||variables(noclick):left_paddle||`` move up and down using code for the
``||controller:controller buttons||``. Use the velocity of `0` for ``||controller:vx||`` and `150`
for ``||controller:vy||``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(left_paddle, 0, 150)
```

## {Step 10}

Add code to ``||sprites:set the left||`` position of ``||variables(noclick):left_paddle||`` to ``0``.
Also, put in more code to make ``||variables(noclick):left_paddle||`` ``||sprites:stay in screen||``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(left_paddle, 0, 150)
    left_paddle.left = 0
    left_paddle.set_stay_in_screen(True)
```

## {Step 11}

Create another function, ``create_right_paddle``, for the ``||variables(noclick):right_paddle||``.
Copy all of the code from the ``create_left_paddle`` function and put it in this new
function. Change all of the ``||variables(noclick):left_paddle||`` variables in the function to
``||variables(noclick):right_paddle||``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(left_paddle, 0, 150)
    left_paddle.left = 0
    left_paddle.set_stay_in_screen(True)

def create_right_paddle():
    right_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(right_paddle, 0, 150)
    right_paddle.left = 0
    right_paddle.set_stay_in_screen(True)
```

## {Step 12}

Let's make some more changes inside of ``create_right_paddle``. Click the paint palette and then click ``||assets||`` and then choose the rightPaddle image.
Set the kind of the paddle sprite to ``RightPaddles``. Change the position setting of the paddle from ``||variables(noclick):left||`` to
``||variables(noclick):right||`` and set the value to `160`. To make this a 2 player game, replace the
``||controller:move||`` code with a multiplayer ``||controller:move player 2||`` for
``||variables(noclick):right_paddle||``. Use the same values for ``||controller:vx||`` and ``||controller:vy||``

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(left_paddle, 0, 150)
    left_paddle.left = 0
    left_paddle.set_stay_in_screen(True)

def create_right_paddle():
    right_paddle = sprites.create(assets.image("""rightPaddle"""), SpriteKind.RightPaddles)
    controller.player2.move_sprite(right_paddle, 0, 150)
    right_paddle.right = 160
    right_paddle.set_stay_in_screen(True)
```



## {Step 13}

``||functions:Call||`` all 3 functions at the bottom of the code.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(left_paddle, 0, 150)
    left_paddle.left = 0
    left_paddle.set_stay_in_screen(True)

def create_right_paddle():
    right_paddle = sprites.create(assets.image("""rightPaddle"""), SpriteKind.RightPaddles)
    controller.player2.move_sprite(right_paddle, 0, 150)
    right_paddle.right = 160
    right_paddle.set_stay_in_screen(True)

create_ball()
create_left_paddle()
create_right_paddle()
```

## {Step 14}

Add an event that runs code when ``||variables(noclick):ball||`` ``||sprites:overlaps||``
with ``||variables(noclick):left_paddle||``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(left_paddle, 0, 150)
    left_paddle.left = 0
    left_paddle.set_stay_in_screen(True)

def create_right_paddle():
    right_paddle = sprites.create(assets.image("""rightPaddle"""), SpriteKind.RightPaddles)
    controller.player2.move_sprite(right_paddle, 0, 150)
    right_paddle.right = 160
    right_paddle.set_stay_in_screen(True)

create_ball()
create_left_paddle()
create_right_paddle()

def on_on_overlap(sprite, otherSprite):
    pass
sprites.on_overlap(SpriteKind.player, SpriteKind.LeftPaddles, on_on_overlap)
```

## {Step 15}

Use the inverse of the horizontal speed (``vx``) of ``||variables(noclick):sprite||`` to simulate
the bounce on the paddle... and ``||info:change score||`` of the player by ``1``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(left_paddle, 0, 150)
    left_paddle.left = 0
    left_paddle.set_stay_in_screen(True)

def create_right_paddle():
    right_paddle = sprites.create(assets.image("""rightPaddle"""), SpriteKind.RightPaddles)
    controller.player2.move_sprite(right_paddle, 0, 150)
    right_paddle.right = 160
    right_paddle.set_stay_in_screen(True)

create_ball()
create_left_paddle()
create_right_paddle()

def on_on_overlap(sprite, otherSprite):
    sprite.vx = sprite.vx * -1
    info.change_score_by(1)
sprites.on_overlap(SpriteKind.player, SpriteKind.LeftPaddles, on_on_overlap)
```

## {Step 16}

Add another event that runs code when ``||variables(noclick):ball||`` ``||sprites:overlaps||``
with ``||variables(noclick):right_paddle||``. Invert ``vx`` the right paddle's ``vx`` and
``||info:change the score||`` of player 2 by ``1``.

```python
@namespace
class SpriteKind:
    LeftPaddles = SpriteKind.create()
    RightPaddles = SpriteKind.create()

def create_ball():
    ball = sprites.create(assets.image("""ball"""), SpriteKind.player)
    ball.set_velocity(100, 100)
    ball.set_bounce_on_wall(True)
    ball.y = randint(0, 120)

def create_left_paddle():
    left_paddle = sprites.create(assets.image("""leftPaddle"""), SpriteKind.LeftPaddles)
    controller.move_sprite(left_paddle, 0, 150)
    left_paddle.left = 0
    left_paddle.set_stay_in_screen(True)

def create_right_paddle():
    right_paddle = sprites.create(assets.image("""rightPaddle"""), SpriteKind.RightPaddles)
    controller.player2.move_sprite(right_paddle, 0, 150)
    right_paddle.right = 160
    right_paddle.set_stay_in_screen(True)

create_ball()
create_left_paddle()
create_right_paddle()

def on_overlap(sprite, otherSprite):
    sprite.vx = sprite.vx * -1
    info.change_score_by(1)
sprites.on_overlap(SpriteKind.player, SpriteKind.LeftPaddles, on_overlap)

def on_overlap2(sprite, otherSprite):
    sprite.vx = sprite.vx * -1
    info.player2.change_score_by(1)
sprites.on_overlap(SpriteKind.player, SpriteKind.RightPaddles, on_overlap2)
```


