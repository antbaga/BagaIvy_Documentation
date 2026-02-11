# Visibility & Optimization

The **Visibility** menu is designed to help you manage your scene's performance by hiding or simplifying elements in the 3D viewport. This is particularly useful when working on complex environments with multiple ivy objects.

---

## Viewport Visibility

You can selectively toggle the display of different parts of the plant to keep your viewport responsive:

* **Use Leaf**: Displays or hides all leaf assets in the viewport.
* **Use Flower**: Displays or hides all flower and fruit assets in the viewport.
* **Masking Trunks (Fast Mode)**: When using Fast mode, trunks can also be masked to further improve performance during navigation.

---

## Optimization & Proxies

Once your ivy is correctly positioned and configured, it is highly recommended to use the **Proxy system**. Blender Viewport doesn't like displaying too many instances...

### Proxy Options
* **Use Proxy**: Generates a simplified proxy for the **entire ivy object** (branches and foliage) within the viewport.
* **Create Leaf Proxy**: Specifically generates a proxy for **flowers and leaves only**, while keeping the branches visible.

---

## More

For background assets that do not require high visual fidelity, you can use the **Decimate** function located in the Generation Method menu. 

!!! info "Proxy"
    * **Proxies** are only for the **viewport**; the full detail returns during rendering.

!!! info "Blender being Blender"
    * If you’re using Cycles, switching to Rendered view with Overlays disabled can be faster than staying in Material Preview.

---

!!! tip "Resolution Control"
    Remember that in **Accurate Mode**, you can also set a lower **Viewport Resolution** compared to your **Render Resolution** to maintain a smooth frame rate while working.