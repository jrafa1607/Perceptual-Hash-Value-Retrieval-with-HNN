## Content-based Image Retrieval using Differential Hashing and Hopfield Neural Network
> In this repository are the files used for the development of a computer vision system for retrieving Differential Hash values with Hopfield Neural Networks. Using this computer vision system, it is possible to calculate the differential Hash of countless images, original and altered, and use HNN to retrieve the original value. Other important information for the development of the experiment:
- <a href="https://www.ime.usp.br/~kellyrb/mac2166_2015/tabela_ascii.html"> ASCII Table </a>
- <a href="https://didatica.tech/underfitting-e-overfitting/"> What is Overfitting and Underfitting? </a>
- <a href="https://ieeexplore.ieee.org/document/8623902"> IEEE Paper - Example of HNN application to retrieval Perceptual Hash </a>
- <a href="https://github.com/andreasfelix/hopfieldnetwork"> Github Hopfield - Another Aplication </a>

## Computer Vision Experiment
### 💻 Experiment Resume

For the development of the experiment, 5 Image databases were selected. All databases have an Original image and other variations of the Original image. The objective of the experiment was to recover the hash value of altered images with Hopfield Neural Networks. For example:

- Original Hash: ABC01234
- Altered  Hash: ABC01222

Hopfield Neural Network Training was carried out with the Original Values, so that when a changed value was provided as input, the output would be the correct Hash value.

- Original Hash: ABC01234
- Altered  Hash: ABC01222
- Retrived Hash with HNN: ABC01234

### 💻 Image Bases for Experiments

All image bases used in this experiment are available [in this folder](https://github.com/jrafa1607/HNN-to-Content-Based-Hash-Retrieval/tree/main/Image%20Database)

- [x] LennaDatabase - Avaliable in: [<b> Images from Digital Image Processing, 3rd ed, by Gonzalez and Woods.</b>](https://imageprocessingplace.com/root_files_V3/image_databases.htm)

- [x] WashingtonDatabase - Avaliable in: [<b> Images from Digital Image Processing, 3rd ed, by Gonzalez and Woods.</b>](https://imageprocessingplace.com/root_files_V3/image_databases.htm)

- [x] PalaceDatabase - Avaliable in: [<b> SUID: Synthetic Underwater Image Dataset.</b>](https://ieee-dataport.org/open-access/suid-synthetic-underwater-image-dataset)

- [x] Mountain Database - Avaliable in: [<b> SUID: Synthetic Underwater Image Dataset.</b>](https://ieee-dataport.org/open-access/suid-synthetic-underwater-image-dataset)

- [x] ParkDatabase - Avaliable in: [<b> CoMoFoD - Image Database for Copy-Move Forgery Detection.</b>](https://www.vcl.fer.hr/comofod/download.html)

## Computer Vision Automation - Main Steps:
### 📊📝 HNN-to-Content-Based-Hash-Retrieval

- [x] Library Importing </b>
- [x] Definition of Activation Function to HNN: (Bipolar: -1 e 1)
- [x] Definition of Recovery Matriz to HNN
- [x] Definition of total of neurons (128)
- [x] Create the HNN Architecture (Training + Recovery Matriz)
- [x] Create the Converter Fcuntion between Hash Values and Binary Value: 

#### Example of Conversion: Hash -> Binary ASCII
"6470795b33135a38" -> "00110110 00110100 00110111 00110000 00110111 00111001 00110101 01100010 00110011 00110011 00110001 00110011 00110101 01100001 00110011 00111000"

#### Example of Conversion: Binary ASCII -> Hash
"00110110 00110100 00110111 00110000 00110111 00111001 00110101 01100010 00110011 00110011 00110001 00110011 00110101 01100001 00110011 00111000" -> "6470795b33135a38"

- [x] Values of the Original Images from each five bases of images.

| Database | D-Hash |
| ---      | ---       |
| Lenna Database | 7670795b33135a38 |
| Washington Database | d3d85833daeab5a9 |
| Palace Database | e6ce8e991c149694 |
| Mountain Database | 402416531b191a1f |
| Park Database | 4659d98bcbcb9639 |

- [x] Conversion of Value Hash to Binary
- [x] HNN Training with Binary Value
- [x] Input a Noise Information (Hash from Altered Image) to HNN
- [x] Avaliate the retrieve for the Original Value

### 📈 Info about the experiment.
- The file " - Experimento.xlsx"- All the Results;
- The file " - Resultados.xlsx" - All the Graphics of the Results;
- The file " - Full Experiment" - Main file with all the experiment;
- The file " - D-Hash Calc" - Example of Differential Hash Application
- The file " - Hamming Distance" - Make the <a href="https://www.geeksforgeeks.org/hamming-distance-two-strings/"> Hamming Distance Calc </a> between the Hash Value Original and the Hash Value retrieved by HNN;