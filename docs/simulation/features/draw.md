# Draw Control

The **Draw Influence** system allows you to direct the growth of your ivy by proximity to manually drawn curves. By sketching paths in the viewport, you can force the simulation to follow specific artistic directions or climb certain architectural features.

This system is available in both **Step 1 - Core Growth** and **Step 2 - Foliage Growth** and follow the same curves.

---

## Entering Draw Mode

Click the **Draw Mode** button located at the bottom of the BagaIvy N-panel.
Once in Edit Mode, use the standard Blender **Draw Tool** to sketch curves directly on your target surfaces. The simulation will then use these curves as guides.

---

## Parameters

* **Guide Strength**: Defines the intensity of the influence. High values will force the ivy to follow the curve strictly, while lower values allow for more freedom.
* **Effect Distance**: The maximum distance at which a branch must be from a curve to begin being influenced by it.
* **Distance Fade**: Controls the progressive falloff of the influence. Instead of the guidance stopping abruptly at the edge of the *Effect Distance*, this parameter allows for a smooth transition as the branch moves away from the curve.

---

## Important Limitations

!!! warning "Baking and Influence"
    The **Draw Influence** settings are only available during before baking. Once a step is **Baked**, its influence is frozen. If you need to change the the influence after a bake, you must delete the cache and re-simulate.

!!! info "Step 2"
    In **Step 2 - Foliage Growth**, the secondary branches will follow the same guiding curves established for Step 1.