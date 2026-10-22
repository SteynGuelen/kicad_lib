# KiCad libraries

Custom symbols, footprints, 3D models, drawing sheets, and reusable design blocks by Steyn Guelen.

## Requirements

Use KiCad 10 or newer for the complete collection. Some files were saved with KiCad 10; older versions may not open all assets. Git is optional if you download a ZIP instead.

## Install

1. Clone this repository into a permanent location:

   ```sh
   git clone https://github.com/SteynGuelen/kicad_lib.git
   ```

   Alternatively, choose **Code → Download ZIP** on GitHub and extract it.

2. In KiCad, open **Preferences → Configure Paths**. Add `KICAD_LIB` pointing to the absolute path of your `kicad_lib` folder.

3. Open **Preferences → Manage Symbol Libraries**. Select **Global Libraries** to make the symbols available to all projects, or **Project Specific Libraries** for the current project. Click **Add existing library** and select the `.kicad_sym` files inside `symbols/`.

4. Open **Preferences → Manage Footprint Libraries**. Add the `.pretty` directories inside `footprints/` as existing libraries. Select directories, rather than the individual `.kicad_mod` files. Keep the directory names as library nicknames, for example `integrated_circuits` and `standards`.

You can use paths such as `${KICAD_LIB}/symbols/integrated_circuits.kicad_sym` and `${KICAD_LIB}/footprints/integrated_circuits.pretty` in the library tables.

## 3D models and footprint assignments

Some footprints contain embedded 3D models; others reference external STEP files. Some existing references still use the original author’s absolute Windows paths. If a model is missing, open the footprint’s properties in the Footprint Editor, select **3D Models**, and replace its path with the matching file under `${KICAD_LIB}/3dmodels/` or the footprint library’s `packages3d/` directory.

Some symbols also contain older or differently capitalized footprint library nicknames. If a footprint assignment cannot be resolved, use **Assign Footprints** in the Schematic Editor to select the corresponding footprint from your installed libraries.

The corrected library name is `integrated_circuits`. Existing projects using the former spelling `intergrated_circuits` need their library paths and assignments updated.

## Other assets

- `design_blocks/`: reusable KiCad design-block libraries. Add the `.kicad_blocks` directory through KiCad’s design-block library manager.
- `sheets/`: custom `.kicad_wks` drawing sheets. Select one through the schematic or PCB editor’s **Page Settings** dialog.
- `3dmodels/`: external STEP models for footprint previews.

## Update

If installed using Git, run this inside the cloned folder:

```sh
git pull --ff-only
```

For a ZIP installation, download and extract the latest version into the same location. Keep any personal edits backed up before replacing files.

See the [official KiCad documentation](https://docs.kicad.org/) for library management and path configuration.
