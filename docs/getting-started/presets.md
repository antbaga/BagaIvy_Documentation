# Presets

Baga Ivy Generator comes with a massive library of over **70 species presets** and more than **300 individual assets** (leaves, flowers, fruits). Every preset is a pre-configured combination of these assets and growth parameters designed to mimic real-world species.

---

## Using Presets

### Adding a Preset
When adding a new ivy, you can choose a species directly from the **Asset Browser**. 
> **Important**: Ensure your Asset Browser is set to the **BagaIvy Generator** library. If it is set to "All," the import process may fail to detect the species correctly.

### Replacing a Preset
You can swap the species of an existing ivy at any time:

1.  Select your Ivy object in the viewport.
2.  In the Asset Browser, select the new preset you want to use.
3.  Click the **Replace Presets** button at the top of the BagaIvy N-panel.

!!! warning "Settings Reset"
    When you replace a preset, all current growth and foliage values are reset to the **default values** of the new species. Any custom tweaks you made to the previous preset will be lost.

---

## Customizing & Creating Presets

### Saving Custom Values
If you have fine-tuned a preset and want those settings to become the new "default" for that species:

* Click the **Save Preset Values** icon (the down-arrow icon at the very top of the panel). 
* This overrides the default values stored in the addon's internal JSON file with your current settings.

### Creating a New Preset
You can save your unique ivy setups as new presets to use in future projects:

1.  Configure your ivy (assets and parameters) exactly as you want it.
2.  Click **Create Ivy Preset**.
3.  **Preset Name**: Give your creation a unique name.
4.  **Select Preview**: Choose a preview image (we recommend rendering a small thumbnail beforehand).
5.  **Asset Library**: Select the library where the preset will be saved.


!!! info "Management"
    You can view and manage all your saved presets directly in the **Addon Preferences** tab of Blender.

---

## BagaIvy Assets

### Subdivision Modifier
Most assets included in the library have a **Subdivision Surface** modifier active by default for high-quality close-ups. 
To improve performance, you can remove or disable this modifier, especially for background vegetation.

### Simulation Mode
If you change or replace a preset while using the **Simulation method**, you must **Re-bake** the ivy, previous bake are lost.

---

## Technical Background

* **Storage**: Preset parameters are stored in **JSON files** within the addon folder. These values are mapped to the internal modifier names rather than the UI labels.
* **Preset Assets**: Assets are saved as **Collections**. The addon identifies the correct preset by matching the collection name with the preset name stored in the JSON. 