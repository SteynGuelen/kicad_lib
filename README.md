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

2. Open **Preferences → Manage Symbol Libraries**. Select **Global Libraries** to make the symbols available to all projects, or **Project Specific Libraries** for the current project. Click **Add existing library** and select the `.kicad_sym` files inside `symbols/`.

3. Open **Preferences → Manage Footprint Libraries**. Add the `.pretty` directories inside `footprints/` as existing libraries. Select directories, rather than the individual `.kicad_mod` files. Keep the directory names as library nicknames, for example `integrated_circuits` and `standards`.

## Install the MPlab project template

The `templates/MPlab/` folder contains the MPlab project template, including its schematics, PCB, embedded drawing sheets, and template preview.

1. In KiCad, open **Preferences → Configure Paths** and find `KICAD_USER_TEMPLATE_DIR`. This is your user template folder.
2. Copy the entire `templates/MPlab/` folder into that folder. The resulting layout should be `<user template folder>/MPlab/meta/info.html`, with the project files directly inside `MPlab/`.

   For example, on this Mac the destination is:

   ```text
   /Users/steyn/Documents/KiCad/10.0/template/MPlab/
   ```

   If a copy already exists, back it up before replacing it.

3. In KiCad’s Project Manager, choose **File → New Project from Template**, open **User Templates**, and select **MPLab**. Choose a new project name and location to create your own project from the template.

See [KiCad’s template documentation](https://docs.kicad.org/10.0/en/kicad/kicad.pdf) for details about user template locations.

## Other assets

- `design_blocks/`: reusable KiCad design-block libraries. Add the `.kicad_blocks` directory through KiCad’s design-block library manager.
- `sheets/`: custom `.kicad_wks` drawing sheets. Select one through the schematic or PCB editor’s **Page Settings** dialog.

## Update

If installed using Git, run this inside the cloned folder:

```sh
git pull --ff-only
```

For a ZIP installation, download and extract the latest version into the same location. Keep any personal edits backed up before replacing files.

See the [official KiCad documentation](https://docs.kicad.org/) for library management and path configuration.
