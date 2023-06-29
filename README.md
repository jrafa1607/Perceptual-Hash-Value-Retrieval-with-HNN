## Recuperação de Valor Hash Diferencial com Redes Neurais de Hopfield 
> Nesse repositório, estão armazenadas os arquivos utilizados para o desenvolvimento de um sistema de visão computacional para recuperação de valores Hash Diferenciais com Redes Neurais de Hopfield (HNN-to-Content-Based-Hash-Retrieval). Ao utilizar este sistema de visão computacional, é possível calcular o Hash diferencial de inúmeras imagens, originais e alteradas, e utilizar HNN para recuperar o valor Original.


## Experimento de Visão Computacional
### 💻 Base de Imagens para os Experimentos

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20210216132537/Architecureofnetwork-660x377.png" alt="Hopfield Neural Network">
</p>

Para o desenvolvimento do experimento, foi utilizado 5 bases de Imagens.
Todas as bases possuem uma imagem Original e outras variações da imagem Original.
O Objetivo do experimento é identificar que ambas as imagens, Original e Variações, possuem uma relação determinada pelo Hash Perceptivo.
Todas as bases de imagens estão disponíveis [nesse repositório:](https://github.com/jrafa1607/Evaluation-of-Perceptual-Hash-Algorithms/tree/main/ImageDatabase)

####  LennaDatabase e WashingtonDatabase
As Bases LennaDatabase e WashingtonDatabase foram selecionadas da publicação: <b> Images from Digital Image Processing, 3rd ed, by Gonzalez and Woods.</b> Disponível no Link: https://imageprocessingplace.com/root_files_V3/image_databases.htm
- [x] Lenna Database (21 Imagens)
- [x] Washington Database (07 Imagens)

#### PalaceDatabase e MountainDatabase
As Bases PalaceDatabase e MountainDatabase foram selecionadas na Base de Imagens: <b> SUID: Synthetic Underwater Image Dataset.</b> Disponível no Link: https://ieee-dataport.org/open-access/suid-synthetic-underwater-image-dataset
- [x] PalaceDatabase (31 Imagens)
- [x] MountainDatabase (30 Imagens)

#### ParkDatabase
A Base ParkDatabase foi selecionada na Base de Imagens: <b> CoMoFoD - Image Database for Copy-Move Forgery Detection.</b> Disponível no Link: https://www.vcl.fer.hr/comofod/download.html
- [x] ParkDatabase (11 Imagens)


## Sobre as Automações
### 📊📝 Automações para Visão Computacional com Python
Para realizar os experimentos, foram desenvolvidos duas automações em Python:
- [x] <b>Perceptual Hashing Evaluation:</b> Automação responsável por Calcular a distância de Hamming entre os 6 Tipos de Hash Perceptivo e a Imagem Original
- [x] <b>Distance Calc (Euclidean & Manhattan):</b> Automação responsável por Cálcular a distância Eucliana e Manhattan dos Valores de Hamming obtidos pela primeira automação.


### 📈 Informações sobre o Experimento
- A pasta Dados contém o valor das distâncias de Hamming entre o Hash Perceptivo e a Imagem Original.
- A pasta Resultados contém os resultados do Hash Convencional, do Hash Perceptivo e dos cálculos de distância.
- A pasta Anexos contém as imagens com as fórmulas e anotações sobre as Distâncias de Hamming, Euclidiana, Manhattan e Minkovski.







# HNN-to-Content-Based-Hash-Retrieval

Hopfield Neural Network to Content-Bases Hash Retrieval Information 

- Example of Application: https://ieeexplore.ieee.org/document/8623902
- Hopfield Neural Network Description: http://www2.decom.ufop.br/imobilis/redes-de-hopfield/
- Table ASCII: https://www.ime.usp.br/~kellyrb/mac2166_2015/tabela_ascii.html
- Overfitting and Underfitting Explanation: https://didatica.tech/underfitting-e-overfitting/

Step by Step of Code:

- 1: Import of Libraries
- 2: Definition of Activation Function (In this case, Bipolar)
- 3: Definition of a Retrive Matrix
- 4: Create a structure of HNN, WIth the Train Step and the Call of Retrive Matrix Function

After that, we have:
- Example with a Binaty String (8 bits with values: 0 and 1)

About Customized Functions to this Experiment:
- 1: Function to Convert Character into a Binary
- 2: Function to Convert a String Hash to Binary and Split into a List
- 3: Function to Convert ASCII values into String

To validate this experiment, we have the Hamming Distance:
https://www.geeksforgeeks.org/hamming-distance-two-strings/
