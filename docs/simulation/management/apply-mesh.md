# Apply & Export

Finalizing your ivy allows you to convert it into a mesh. This is essential if you want to edit it or exporting your work to other 3D software.

---

## Apply Ivy (Convert to Mesh)

At the bottom of the panel, there’s an Apply button.

!!! danger "Irreversible Process"
    Once you apply the ivy, you lose all controls.

### How it Works
* **Branches**: The trunk and branches are converted into real editable geometry. You can enter **Edit Mode** to manually deform, sculpt, or delete specific segments.
* **Leaves & Flowers**: These are converted into **faces**. Each face stores the **leaf** attributes (instance index and transform) that allow them to be restored to the exact same position, keeping the scene optimized (otherwise you can end up with a million-poly mesh).
* **Animation (V3)**: Unlike previous versions, BagaIvy V3 **preserves foliage animation** after the apply process. Your leaves will continue to move even as a static mesh.

!!! info "Growth Animation"
    Growth animation is lost when applied !

---

## Exporting to Other Software

There are no export features for external software at the moment.