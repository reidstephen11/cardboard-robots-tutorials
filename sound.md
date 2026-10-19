# Sensor Lab: Sound

### @diffs true

## Introduction @unplugged
The **microphone** hears sound. It's the tiny hole on the front, next to the gold logo.

Build a robot that jumps at a loud noise and falls asleep when it's quiet.

## Step 1 — React to a loud sound
From **Input**, drag ``||input:on loud sound||`` into the workspace.
From **Basic**, put ``||basic:show icon||`` inside it and pick the **surprised** face.

```blocks
input.onSound(DetectedSound.Loud, function () {
    basic.showIcon(IconNames.Surprised)
})
```

## Step 2 — Fall asleep when it's quiet
Drag in a second ``||input:on loud sound||`` and change **loud** to **quiet**.
Put a ``||basic:show icon||`` inside it with the **asleep** face.

```blocks
input.onSound(DetectedSound.Loud, function () {
    basic.showIcon(IconNames.Surprised)
})
input.onSound(DetectedSound.Quiet, function () {
    basic.showIcon(IconNames.Asleep)
})
```

## Step 3 — Test it
On the simulator, drag the **microphone** bar up high, then right down low. The face should change each time.

Then click **Download**, and try a clap and then silence.

## Challenge — Too jumpy?
Your robot might react to every little noise. Make it react **only to a clap**, not to talking.

Find the number that works in your room by testing.

```ghost
input.setSoundThreshold(SoundThreshold.Loud, 128)
```

#### ~ tutorialhint
In **Input**, click **more**. Find ``||input:set loud sound threshold||`` and put it in ``||basic:on start||``. Try **200**, test it, then change the number.


## Finished @showdialog
Nice work. Go back to the QLearn page and pick your next sensor.
