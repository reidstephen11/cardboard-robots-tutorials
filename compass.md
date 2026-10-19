# Sensor Lab: Compass

### @diffs true

## Introduction @unplugged
The **compass** tells you which way the micro:bit is facing, in degrees.

**0** is north, **90** is east, **180** is south and **270** is west.

## Step 1 — Show the heading
From **Basic**, drag ``||basic:show number||`` into the ``||basic:forever||`` block.
From **Input**, drag ``||input:compass heading (°)||`` into the gap.

```blocks
basic.forever(function () {
    basic.showNumber(input.compassHeading())
})
```

## Step 2 — Test it
On the simulator, the gold logo turns into a compass needle, with the heading beside it. Drag the needle round: the number changes as it turns.

Then click **Download**. The first time, the real micro:bit says **TILT TO FILL SCREEN**. Tilt it slowly in every direction until all the LEDs are lit: that sets up the compass.

## Challenge — North finder
Show **N** only when the micro:bit faces within 45 degrees of north (either side). Otherwise, clear the screen.

This one uses an **if** block, which Lesson 3 teaches.

```ghost
basic.forever(function () {
    if (input.compassHeading() < 45 || input.compassHeading() > 315) {
        basic.showString("N")
    } else {
        basic.clearScreen()
    }
})
```

**Hint:** Use ``||logic:if then else||`` from **Logic**, with a comparison like ``||logic:0 < 0||``. North is at both ends of the numbers (near 0 and near 359), so you'll need ``||logic:or||``.


## Finished @showdialog
Nice work. You've tried every sensor. Go back to the QLearn page.
