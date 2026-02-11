# Adding Ivy (Procedural Method)

This guide covers the workflow for adding ivy using the **Procedural** method. This method allows for instant generation and is highly flexible.

---

## Step-by-Step Workflow

To create your first ivy, follow these steps in the **N-Panel** (BagaIvy tab):

### 1. Select the Target
Select the mesh (or multiple meshes) in your 3D view that the ivy will grow on. These are your **Target** objects.

### 2. Configure the Generator
In the addon panel, ensure the following are set:

* **Method/Generator**: Select **Procedural**.
* **Generation Mode**: Choose between **Fast**, **Accurate**, or **Precision**. You can change this later, but it's more intuitive to pick one now.
* **Select Asset Source**: 
    * **Asset Browser**: To use official presets or your own library.
    * **View 3D**: To use objects already present in your scene.

### 3. Choose your Species (Presets)
Open the **Asset Browser**, go to the **Baga Ivy Generator** library, and select a species from the **Presets** category.
> **Tip**: You can also select any object from any of your personal libraries in the Asset Browser to use it as a custom leaf/flowers..Assets with "flower" in the name will automatically be assigned in the flower part (Collection) of the ivy.

### 4. Place the Start Point
The ivy needs to know where to begin.

* Place the **3D Cursor** on the surface of your target object (**Shift + Right Click**).
* The generator will create a **Start Point** at this exact location.
* *Note: You can move this point or add more later to create multiple growth origins.*

### 5. Generate
Click the **Add New Ivy** button. Your ivy will appear instantly!

---

## Important Rules

### Switching Modes
* **Within Procedural**: You can freely switch between **Fast**, **Accurate**, and **Precision** modes at any time after creation.
* **Simulation vs Procedural**: You **cannot** switch a procedural ivy to a simulation ivy (and vice-versa). These methods use different calculation systems.

### Changing Presets
Don't worry if you change your mind! You can **change the preset** or the assets used even after the ivy has been generated. The generator will update the existing structure with the new assets.

---

## Next Step
Once your ivy is added, you can refine its shape manually using the **[Drawing Mode](procedural/creation/drawing.md)**.