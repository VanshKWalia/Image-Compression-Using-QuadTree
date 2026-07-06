# 🌲 Image Compression Using QuadTree (Python)

A Python-based image compression tool that uses the **Quadtree data structure**. The algorithm recursively divides an image into smaller regions and compresses areas with similar pixel values, reducing the overall image size while preserving visual quality.

---

## ✨ Features

- Quadtree-based image compression
- Adjustable compression threshold (user-controlled)
- Preserves important image details
- Automatically saves the compressed image
- Built with Python, NumPy, and OpenCV

---

## 📁 Project Structure

```
Image-Compression-Using-QuadTree/
│
├── main.py
├── input.jpg
├── compressed_image.jpg
├── requirements.txt
└── README.md
```

---

## ⚙️ How It Works

1. The image is loaded from `input.jpg`.
2. The entire image is represented by a quadtree root node.
3. Each node calculates the **average RGB value** of its region.
4. If all pixels in that region fall within the **threshold** of the average value, the node is treated as a **leaf node** (i.e., a homogeneous region).
5. If the region is not homogeneous, it is split into **4 smaller quadrants**, and the process repeats recursively.
6. Finally, the tree is traversed to build a **compressed image**, where each leaf node fills its region with a single average color.

---

## 🛠️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/VanshKWalia/Image-Compression-Using-QuadTree.git
cd Image-Compression-Using-QuadTree
```

### 2. Create a virtual environment (Recommended)

**Windows**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**Linux / macOS**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install numpy opencv-python
```

---

## ▶️ Usage — How To Run This Project

Follow these steps to use the project:

1. **Add your image** — Place the image you want to compress inside the project folder, and name it `input.jpg` (or replace the existing sample file with your own image renamed to `input.jpg`).

2. **Run the program** from the project folder:

   ```bash
   python main.py
   ```

3. **Enter a threshold value** when prompted:

   ```
   Input Threshold
   Choose greater than 5 for good compression
   Choose 5 for better compression
   Choose lesser than 5 for best compression
   More the value of threshold, lesser will be the runtime
   Threshold: 
   ```

   Type a number (e.g. `5`) and press Enter.

4. **Wait for processing** — The program builds a quadtree from your image and compresses it. Larger images or lower thresholds will take longer to run.

5. **Get your output** — Once done, you'll see:

   ```
   Image compression complete.
   ```

   A new file called `compressed_image.jpg` will appear in the project folder — this is your compressed image.

### Threshold Guide

| Threshold | Compression Level |
|-----------|-------------------|
| > 5 | Low Compression (better quality, larger file) |
| = 5 | Balanced Compression |
| < 5 | High Compression (smaller file, more detail loss) |

> 💡 Tip: A higher threshold runs faster but compresses less. A lower threshold compresses more but takes longer to run.

---

## 📤 Output

The program generates:

- `compressed_image.jpg` — The final compressed image (saved at JPEG quality 50)

---

## 📋 Requirements

- Python 3.10+
- NumPy
- OpenCV (`opencv-python`)

---

## 🧰 Technologies Used

- Python
- NumPy
- OpenCV
- Quadtree Data Structure

---

## 🚀 Future Improvements

- [ ] GUI using Tkinter or PyQt
- [ ] Compression ratio statistics
- [ ] Support for PNG, BMP formats
- [ ] Drag-and-drop image selection
- [ ] Batch image compression (multiple images at once)

---

## 📄 License

This project is intended for educational and learning purposes.

---

## 🙌 Acknowledgements

Built with ❤️ using Python, NumPy, and OpenCV as a college project.