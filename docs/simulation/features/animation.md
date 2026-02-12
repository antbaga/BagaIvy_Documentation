# Animation (Simulation)

The Animation section allows you to manage the growth animation of your ivy, branch Deformation and winds. While procedural ivy is limited to leaf movement, simulation mode enables full growth animation.

---

## Growth

This section handles the progression of the ivy from birth to full growth.

### Growth Methods
You can choose how the growth is triggered:

* **Scene Time**: The growth is synchronized with the baked frame range. 
    * **Time Scale**: Allows you to speed up or slow down the overall growth speed.
    * **Time Offset**: Shifts the starting frame of the animation.
* **Manual**: Replaces timeline synchronization with a simple **0 to 1 slider**. 
    * **0** represents the very start of the growth.
    * **1** represents the fully grown ivy.
    * This slider is fully animatable via keyframes for precise control.

### Growth Parameters
* **Time Profile**: Used to edit the velocity curve of the growth (e.g., fast at the start, slow at the end, loops, ...).
* **Branch Growth Mode**: A factor that balances two growth behaviors:
    * **At 0**: All branches continue to grow slowly until the entire baked frame range has passed (older branches slow down as they age).
    * **At 1**: Branches grow at a constant speed and finish their growth much earlier than the total animation length.
    * **Tip**: A value of **0.8** is recommended for the most natural-looking results.
* **Deform Animation**: Adds an organic offset/displacement effect to the branches during their growth phase.

---

## Wind

The Wind panel is used to animate leaf movement. These settings are identical to the Procedural mode.

### Wind Methods
* **Continue**: Provides a constant, randomized wind effect.
* **Loop**: Designed for seamless animation loops in long sequences.

### Parameters
* **Speed & Turbidity**: Sets the basic velocity and chaos of the swaying foliage.
* **Vertical & Horizontal Influence**: Fine-tune the movement independently for each axis.
    * **Intensity**: The strength of the wind on that specific axis.
    * **Time Offset**: Offsets the animation between different leaves so they don't move in perfect unison.
    * **Influence Texture**: Uses a procedural texture to drive the movement's intensity locally.