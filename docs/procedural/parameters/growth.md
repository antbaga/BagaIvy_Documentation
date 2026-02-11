# Ivy Growth & Parameters

The **Ivy Growth** section is where you define how the plant spreads, its density, and its overall morphology. 

!!! warning "Mode Specificity"
    Parameters in the Growth menu vary significantly depending on whether you are using **Fast**, **Accurate**, or **Precision** mode. Because each mode uses a different generation algorithm, **settings are not synchronized** when you switch between them.

---

## 1. Fast Mode Parameters
**Best for: Backgrounds and large surfaces.**

In **Fast Mode**, the generator creates a small initial "piece" of ivy—called an **Island**—and replicates it across the drawn areas to maximize performance.

### Main Settings
* **Ivy Density**: Controls the global amount of vegetation (Leaves, Flowers and Fruits).
* **Ivy Propagation**: Defines how far the ivy spreads from curvz.
* **Angle Target Edge**: Adjusts how the ivy embraces the shape of the geometry as it unfurls.
* **Ivy Bridge**: Settings to control how ivy spans gaps between different surfaces.

### Ivy Island (Exclusive to Fast Mode)
This sub-menu allows you to modify the individual "piece" used for replication:

* **Display Only Ivy Island**: Isolate the original island to see exactly what is being instantiated.
* **Branch Detachment**: Add or remove assets specifically from the island structure.
* **Wavy Growth**: Adds random variation to the scale and shape of the island assets.
* **Branch Radius**: Defines the minimum and maximum thickness of the island's branches.

---

## 2. Accurate Mode Parameters
**Best for: Medium to close-up shots requiring realistic branching.**

This mode generates a true mesh of branches with *"realistic"* ramifications (splitting branches).

* **Ivy Growth**: Increases or reduces the length of the individual segments that compose the trunk and branches.
* **Network Density**: Regulates the density of the branch network by increasing the probability of branch intersections.
* **Precision**: Sets how closely the branches follow the target geometry, especially near the edges.
* **Surface Offset**: Creates a slight gap between the wall and the ivy. 
    * *Warning: If set too high, the ivy may fail to generate.*

---

## 3. Precision Mode Parameters
**Best for: Hero assets and foreground elements.**

In **Precision Mode**, you draw branch by branch. You have total manual control, but the generator does **not** produce automatic ramifications (secondary branches).

* **Curve-Based Control**: You can manually adjust the **Radius** (thickness) and **Tilt** (rotation) of each branch using Blender's curve tools.
* **Branch Profile & Shader**:
    * **Auto Radius**: Automatically merges branches together for a more organic look.
    * **UV Scale**: Adjusts the scale of the procedural bark texture.
    * **Material/Color**: Direct access to customize the bark's color, brightness, and material assignment.

---

## Common Settings (All Modes)

### Targets & Origins
* **Target (+/-)**: Add or remove surfaces the ivy is allowed to grow on.
    * *Note: The Ivy must be the active object when adding a new target.*
* **Add Start Point to 3D Cursor**: Adds a new growth origin at your 3D cursor's position.

### Performance & Visibility
* **Ivy Resolution**: Controls the mesh detail. You can set different values for the **Viewport** (lower for speed) and **Render** (higher for quality).
* **Decimate**: Merges branches together to reduce polycount at the expense of realism (best for background assets).

!!! info "Normals Matter"
    Ivy growth depends on the **Face Orientation (Normals)** of your target objects. If your ivy is growing inside a wall or not appearing, check that your target's faces are pointing outward.