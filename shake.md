# Sensor Lab: Shake

### @diffs true

## Introduction @unplugged
The **accelerometer** feels movement: a shake, a tilt, and which way up the micro:bit is.

Build a robot that gets a fright when it's shaken, then calms down.

## Step 1 — React to a shake
From **Input**, drag ``||input:on shake||`` into the workspace.
From **Basic**, put ``||basic:show icon||`` inside it and pick the **surprised** face.

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Surprised)
})
```

## Step 2 — Calm down
Under the face, add ``||basic:pause (ms)||`` and set it to **1000** (one second).
Then add another ``||basic:show icon||`` with the **happy** face.

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Surprised)
    basic.pause(1000)
    basic.showIcon(IconNames.Happy)
})
```

## Step 3 — Test it
Click **SHAKE** on the simulator. You should see the surprised face, then the happy face a second later.

Then click **Download**, and shake the real micro:bit.

## Challenge — Put me down!
Make the robot **sad** when it's turned face down, and **happy** again when it's turned face up.

Test this one on the real micro:bit: the simulator can only shake.

```ghost
input.onGesture(Gesture.ScreenDown, function () {
    basic.showIcon(IconNames.Sad)
})
```

**Hint:** Drag in another ``||input:on shake||`` and click its dropdown. **screen down** and **screen up** are in the list.


## Finished @showdialog
Nice work. Go back to the QLearn page and pick your next sensor.
