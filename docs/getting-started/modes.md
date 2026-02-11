# Generation Modes

Baga Ivy Generator V3 offers two distinct generation methods: **Simulation** and **Procedural**. Selecting the right method depends on whether you need high-end realism and animation or instant results for background scenes.

---

# Simulation Method (V3)
**Best for: Physics-based growth, Hanging vines, and Realistic growth animations.**

The Simulation method provides a highly realistic behavior where the ivy follows the surface morphology precisely and can even detach or fall under gravity. Unlike the procedural method, Simulation requires a **Baking process** to generate the final result.

### The Two-Step Workflow
To create a simulated ivy, you must proceed through two consecutive baking stages:

1.  **Step 1 - Core Growth**: This creates the main skeleton of the ivy. It defines the primary path the plant takes across the target surface.
2.  **Step 2 - Foliage Growth**: Once the core is baked, this step generates the volume and smaller branches branching out from the core structure.

This two-step approach allows you to first control the global positioning (Step 1) before managing the density and propagation of the foliage (Step 2).

### Calculation Modes
For each step, you can choose between two calculation methods:

* **Immediate**: Calculates all growth steps at once based on your current frame (e.g., at frame 60, it calculates 60 steps instantly). 
    * *Best for:* Real-time tweaking of settings. We recommend using this at a low frame (30 or 40) to find the right look.
* **Progressive**: Calculates one growth increment ("step") per frame as you run the timeline.
    * *Best for:* Large-scale ivy or final bakes. It is much lighter on performance as it only calculates one step at a time.
    * *Pro Tip:* Dial in your settings using **Immediate** mode first, then switch to **Progressive** and increase the frame range for the final bake.

> **Note on Animation**: The timing used during the setup and baking process does not lock your final animation. Once baked, you have full artistic control over the growth speed and timing of the ivy.

---

# Procedural Method (V2 & 3)

The procedural method generates ivy instantly, providing immediate feedback and extensive control over propagation without the need for baking. 

## 1. Fast Mode
**Best for: Large areas, Backgrounds, and Performance optimization.**

The **Fast** mode is designed to cover massive surfaces quickly. It uses a simplified calculation method to ensure Blender remains responsive even when generating vast amounts of vegetation.

* **Use case**: Covering distant castle walls or large environmental spaces.
* **Performance**: Extremely high; creates fewer calculations per branch.
* **Limitation**: Reduced control over individual branch behavior.

---

## 2. Accurate Mode
**Best for: Medium shots and Realistic surface adaptation.**

The **Accurate** mode calculates growth with more finesse. It respects the geometry of your target object more closely, creating realistic branching patterns suitable for most standard uses.

* **Use case**: Ivy growing on pillars, window frames, or human-scale props.
* **Performance**: Medium; requires more calculation time than Fast mode.

---

## 3. Precision Mode
**Best for: Hero assets and Manual artistic control.**

**Precision** mode offers the ultimate control by allowing you to draw branches manually. This is the ideal choice for ivy placed directly in front of the camera.

* **Use case**: Specific artistic direction or focal points.
* **Feature**: Enables the **Draw Tool** (automatically switches Blender to Edit Mode).
* **Performance**: Variable; depends on the complexity of your manual drawing.

---

## Important Notes

!!! warning "Changing Modes"
    While you can switch between Procedural modes (Fast, Accurate, Precision) **after** generating an ivy, be aware that the addon must re-calculate the entire generation. For complex setups, this may cause Blender to freeze temporarily while it processes the new data.

!!! tip "Tool Tips"
    If you are unsure about a specific setting, click the **`i` (Info) icon** next to the parameter. A window will appear with explanatory text and a link to a video tutorial.