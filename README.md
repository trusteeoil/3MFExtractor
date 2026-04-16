# 3MF Print File Extractor Tool

Extract all print settings from a `.3mf` file into a searchable table, then copy it as Markdown.

This tool runs entirely in your browser. No uploads, no tracking, no data leaving your device.

---

## What This Tool Does

* Upload a `.3mf` file (BambuStudio, OrcaSlicer, and similar)
* Extract embedded print settings
* Display them in a clean, searchable table
* Copy the data as a Markdown table for easy sharing

Useful for:

* Troubleshooting 3D prints
* Sharing settings in forums or Discord
* Comparing slicer profiles
* Feeding structured data into AI tools

---

## How It Works

* Reads the `.3mf` file as a ZIP archive
* Extracts:
  `Metadata/project_settings.config`
* Parses the JSON settings inside
* Flattens nested data into key paths like:
  `filament_type[0]`, `nozzle_temperature[0]`
* Separates:

  * Print settings
  * G-code sections

---

## Features

* Drag-and-drop `.3mf` file upload
* Search and filter settings instantly
* Sorted view that prioritizes important settings
* Raw view for full data inspection
* Copy output as a Markdown table
* Separate tab for G-code sections
* Human-readable and raw key display modes

---

## Privacy

* All processing happens locally in your browser
* No files are uploaded
* No data is sent to any server
* Uses JSZip via CDN (with integrity protection)

---

## Supported Files

Works best with:

* BambuStudio `.3mf` files
* OrcaSlicer `.3mf` files

Other `.3mf` files may work if they include:
`Metadata/project_settings.config`

---

## Limitations

* If `project_settings.config` is missing, no settings will be extracted
* Some slicers may store settings differently
* G-code is displayed separately to keep the main table clean

---

## Usage

1. Open the tool
2. Drop in a `.3mf` file or click to browse
3. Click "Extract Print Data"
4. Search or review the settings
5. Click "Copy as Markdown Table" to share

---

## Example Output

```
| Setting | Value |
|:---|:---|
| layer_height | 0.2 |
| nozzle_temperature[0] | 220 |
| bed_temperature[0] | 60 |
```

---

## Why This Exists

Sharing full `.3mf` files is often inconvenient or unnecessary. Sometimes you need help with your print settings but don't want to or can't share the actual 3MF file because it contains the actual 3D model. 

This tool makes it easy to:

* Extract only what matters (settings)
* Share clean, readable data
* Get better help faster

---

## License

Open source. Use it however you want.
