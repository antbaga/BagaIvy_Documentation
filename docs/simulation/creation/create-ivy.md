# Adding Ivy (Simulation Method)

The **Simulation** method in BagaIvy V3 allows realistic growth animations. Unlike the procedural method, this workflow involves a baking process to calculate the plant's interaction with the environment.

---

[Quick Start : Simulation YouTube Tutorial](https://youtu.be/KAdrI_W3c_4){ .md-button .md-button--primary }

---

## 1. Preparation

### Select Targets
Select one or more **Mesh** objects in your 3D Viewport. These will be your **Targets**—the surfaces upon which the ivy will grow.

### Place the Start Point
The **3D Cursor** defines the origin of the growth.

* Position the 3D Cursor on your target surface (**Shift + Right Click**).
* This creates the initial **Start Point**.
* *Note: You can move this point later or add multiple start points to create several growth origins.*

---

## 2. Configuration

In the **BagaIvy N-Panel**, set the generation method to **Simulation**.

### Auto Bake Option
* **Auto Bake Button**: When enabled, the addon will automatically run both simulation stages: **Step 1 (Core Growth)** and **Step 2 (Foliage Growth)** immediately after creation.
* **Frame Range**: To the right of the Auto Bake button, you can define the frame range for the simulation.
* **Interrupting**: If you need to stop the Auto Bake process while it is running, simply press **Escape**.

> **Tip**: All baking settings and frame ranges can be modified at any time after the ivy is created.

---

## 3. Asset Selection

Choose the source for your leaves and flowers:

* **View 3D**: Use objects already present in your current Blender scene.
* **Asset Browser**: Use assets from the official BagaIvy library or any other library (must be a mesh).
* **Using Presets**: To use a BagaIvy preset, select the **BagaIvy Generator** library, navigate to the **Presets** category, and pick a preset.

### Important Asset Rules
* **Naming Convention**: Any imported asset with the word **"flower"** in its name will be automatically assigned to the Flowers collection by the addon.
* **Library Selection**: You cannot use the "ALL" category in the Asset Browser. You must select a specific library (e.g., **BagaIvy Generator**).
* **If you’re reading this**: Thanks! There’s a hidden coupon code in the simulation node tree. *Go straight to the source!* If you’ve already done a [coupon code], send us a message ! 10 first get 90% off.

---

## 4. Add Simulation !

Click the **Add Simulation** button. BagaIvy will Import assets, create collections, and setup the simulation nodes.
By default, the addon will switch Blender to **Edit Mode**. 
*Note: You can enable or disable this automatic switch in the Addon Preferences.*

### Influencing Growth
While in Edit Mode, you can use the **Draw Tool** to create curves. These curves are used to guide and influence the path of the simulation. For more details on this, see the **Draw Control** in the Feature section.
