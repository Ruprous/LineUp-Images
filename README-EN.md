# 📐 LineUp-Images

This tool arranges all images in a selected directory in a horizontal layout with a fixed width of 3000px.  
You can configure the number of columns, margin between images, and background color.  
The input and output paths are selected via GUI, and output is saved as a PNG image.

<img src="./src/lineupimage.png" alt="Sample Image" width="50">

---

## 🖥️ System Requirements

### When using the EXE version
- **OS**: Windows 10 or later
- **No need to install Python**
- **Download the executable from the [Releases page](https://github.com/Ruprous/LineUp-images/releases)**

### When using the Python script
- **Python 3.8 or higher**
- Required libraries:
  - `Pillow`
  - `tkinter` (standard library)

Install libraries with:

```bash
pip install pillow
```

---

## 🚀 How to Use

### 1. Using the EXE Version

1. Double-click `LineUp-Images.exe` to run.
2. Follow the prompts:
   - **Select image folder**: Use Explorer to choose a directory containing images.
   - **Choose save location and file name** (output will be `.png`)
   - **Background setting**: Choose whether to use transparent or black background
     - `yes`: Transparent background
     - `no`: Black background (`#000000`)
   - **Number of columns**: Input the number of images to place per row.
   - **Margin (px)**: Set margin between images (0–300px).

---

### 2. Using the Python Script

1. Run the script with:

```bash
python LineUp-Images.py
```

Or double-click `run.bat`.

2. The following steps are the same as the EXE version.

---

## 📤 Output

- The final image will be saved in the specified location as a PNG file.
- Output width is fixed to 3000px.
- Images are resized proportionally with padding to preserve aspect ratio.

---

## ⚠️ Notes

1. **Supported image formats**:
   - `.jpg`, `.jpeg`, `.png`, `.bmp`, `.gif`
   - Other file types will be ignored.

2. **Margin limit**:
   - Margins must be within `0–300px`.

3. **Image resizing behavior**:
   - Images are resized to fit into square slots based on the number of columns and margin.
   - Aspect ratio is preserved; background padding is applied if needed.

---

## 📁 Example

### Folder structure

```plaintext
images/
├── image1.jpg
├── image2.png
├── image3.jpeg
└── image4.bmp
```

### Example input during EXE execution

```plaintext
Use transparent background? (yes/no): yes
Number of columns: 3
Margin between images (0–300 px): 20
```

---

## 📦 Files in the Repository

- `LineUp-Images.exe`: Windows executable (⚠️ not included in this repo; download from the Releases page)
- `LineUp-Images.py`: Python source code
- `run.bat`: Windows batch launcher
- `LICENSE`: License file
- `README.md`: Japanese version
- `README-EN.md`: This file

---

## 🪪 License

This tool is released under the [MIT License](./LICENSE).
