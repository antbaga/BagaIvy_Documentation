# Drawing & Editing Ivy

Once you have added your ivy, you can control exactly where it spreads and how it grows by drawing directly on your target surfaces.

---

## The Drawing Workflow

When you add a new ivy, BagaIvy automatically switches to **Edit Mode**. This allows you to draw on your surface and thus define precisely where the ivy will grow.

### How it works ?
* **Curve-Based System**: The ivy's structure is built upon a curve. By drawing or editing this curve, you define the path and repartition of the ivy.
* **Surface Snapping**: The ivy is designed to automatically snap to the nearest target surface, but it will always prioritize following the path of the curve you draw.
* **Draw**: Simply use the **Draw Tool** to sketch on your mesh, and the ivy will generate along your brush strokes.

### Re-entering Draw Mode
If you have exited Edit Mode to tweak parameters and want to go back to drawing:

1. Select your Ivy object.
2. At the bottom of the **BagaIvy N-Panel**, click the **Draw Mode** button.
3. Alternatively, you can simply press **`Tab`** to enter Blender's standard Edit Mode.

---

## Pro Tips for Realistic Results

### Watch your Distance
The drawing tool requires a logical path to follow. If you start a new stroke **too far** from the existing ivy, the generator will not be able to bridge the gap. Always try to start your strokes near an existing branch to ensure a continuous growth.

### Creating Detail Branches
You can add a high level of realism by drawing short strokes **near** the main ivy structure (without overlapping it). 

* If the stroke is close enough, the generator will treat it as a secondary branch extending from the main vine.
* This is a great way to add "flyaway" branches or smaller vines that give the plant a more natural, unconstrained look.