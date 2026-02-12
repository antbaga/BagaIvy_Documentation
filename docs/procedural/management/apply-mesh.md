# Finalizing: Apply & Delete

Once you have finished configuring and drawing your plant, you may need to convert it into a static mesh for editing or export. This panel provides the tools to finalize or safely remove your ivy.

---

## Deleting Ivy

When you want to remove an ivy object from your scene, it is **strongly recommended** to use the **Delete** button in the BagaIvy N-Panel instead of the standard Blender delete key (`X` or `Delete`).

* **Why**: Deleting via the addon panel ensures that all associated collections (Targets, Start Points, Assets) are properly cleaned up.
* **Avoid "Ghost" Data**: Manual deletion often leaves empty collections or hidden data-blocks in your file.

---

## Apply Ivy (Convert to Mesh)

The **Apply Ivy** function transforms the ivy into a standard Blender mesh. 

!!! warning "Irreversible Process"
    Once you apply the ivy, you lose all procedural controls and the ability to use the Draw tool.

### How it Works:
* **Branches**: The trunk and branches are converted into real, editable geometry. You can enter Edit Mode to manually deform, sculpt, or delete specific segments.
* **Leaves & Flowers**: These are converted into optimized **faces**. Each face is assigned specific attributes that allow Blender to treat them as instances, keeping the scene highly optimized.
* **Animation (V3)**: Unlike previous versions, BagaIvy V3 **preserves foliage animation** after the apply process. Your leaves will continue to move even as a static mesh.

---

## Exporting to Other Software ?

There are no export features for external software at the moment.

---

!!! tip "Resource Management"
    Applying ivy is a resource-intensive task. For very large or complex plants, Blender may appear to freeze momentarily.