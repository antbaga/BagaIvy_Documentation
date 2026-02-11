# Effectors (Obstacles)

An **Effector** is a specialized function used to "push back" the ivy from specific areas. It acts as a collision or exclusion zone, allowing you to precisely control where the plant is allowed to grow—for example, to prevent leaves from penetrating window frames or doors.

*Available only in Accurate mode.*

---

## How to use Effectors

Setting up an exclusion zone is a simple three-step process:

1.  **Select the Effector object**: In the 3D View, select the mesh you want to use as an obstacle.
2.  **Select the Ivy**: Hold `Shift` and select the Ivy object.
3.  **Add**: In the **Effector panel** of the BagaIvy panel, click the **+ Add** button.

*To stop an object from acting as an effector, simply select the object and the ivy, then click the **- Remove** button.*

---

## Effector Parameters

Once an object is assigned as an effector, you can fine-tune its influence:

* **Distance**: Defines the reach of the exclusion zone around the effector object.
* **Affect Branches**: A toggle to choose if the effector should push back the entire plant structure or **only the foliage** (leaves and flowers).
* **Distance Random**: Adds organic variation to the exclusion zone so the ivy doesn't stop in a perfectly straight line.
* **Leaf Offset**: Adjusts the specific offset between the foliage and the branches within the effector's range.

---

## Pro-Tip: Using Hidden Volumes

Instead of using your complex render geometry (like a high-poly window frame) as an effector, it is often more efficient and flexible to:

1.  **Create a Simple Mesh**: Place a simple cube or primitive that covers the area you want to protect.
2.  **Set as Effector**: Assign this simple mesh as the effector for your ivy.
3.  **Hide for Render**: In the Outliner, disable the **Camera icon** for this mesh so it is hidden during the final render.

This method allows you to "sculpt" the exclusion zone precisely without being limited by the topology of your actual scene assets.

---

!!! tip "Manual Control"
    Effectors are particularly useful at the base of walls to prevent ivy from clipping into the ground, or around architectural openings where you want to keep glass surfaces clear.