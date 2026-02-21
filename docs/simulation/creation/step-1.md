# Step 1 - Core Growth

**Step 1** is the skeletal stage of your ivy. It defines the main structure: where the plant goes, how far it spreads, how often it branches, and when it starts to fall away from the surface.

The simulation works on a generational logic: a main branch grows and spawns new offshoots, which in turn grow and spawn their own branches. 

!!! warning "Exponential Growth"
    Be careful with high spawn rates and long lifetimes. Because branches spawn new branches which then spawn more, the simulation can quickly become exponential and impact performance.

---

## Simulation Settings
These parameters define the physical behavior of the ivy during the growth calculation.

* **Lifetime**: Defines how long each branch lives (in iterations) before it stops growing or disappears.
* **Growth Step**: Sets the speed and distance of growth per iteration.
* **Detach Age**: The branch age (in iterations) after which it stops clinging to surfaces and begins to fall due to gravity.
* **Gravity Strength**: The strength of the downward force that pulls branches down once they are detached or airborne.
* **Detection Radius**: The maximum distance at which a branch can detect and attach to nearby target surfaces.
* **Spawn Rate**: Controls how frequently new branches are created per iteration.
* **Max Spawn Age**: The maximum branch age where new offshoots can still sprout; beyond this limit, no new branches form from that specific segment.
* **Branch Angle**: The angle between the main parent branch and a newly created offshoot.

---

## Draw Influence & Deformation
* **Draw Influence**: You can use curves to manually guide the path of the ivy. For detailed control, refer to the **Draw Control** in the Features section.
* **Deformation**: Adds organic noise and smoothing to the generated curves to make them look more natural.

!!! info "Post-Bake Restrictions"
    Once the simulation is **Baked**, the **Simulation Settings**, **Draw Influence** and **Deformation** panels are locked and no longer available. The bake process freezes the underlying curves.

---

## Geometry
Unlike the simulation settings, the **Geometry** panel remains fully adjustable even after the ivy is baked. This allows you to fine-tune the visual mesh without re-simulating.

* **Radius (Start/End)**: Sets the thickness of the branches at their origin and tips.
* **Minimum Radius**: Ensures branches do not become thinner than this value.
* **Step Reduction**: Gradually reduces the radius as the branch grows.
* **Resolution & Segment Length**: Controls the density of the mesh topology.
* **Material**: Assign your bark or stem material here.
* **UV Scale**: Adjusts the tiling of the trunk texture. Remember to use an 'Attribute' node and use **'UVs'** aas attribute name in your shader.

## Fix Sharp Angles

If the ivy has sharp edges or hard breaks, go to **Geometry** (sub-panel).

* Increase **Smooth Angles** to `3` or higher
* Reduce **Segment Length** to `0.01`

---

## Target Management
You can modify which objects the ivy interacts with using the **Target** panel.

* **Add selection to Targets**: Includes the currently selected objects in the ivy's Target Collection.
* **Remove selection from Targets**: Excludes selected objects so the ivy will no longer grow on them.