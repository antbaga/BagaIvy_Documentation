# Generation Modes

Baga Ivy Generator offers distinct generation algorithms, each optimized for specific situations—from covering large backgrounds to creating detailed hero assets.

Selecting the right mode is crucial for managing your scene's performance and the visual quality of the ivy.

---

## 1. Fast Mode
**Best for: Large areas, Backgrounds, Optimization.**

The **Fast** mode is designed to cover large surfaces quickly. It uses a simplified calculation method to generate ivy over extensive areas without overloading Blender.

* **Use case:** Covering a castle wall in the background, filling large spaces.
* **Performance:** High. It creates fewer calculations per branch.
* **Limitation:** Less control over individual branch behavior compared to other modes.

![Fast Mode Example](assets/fast_mode_example.jpg)
*(Placeholder: Add an image of a large wall covered in ivy here)*

---

## 2. Accurate Mode
**Best for: Small surfaces, Medium shots, Realism.**

The **Accurate** mode calculates growth with more finesse. It respects the geometry of your target object more closely and produces more natural-looking branching patterns for standard use.

* **Use case:** Ivy growing on a pillar, a window frame, or a human-scale object.
* **Performance:** Medium. Requires more calculation time than Fast mode.

![Accurate Mode Example](assets/accurate_mode_example.jpg)
*(Placeholder: Add an image of a detailed prop with ivy here)*

---

## 3. Precision Mode
**Best for: Hero assets, Foreground, Manual Control.**

The **Precision** mode offers the ultimate control. It allows you to draw branches manually, branch by branch. This is the mode to use when the ivy is right in front of the camera and needs to look perfect.

* **Use case:** Specific artistic direction, main camera focus, drawing text with ivy.
* **Feature:** Enables the **Draw Tool** (switches Blender to Edit Mode).
* **Performance:** Depends on how much you draw, but generally used for specific details.

![Precision Mode Example](assets/precision_mode_example.jpg)
*(Placeholder: Add a GIF of someone drawing ivy manually)*

---

## 4. Simulation (V3) :new:
**Best for: Physics-based growth, Hanging vines, realism.**

*Documentation for the Simulation system is currently being written.*

### Physics Settings
*(Coming soon)*

### Growth Animation
*(Coming soon)*

---

## Important Notes

!!! warning "Changing Modes"
    It is possible to switch modes **after** generating an ivy (e.g., switching from Fast to Accurate). 
    
    **However, be careful:** Changing the mode requires the addon to **re-calculate the entire generation**. On complex ivies, this may freeze Blender for a few seconds or slow down your computer.

!!! tip "Tool Tips"
    If you don't know what a specific button does, **click on the `i` (Info) icon** next to the parameter or section title. A window will appear with an explanatory text and often a video link.