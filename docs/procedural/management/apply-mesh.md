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

While we do not currently provide official export tools for software like **Cinema 4D, 3ds Max, or Unreal Engine**, you can still export your finalized ivy manually:

1.  **Mesh Export**: Export the geometry as usual (FBX/OBJ/USD).
2.  **Instance Data**: The small faces representing the leaves contain the necessary data to re-instance assets in other engines.
3.  **Manual Re-instancing**: In the target software, you will need to export your leaf assets separately and use the faces of the ivy mesh as a distribution source.

### Important: Leaf Indexing
The faces representing the leaves use **indices** to determine which asset from your collection goes where. 

* These indices are strictly based on the order of the assets within your leaf/flower collections.
* If you change the order of the assets or add/remove items from the collection *after* applying, the leaves will be repositioned or swapped across the faces.

---

!!! tip "Resource Management"
    Applying ivy is a resource-intensive task. For very large or complex plants, Blender may appear to freeze momentarily.