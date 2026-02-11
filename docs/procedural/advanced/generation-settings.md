# Generation Method (Accurate Mode ONLY)

The **Generation Method** menu provides access to advanced parameters that govern the underlying behavior of the ivy generation. These settings are primarily intended for experienced users.

!!! info "Exclusivity"
    This menu is exclusively available when using the **Accurate** generation mode.

---

## Advanced Parameters

Use these settings to refine the physical interaction between the ivy and your target surfaces:

### Snapping
* **Distance**: Sets the threshold at which leaves are influenced by the **Normals** of the target face.
* **Usage**: This is particularly useful for **bridges** (ivy growing between two objects). It determines the distance at which the leaves stop following the surface orientation and become "free" in space.

### Displacement
* **Noise Scale & Intensity**: Adds procedural noise to the ivy based on the surface's normality. This helps break up perfectly straight lines and adds a layer of organic randomness to the growth.

### Offset
* **Distance**: Creates a global offset between the target wall and the entire ivy structure (both foliage and branches).

---

## Optimization: Decimate

The **Decimate** function is a powerful tool for reducing the complexity of your scene.

* **Segment Length**: Increasing this value reduces the number of segments in the trunk and branches, effectively lowering the polycount.

!!! warning "Decimate vs. Proxy"
    Unlike the **Proxy system**, which only affects the viewport, the **Decimate** effect is **active during rendering**. 
    
    Because it reduces the actual geometry detail to save resources, this option is best reserved for **background ivy** where high-frequency detail is not required.