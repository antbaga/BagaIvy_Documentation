# Foliage & Trunk Parameters

This section covers the customization of leaves, flowers (including fruits), and the main trunk/branch structure. 

!!! info "Fruits Management"
    In Baga Ivy Generator, **Fruits** are managed within the **Flowers** menu. Presets that include fruits use the same distribution and alignment logic as flowers.

---

## Leaves

The Leaves menu allows you to set parameters related to density, orientation, and scale. Note that the available settings change depending on your generation mode.

### Fast & Accurate Modes
* **Leaves Density**: Regulates the overall density of the foliage.
* **Distance Min**: Suppresses leaves that are too close to each other to prevent overlapping and limit polycount.
* **Leaves Random Scale**: Sets a minimum and maximum random scale for the leaf assets.
* **Alternating & Random Rotation**: Adjusts the distribution and orientation of leaves along the branches.
* **Inclination**: Controls the leaf angle relative to the branch.
* **Offset**: Creates a distance between the leaf and the branch surface.

### Precision Mode
* **Density Radius Based**: Automatically adjusts leaf density based on the thickness of the branch.
* **Alignments**: Specialized toggles to align leaves with the **Branch normal**, **Global Ground (Z-axis)**, or the **Target surface**.
* **Scale & Local Offset**: Fine-tune the scale and position of assets along the local axis of the branch.

---

## Flowers & Fruits

The Flowers menu functions similarly to the Leaves menu and is used to manage both flowers and fruit assets.

### Fast & Accurate Modes
* **Flower Probability**: Controls the chance of a flower/fruit appearing at any given point.
* **Random Scale**: Randomizes the size of the flower/fruit assets.
* **Rotation**: Adjusts the local tilt. For falling assets like wisteria or heavy fruits, it is often necessary to orient them towards the **Global Z-axis**.

### Precision Mode
* **Animation**: Specifically available in Precision mode to add dynamic movement to flowers.
* **Advanced Alignment**: Just like leaves, flowers can be aligned to the branch, ground, or target surface for perfect positioning.

---

## Trunk & Branches

This menu defines the diameter of the trunk and branches, as well as their visual appearance through materials.

### Main Parameters (Fast & Accurate)
* **Trunk & Branch Radius**: Independently set the thickness of the main trunk and the secondary branches.
* **Procedural Bark Material**: By default, branches use a procedural shader where you can adjust **Luminosity, Contrast, Saturation, and Tint Intensity** directly from the N-Panel.

### Using Custom Materials
If you wish to use your own textures for the trunk:

1.  Assign your material in the **Material** slot.
2.  In your Shader Editor, use an **Attribute node**.
3.  **Important**: Set the attribute name to **`UVs`** (case sensitive) and connect it to a Mapping node to ensure the textures wrap correctly around the generated branches.

### Precision Mode: Branch Profile
* **Auto Radius**: Merges branches together where they intersect, creating a more organic, flared base for the trunk.
* **UV Scale**: Quickly adjust the tiling of the bark texture without entering the Shader Editor.

---

!!! tip "Adding/Removing Assets"
    You can add your own custom leaf or flower objects by selecting **"View 3D"** as the source, selecting your object, then clicking the **+ Add Leaf/Flower** button while the ivy is selected.