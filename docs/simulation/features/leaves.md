# Leaves & Flowers (Simulation)

This section controls how leaves, flowers, and fruits are distributed and how they grow over time. If you are using a preset that includes fruits, these are managed directly within the **Flowers** collections and parameters.

!!! info "Prerequisite: Baking"
    Leaves and flowers will only appear in your scene once both **Step 1 - Core Growth** and **Step 2 - Foliage Growth** have been **Baked**.

---

## Assets Management
The **Assets** panel is where you manage the specific 3D models used for your foliage.

* **Asset List**: You can see all assigned assets here. To remove an asset, simply click the **X** icon next to its name.
* **Adding New Assets**:
    * **Source: View 3D**: Select an object (Mesh or Curve) in your viewport, then click **+ Add Selected**.
    * **Source: Asset Browser**: Select an asset in your Blender Asset Browser, then click **+ Add Selected**.
* **Naming Tip**: Assets with "flower" in their name are automatically sorted into the Flower list upon import.

---

## Growth (Age-based Animation)
The **Growth** panel defines the "birth" animation of each leaf or flower based on its age.

* **Logic**: To create a realistic growth effect, assets start small and aligned with the branch, then gradually scale up and tilt to their final orientation.
* **Start & End Values**: These represent **"age"**. They define when the asset begins and finishes its transition for **Angle** and **Scale**.

---

## Repartition (Density Control)
This section defines how densely the foliage is packed onto the branches.

### Repartition Leaves
* **Distance Leaves**: Sets a base distance between each leaf instance.
* **Min Distance (Key Feature)**: Set a minimum distance between leaves. This uses a dynamic calculation to prevent leaf clusters and overlapping.
    * *Note: Because this is a dynamic calculation, you must **run the animation timeline** to see the results after changing this value.*

### Repartition Flowers
* **Repartition Mode**:
    * **Start**: Flowers grow only at the base of branches (near the core).
    * **End**: Flowers grow only at the tips of branches.
    * **Every**: Flowers are distributed along the entire length.
* **Flower Probability**: Controls the chance of a flower appearing.

---

## Orientation & Scale
Fine-tune the final look and movement of your foliage.

### Orientation
* **Alignment**: Standard controls to align assets to the branch tangent, branch normal, target surface, or global Z-axis.
* **Animation Smooth Rotation**: This is a critical parameter for growth animations. It prevents "flickering" or snapping when a leaf reaches its final orientation.
    * *Usage: A value of **0.7** provides light smoothing; **0.95** provides very strong smoothing. You must **play the animation** to update this effect*
    * *This uses a dynamic calculation, you must **run the animation timeline** to see the results.*

### Scale
Defines the final size of assets based on their position on the branch:

* **Tip**: Scale of assets at the youngest part of the branch.
* **Base**: Scale of assets at the oldest part of the branch.