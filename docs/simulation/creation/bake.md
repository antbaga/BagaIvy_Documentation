# Simulation Baking - BagaIvy V3

In BagaIvy, Simulation results are dynamic until they are **Baked**. Baking converts the procedural physics calculations into a stored data cache, ensuring your ivy stays exactly as you designed it and remains performant during playback. **You must save your file before Baking.**

!!! info "Bake Packing"
    BagaIvy Simulation is available from Blender 4.2 and newer versions.
    However, in Blender 4.2 only, there may be issues when removing bake caches. We recommend using the addon in Blender 4.3 or newer, as bake caches are stored directly inside the .blend file in those versions, which reduces potential bugs.

---

## The Two-Step Workflow

All simulation logic in BagaIvy relies on a two-stage baking process. You must complete Step 1 before you can proceed to Step 2.

* **Step 1 - Core Growth**: Creates the main skeleton of the ivy. It defines the primary path and propagation of the plant.
* **Step 2 - Foliage Growth**: Generates the volume, smaller branches, and foliage based on the skeleton created in Step 1.

!!! warning "Dependencies"
    These steps are linked. You can only bake **Step 2** if **Step 1** is already baked. If you delete the Step 1 cache, the Step 2 cache will automatically be deleted as well.

---

## Calculation Modes

Before clicking "Bake," you must choose how the addon calculates the growth :

* **Immediate Mode**: Calculates all growth steps* instantly up to your current frame (e.g., at frame 60, it calculates 60 steps* at once).
    * *Best for:* Real-time tweaking of settings. Use it at low frames (30-40) to find your look.
* **Progressive Mode**: Calculates one growth increment step* per frame as the timeline plays.
    * *Best for:* Final bakes or very large ivy setups, as it is much lighter on performance.

**Step: Here step represents a unit of growth. It is the physical increment of the plant in the simulation.*

**Pro Tip:** Dial in your settings in **Immediate** mode first, then switch to **Progressive** for the final high-frame-range bake. You can use different modes for Step 1 and Step 2.
**Progressive and Immediate produce the exact same result.**

---

## Technical: The Bake Cache

BagaIvy stores bake data in external folders. This is why **you must save your .blend file before baking**.

### Folder Structure
By default, the cache is created in the same directory as your `.blend` file in a folder named `blendcache_[your_file_name]`. Inside, you will find:

* **Modifier Subfolders**: Folders corresponding to the simulation modifiers.
* **9-digit Folders**: In Modifier Subfolders, each 9-digit folder (e.g. "314159265") represents a specific Bake Node. These contain a `blob` folder (raw data) and a `meta` folder (JSON identification).

!!! danger "Deleting Files"
    If you manually delete these folders from your hard drive, you lose your baked simulation data.

### Custom Locations & Packaging
Click the **Package** icon (folder icon) to:

1.  **Pack** the bake data directly into the `.blend` file for easier sharing.
2.  Set a **Custom Location** to save the bake data on a specific drive or server.

---

## Optimization Bake

Located in the **Optimization** menu, this third bake button is designed as final step. It can only be used once Step 1 and Step 2 are baked.

* **Still**: Freezes the ivy in its current form. The plant will not move.
* **Animation**: Calculates and freezes every frame of the viewport animation.

!!! warning "Render Note"
    If you bake for optimization while using proxies or hidden elements, the final render will show those simplified versions. Ensure you bake with full detail or delete the optimization bake before rendering.

---

## Troubleshooting & Manual Management

### Resetting a Bake
If you want to modify any settings belonging to a stage (e.g., changing Step 1 simulation parameters), you **must delete the cache** for that step and re-bake.

### Identifying the Cache
Click the **"?" icon** next to the Bake button to reveal the unique **9-digit ID** of the current bake. This helps you find the exact folder in your `blendcache` directory.
If you overwrote an existing file with a new bake cache and encounter an issue, deleting the old cache might fix the issue. I’m pretty sure someone will show up with some completely random bug that makes zero sense, so trying this might save time… meh.

### Rare Issues
If the UI indicates an ivy is baked when it isn't (or vice versa):

1.  **Force Refresh**: Toggle the visibility of the `Baga_Ivy_Simulation` geometry node modifier.
2.  **Manual Check**: Verify the bake path at the bottom of the modifier under **Manage > Bake > Bake Path** and delete the folder manually if necessary.
