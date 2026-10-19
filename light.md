# Sensor Lab: Light

### @diffs true

## Introduction @unplugged
The LEDs on the front can **sense light** as well as show it.

Build a light meter: the brighter it is, the more LEDs light up.

## Step 1 — Draw a bar graph
From **Led**, drag ``||led:plot bar graph of||`` into the ``||basic:forever||`` block.

```blocks
basic.forever(function () {
    led.plotBarGraph(0, 255)
})
```

## Step 2 — Measure the light
From **Input**, drag ``||input:light level||`` into the first gap, where the **0** is.
Leave **up to** at **255**, the brightest light level.

```blocks
basic.forever(function () {
    led.plotBarGraph(input.lightLevel(), 255)
})
```

## Step 3 — Test it
On the simulator, drag the **sun** up and down. More light, more LEDs.

Then click **Download**, and cover the LEDs with your hand.

## Challenge — Find your threshold
Swap the bar graph for ``||basic:show number||`` so the micro:bit shows the light level as a number.

Write down the number in normal light, then with your hand over the LEDs. Pick a number halfway between them: that's your **threshold**. Lesson 3 uses it.

```ghost
basic.showNumber(input.lightLevel())
```

**Hint:** ``||basic:show number||`` is in **Basic**. Drag ``||input:light level||`` out of the bar graph and into show number, then delete the bar graph.


## Finished @showdialog
Nice work. Go back to the QLearn page and pick your next sensor.
