# Step 2 - Foliage Growth

**Step 2** focuses on generating the secondary branch network—the smaller vines that sprout from the main "Core" established in Step 1. These branches provide the plant's volume and propagation, and they serve as the primary attachment points for all leaves and flowers.

!!! warning "Prerequisite"
    Step 2 is completely unavailable and its results will not be visible until **Step 1 - Core Growth** has been **Baked**.

---

## Workflow & Baking
The baking process for Step 2 utilizes the same **Progressive** and **Immediate** modes found in Step 1.
Once baked, the **Simulation Settings**, **Draw Influence**, and **Deformation** panels are no longer accessible.
The **Geometry** panel remains adjustable even after baking, allowing for visual tweaks without recalculating the simulation.

---

## Simulation Settings
These parameters control the physical birth and growth of the secondary branches.

* **Leaves: Display Preview**: Forces leaves to appear in the viewport before the final bake is complete. 
    * *Note: This is for preview only; foliage may flicker during animation playback, and final density is not yet applied.*
* **Branch Spacing**: Sets the distance between each secondary branch along the core structure.
* **Lifetime**: Defines the number of steps (duration) each foliage branch lives and grows.
* **Growth Start Threshold**: Determines the specific distance along the core branch where secondary growth begins.
* **Randomize**: Adds directional randomness to the growth path while ensuring branches remain attached to the target surface.
* **Surface Offset**: Adjusts the distance between the target surface and the secondary branches.
* **Surface Snap Distance**: The maximum distance at which branches will attempt to snap back to the geometry.
* **Fall Gravity**: Sets the intensity of the gravity.
* **Gravity Influence**: Controls how strictly the branches follow the direction of gravity versus their own growth path.
* **Align to Core**: Defines the initial orientation of the new branch relative to the Step 1 core (Parallel vs. Perpendicular).

---

## Deformation
Deformation acts as a post-simulation layer to add organic complexity to the branches.

* **Start & Smooth Transition**: Defines where the deformation begins relative to the branch base (0 = at the base) and how gradually it appears.
* **Wave & Twist**: Creates "corkscrew" or spiraling effects along the vines.
* **Surface Noise (Normal Based)**: Deforms the branches while keeping them relatively coplanar to the target surface faces.
* **Surface Noise (Perpendicular)**: Deforms the branches in the direction of the surface's face normals.
* **Deform (Anim)**: Adds a basic procedurally animatable deformation to give branches subtle movement.

---

## Geometry (Editable After Bake)
Adjust the visual appearance of the foliage mesh here.

* **Radius (Oldest/Youngest)**: Sets the thickness of the branches from their base to their tips.
* **Minimum Radius**: The absolute smallest thickness a branch can have.
* **Mesh Resolution & Segment Length**: Controls the density of the generated mesh.
* **Material & UV Scale**: Assigns textures and controls their mapping. Use an 'Attribute' node named **'UVs'** in your shader to access the procedural coordinates.

---

## Additional Tools
* **Draw Influence**: Follows the same curve influence logic as Step 1 to guide the foliage.
* **Cut Tool**: A specialized tool used to manually trim away small branches that may protrude or grow in unwanted areas.