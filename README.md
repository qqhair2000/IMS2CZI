# ims2czi: Batch Convert `.ims` to `.czi`

🧬 A simple Python tool to **batch convert Imaris `.ims` files** (from Dragonfly spinning disk microscope) into **Zeiss `.czi` format**, preserving channel names and colors.

## Features
- ✅ Batch convert `.ims` to `.czi`
- ✅ Retains channel names and colors
- ✅ Auto-detects voxel sizes from geometry metadata
- ✅ Simple GUI folder selector

## Installation

```bash
git clone https://github.com/your-username/ims2czi.git
cd ims2czi
pip install -r requirements.txt
```

## Usage

```bash
python ims2czi.py
```

Then select the folder containing `.ims` files. Converted `.czi` files will be saved in the same folder.

## Requirements

- Python 3.8+
- `numpy`, `h5py`, `imaris-ims-file-reader`, `pylibCZIrw`

## License

MIT License
