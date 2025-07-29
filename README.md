# ims2czi: Batch Convert `.ims` to `.czi`

🧬 A simple Python tool to **batch convert Imaris `.ims` files** (from Dragonfly spinning disk microscope) into **Zeiss `.czi` format**, preserving channel names and colors.

## 🧾 Purpose / 使用目的

This script converts `.ims` files (exported by Imaris, often from Dragonfly spinning disk confocal microscopes) into Zeiss `.czi` format for compatibility with downstream analysis software.

It retains:
- Channel names
- Channel display colors
- Voxel dimensions (XY/Z)

---

這個工具能將 `.ims` 檔（如 Dragonfly 顯微鏡產出的）轉為 Zeiss `.czi` 格式，方便在不支援 `.ims` 的工具中使用，例如 ImageJ 或 Zeiss ZEN。

會保留：
- 通道名稱
- 顯示顏色
- 像素大小（XY 與 Z 間距）


## Features
- ✅ Batch convert `.ims` to `.czi`
- ✅ Retains channel names and colors
- ✅ Auto-detects voxel sizes from geometry metadata
- ✅ Simple GUI folder selector

## Installation

```bash
git clone https://github.com/qqhair2000/ims2czi.git
cd ims2czi
pip install -r requirements.txt
```

## Usage

```bash
python ims2czi_name_COLOR-2e.py
```

Then select the folder containing `.ims` files. Converted `.czi` files will be saved in the same folder.

## Requirements

- Python 3.8+
- `numpy`, `h5py`, `imaris-ims-file-reader`, `pylibCZIrw`


## 📄 License

This project is licensed under the **Apache License 2.0**. See [LICENSE](./LICENSE) for full text.

### Included / Invoked Dependencies

This tool invokes but does not bundle or modify the following third-party libraries:

| Dependency                  | License                                     | Purpose                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------|
| `imaris-ims-file-reader`   | MIT License                                 | To read `.ims` files from Imaris format.                       |
| `pylibCZIrw`               | ZEISS PyLibCZIrw License (proprietary)      | To write `.czi` files in a Zeiss-compatible format.            |
| `numpy`, `h5py`            | BSD-style / MIT License                     | For numerical operations and HDF5 reading.                     |

> Note: These dependencies are installed via pip and are not modified or bundled with this repository.
