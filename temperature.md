# Sensor Lab: Temperature

### @diffs true

## Introduction @unplugged
The micro:bit measures **temperature** in °C, with a sensor inside its processor chip on the back.

Build a thermometer that shows the temperature when you press A.

## Step 1 — Show the temperature
From **Input**, drag ``||input:on button A pressed||`` into the workspace.
From **Basic**, put ``||basic:show number||`` inside it. Then drag ``||input:temperature (°C)||`` into the gap.

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(input.temperature())
})
```

## Step 2 — Add the unit
Under it, add ``||basic:show string||`` and type **C**, so people know it's degrees Celsius.

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(input.temperature())
    basic.showString("C")
})
```

## Step 3 — Test it
On the simulator, drag the **thermometer** bar, then press **A**.

Then click **Download**, and press A on the real micro:bit.

## Challenge — Hot hands
Make the temperature show **all the time**, not only when you press A.

Then hold the real micro:bit in your cupped hands for 30 seconds. How many degrees does it go up?

```ghost
basic.forever(function () {
    basic.showNumber(input.temperature())
})
```

**Hint:** Use ``||basic:forever||`` from **Basic** instead of on button A pressed. Blocks inside forever run again and again.


## Finished @showdialog
Nice work. Go back to the QLearn page and pick your next sensor.
