### Perceptual Hash Value Retrieval for Image Forensics: A Hopfield Neural Network Application

This repository contains the source code focused on evaluating **Perceptual Hashing** combined with **Hopfield Neural Networks (HNN)** for image forensics and digital evidence retrieval.
The objective is to investigate how HNN can accurately restore corrupted perceptual hash signatures derived from altered or manipulated images. About the methodology, the application extracts features using **Differential Hash** (`dHash`) and trains an HNN using Hebbian learning rules. It evaluates error margins through **Hamming Distance** ($d_H$) analysis across 94 test samples distributed among distinct image databases.

---

#### Experiments & Analysis
The included implementation performs the following:
1. Loads and processes five distinct image databases: Lenna, Washington, Palace, Mountain, and Park.
2. Calculates perceptual hash values using the [Differential Hash (dHash)](https://www.hackerfactor.com/blog/index.php?/archives/432-Looks-Like-It.html).
3. Converts hash strings into binary ASCII formats.
4. Applies a 128-neuron HNN with bipolar activation (-1 and 1) for pattern storage and recall.
5. Evaluates performance success rates and maps the critical error threshold ($d_H \ge 8$).

---

#### Image Databases

| Database | Dataset Role / Source |
| --- | --- |
| **Lenna** | [ Images from Digital Image Processing, 3rd ed, by Gonzalez and Woods.](https://imageprocessingplace.com/root_files_V3/image_databases.htm) |
| **Washington** | [ Images from Digital Image Processing, 3rd ed, by Gonzalez and Woods.](https://imageprocessingplace.com/root_files_V3/image_databases.htm) |
| **Palace** | [ SUID: Synthetic Underwater Image Dataset.](https://ieee-dataport.org/open-access/suid-synthetic-underwater-image-dataset) |
| **Mountain** | [ SUID: Synthetic Underwater Image Dataset.](https://ieee-dataport.org/open-access/suid-synthetic-underwater-image-dataset) |
| **Park** | [ CoMoFoD - Image Database for Copy-Move Forgery Detection.](https://www.vcl.fer.hr/comofod/download.html) |

---

#### Usage
To run the analysis and execute the Hopfield Neural Network perceptual hash retrieval model:

1. Ensure you have the required libraries installed:
```bash
pip install numpy imagehash pandas scipy matplotlib seaborn
```

2. Import the necessary modules:
```python
import numpy as np
import binascii

# Initialize HNN with 128 neurons
network = HopfieldNetwork(128)
```

3. Train the network using the converted binary ASCII representation of the original image perceptual hash values:
```python
h1 = conv_ascii("Hash Value")
network.train(h1)
```

4. Input an altered or noisy hash value, convert it to binary array format, and execute the network recall function to restore the original pattern:
```python
a_hash = str(input("Hash Value: "))
a_hash_binary = conv_ascii(a_hash)

# Retrieve original information with HNN
retrieved_binary = network.recall(a_hash_binary)
retrieved_text = conv_string(retrieved_binary)
print("Retrieved Hash:", retrieved_text)
```

---

#### 🧰 Tools & Technologies
The project relies on the following core libraries and programming languages:

* **Python:** The core programming language used for data analysis, neural network modeling, and scripting.
* **ImageHash:** Library for image hashing and perceptual similarity calculations (`dHash`).
* **NumPy:** Used for numerical operations, matrix manipulations, and clearing diagonal weights in Hebbian learning.
* **Pandas:** Utilized for structuring, cleaning, and analyzing tabular experimental data and success/error metrics.
* **PIL (Pillow):** Python Imaging Library used for opening, manipulating, and processing various image formats.

---

#### 🔒🛠️ Intellectual Property (IP) Protection ( License, Restrictions, and Copyright )
All source code, documentation, and research methodologies contained in this repository are the exclusive Intellectual Property of the author. All rights reserved. Use of this content for academic or professional purposes must include proper citation and attribution to the original research.

**Copyright © 2026 João Rafael Gonçalves Evangelista.**
