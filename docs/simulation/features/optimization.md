# Optimization (Simulation)

The **Optimization** section is designed to handle heavy scenes by simplifying the display of ivy in the viewport and providing a final "global" bake for the entire plant.

---

## Optimization Bake

This is the final baking stage. Unlike Step 1 and Step 2 which focus on growth physics, the Optimization Bake is designed to freeze the entire result into a stable state for the final scene.

!!! info "Dependencies"
    This button can only be used once **Step 1 - Core Growth** and **Step 2 - Foliage Growth** have been successfully baked.

* **Still**: Freezes the ivy in its current form. Use this if you do not need the ivy to move during your render.
* **Animation**: Calculates and freezes every frame of the viewport animation, including wind and growth.


!!! warning "Bake Warning"
    If you perform an **Optimization Bake** while proxies are active or elements are hidden, the bake will capture those simplified versions. Ensure you bake with full detail or delete the optimization bake before starting your final render.
    
---

## Foliage Optimization

* **% Display**: Reduces the percentage of leaves or flowers visible in the viewport.
* **Display Mode**: Choose how the foliage assets are displayed:
    * **Original Mesh**: Shows the full detail of the assets.
    * **Convex Hull**: Simplifies assets into a basic shrink-wrapped shape.
    * **Bounding Box**: Represents each asset as a simple box.

---

## Branch Wireframe

To further improve performance you can toggle the display of branches:

* **Core Wireframe**: Displays the Step 1 branches as a wire.
* **Foliage Wireframe**: Displays the Step 2 branches as a wire.

---

## Important: Rendering Behavior

It is crucial to understand that the **Display Mode** and **% Display** settings are **only for viewport**. During rendering, the addon will automatically revert to **100% Display** and use the **Original Mesh**.
