# 🎨 Neural Style Transfer — README

## 📌 Project Overview

**Neural Style Transfer (NST)** is a deep learning technique that combines the **content** of one image with the **artistic style** of another image to generate a new stylized image.

This project implements Neural Style Transfer using a pre-trained Convolutional Neural Network (CNN). The algorithm extracts:

* **Content features** from a content image
* **Style features** from a style image
  and optimizes a generated image to match both.

---

## ✨ Features

* Apply artistic styles to any image
* Uses pretrained CNN feature extraction
* Adjustable style and content weights
* Works in **Google Colab** or local Python environment
* Saves high-quality stylized outputs

---

## 🧠 How It Works

1. Load **Content Image**
2. Load **Style Image**
3. Extract feature representations using a pretrained network
4. Compute:

   * Content Loss
   * Style Loss
   * Total Variation Loss (optional)
5. Optimize pixels of a generated image
6. Save the final stylized output

---

## 🛠 Requirements

### Python Version

```
Python 3.8+
```

### Libraries

Install required packages:

```bash
pip install torch torchvision pillow matplotlib numpy
```

For Google Colab:

```python
!pip install torch torchvision pillow matplotlib numpy
```

---

## 📂 Project Structure

```
NEURAL_STYLE_TRANSFER_CODE/
│
├── content.jpg          # Input content image
├── style.jpg            # Input style image
├── output/              # Generated results
├── neural_style.py      # Main implementation
├── utils.py             # Helper functions (optional)
└── README.md
```

---

## ▶️ Usage

### Run Locally

```bash
python neural_style.py \
    --content content.jpg \
    --style style.jpg \
    --output output/result.png
```

### Run in Google Colab

Upload images and run:

```python
python neural_style.py \
    --content content.jpg \
    --style style.jpg
```

---

## ⚙️ Parameters

| Parameter          | Description             | Default    |
| ------------------ | ----------------------- | ---------- |
| `--content`        | Path to content image   | Required   |
| `--style`          | Path to style image     | Required   |
| `--output`         | Output file path        | result.png |
| `--steps`          | Optimization iterations | 300        |
| `--style_weight`   | Style importance        | 1e6        |
| `--content_weight` | Content importance      | 1          |

---

## 🖼 Example Workflow

1. Choose a photo (content image).
2. Choose an artwork painting (style image).
3. Run the script.
4. Generated image appears in `/output`.

---

## 📊 Output

The program generates:

* Stylized image
* Intermediate progress (optional)
* Loss values during optimization

---

## 🧩 Customization

You can modify:

* Optimization steps
* Learning rate
* Style layers used
* Image resolution

Higher resolution produces better quality but requires more GPU memory.

---

## ⚠️ Troubleshooting

**Problem:** CUDA/GPU not detected
✅ Solution:

```python
import torch
torch.cuda.is_available()
```

**Problem:** Out of memory
✅ Reduce image size:

```python
image_size = 256
```

**Problem:** Slow execution
✅ Use GPU runtime in Colab:

```
Runtime → Change runtime type → GPU
```

---

## 📚 Concepts Used

* Convolutional Neural Networks
* Feature Extraction
* Gram Matrix
* Gradient Optimization
* Deep Learning Image Processing

---

## 🙌 Acknowledgment

Inspired by the original Neural Style Transfer research demonstrating artistic style synthesis using deep neural networks.

---

## 📄 License

This project is open-source and free to use for educational and research purposes.

---

## 👨‍💻 Author

Your Name Here
(Add GitHub profile or contact if needed)

---

⭐ If you like this project, consider giving it a star!
