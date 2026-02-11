# Animation

The Animation menu allows you to bring your plant to life by adding wind effect to the foliage. 

---

## Important: Growth vs. Movement

Before configuring your animation, it is essential to understand the difference between the two generation methods:

* **Procedural Method**: You **cannot** animate the "birth" or growth of the ivy (seeing it grow along the wall). This mode only animates the **movement** of the leaves and flowers (wind effect).
* **Simulation Method**: This is the only method that allows for fully animated growth from start to finish.

---

## Animation Methods

You can choose between two main methods depending on your project needs:

### 1. Continue
Provides a constant, randomized movement. This is perfect for standard scenes where you don't need the animation to loop perfectly.

### 2. Loop
Specifically designed for rendering long sequences or background loops. 

* **Loop every X frames**: Set the exact duration of the loop. The movement will seamlessly restart at the end of this frame count.

---

## Main Parameters

Adjust these settings to define the "wind" behavior:

* **Speed**: Controls how fast the leaves sway.
* **Turbidity**: Accentuates the turbulence in the foliage for a more chaotic, natural look.
* **Intensity & Random Intensity**: Defines the strength of the movement globally or per-leaf.
* **Time Offset**: Shifts the animation timing.
* **Influence Texture**: Uses a procedural texture to accentuate the intensity of the animation in specific areas.

---

## New in V3: Preserving Animation

In previous versions, converting your ivy to a mesh would lose all animation data. 

**With BagaIvy V3**, you can now use the **Apply Ivy** function to convert your generator into a static mesh while **preserving the foliage animation**. This is extremely useful for exporting your animated plants to other software or optimizing heavy scenes while keeping the animation.

---

!!! tip "Vertical vs. Horizontal"
    You can fine-tune the intensity of the movement independently on the **Vertical** and **Horizontal** axes to simulate specific wind directions.