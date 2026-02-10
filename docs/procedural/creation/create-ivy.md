# Growth & Branching

The **Ivy Growth** menu gives you control over the shape, length, and behavior of the ivy's trunk and branches. It allows you to add starting points, define target objects, and fine-tune how the plant interacts with surfaces.

---

## Basic Controls

These settings are available in both **Accurate** and **Fast** modes:

* **Ivy Growth:** Reduces or increases the length of the segments that compose the trunk and branches.
* **Ivy Resolution:** Controls the resolution of the trunk mesh in the viewport and render.
* **Surface Offset:** Creates a gap between the wall and the ivy.
    * *Note:* This lifts the ivy slightly, but if set too high, the ivy may fail to generate and disappear.
* **Precision:** Sets how closely branches follow the geometry, especially near the edges of the target object.
* **Network Density:** Regulates the density of the branch network by increasing the probability of intersections.

---

## Targets & Starting Points

To control where the ivy starts and where it grows:

### Add Start Point
Adds a new starting point for the ivy at the **3D Cursor**'s location.
> **Note:** Remember to position your 3D Cursor *before* clicking this button.

### Add New Target
Allows you to add or remove objects on which the ivy can grow.
> **Warning:** The order of selection is important. When adding/removing a target, the **Ivy must always be the active object**.

!!! warning "Face Orientation"
    Ivy growth depends on the **Normals** of the target object's faces. If your ivy does not appear, check that your target's faces are facing the right way (Face Orientation).

---

## Ivy Island (Fast Mode Only)

In **Fast Mode**, to generate large quantities of ivy without slowing down the computer, the addon creates "islands" of vegetation instantiated around the main trace.

* **Display Ivy Island:** Displays only the original island (useful for debugging).
* **Wavy Growth:** Gives a random minimum and maximum scale to the selected island assets.
* **Branch Detachment:** Allows you to add or delete assets from the island system.

---

## Branch Profile (Precision Mode Only)

This menu offers precise control over the trunk's shape and shader, more detailed than in Fast/Accurate modes.

* **Branch Radius:** Defines the maximum and minimum radius of the trunk and branches.
* **Auto Radius:** Merges branches together if there are enough of them, creating a more organic trunk base.
* **UV Scale:** Adjusts the texture mapping on the trunk.