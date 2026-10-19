# Sensor Lab: Touch logo

### @diffs true

## Introduction @unplugged
The gold **logo** on the front is a touch sensor. It feels your finger.

Build a robot that giggles when you give it a pat.

## Step 1 — React to a touch
From **Input**, drag ``||input:on logo pressed||`` into the workspace.
From **Basic**, put ``||basic:show icon||`` inside it and pick the **happy** face.

```blocks
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
    basic.showIcon(IconNames.Happy)
})
```

## Step 2 — Add a giggle
From **Music**, add ``||music:play giggle until done||`` under the face. If it shows a different sound, click the dropdown and choose **giggle**.

```blocks
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
    basic.showIcon(IconNames.Happy)
    music.play(music.builtinPlayableSoundEffect(soundExpression.giggle), music.PlaybackMode.UntilDone)
})
```

## Step 3 — Test it
Click the gold **logo** on the simulator. You should see the face and hear a giggle.

Then click **Download**, and tap the real logo.

## Challenge — Pat or poke?
A quick tap is a pat. Make **holding your finger on the logo** give a different reaction, like an angry face and a sad sound.

To test it in the simulator, hold the mouse button down on the logo for two seconds.

```ghost
input.onLogoEvent(TouchButtonEvent.LongPressed, function () {
    basic.showIcon(IconNames.Angry)
    music.play(music.builtinPlayableSoundEffect(soundExpression.sad), music.PlaybackMode.UntilDone)
})
```

**Hint:** Drag in another ``||input:on logo pressed||`` and change **pressed** to **long pressed**.


## Finished @showdialog
Nice work. Go back to the QLearn page and pick your next sensor.
