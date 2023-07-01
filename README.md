## Recuperação de Valor Hash Diferencial com Redes Neurais de Hopfield 
> Nesse repositório, estão armazenadas os arquivos utilizados para o desenvolvimento de um sistema de visão computacional para recuperação de valores Hash Diferenciais com Redes Neurais de Hopfield <a href="http://www2.decom.ufop.br/imobilis/redes-de-hopfield/"> (HNN-to-Content-Based-Hash-Retrieval) </a>. Ao utilizar este sistema de visão computacional, é possível calcular o Hash diferencial de inúmeras imagens, originais e alteradas, e utilizar HNN para recuperar o valor Original.

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20210216132537/Architecureofnetwork-660x377.png" alt="Hopfield Neural Network">
</p>

> Outras informações informações importantes para o desenvolvimento do experimento:
- <a href="https://www.ime.usp.br/~kellyrb/mac2166_2015/tabela_ascii.html"> Tabela ASCII </a>
- <a href="https://didatica.tech/underfitting-e-overfitting/"> Breve explicação sobre Overfitting e Underfitting </a>
- <a href="https://ieeexplore.ieee.org/document/8623902"> Exemplo de Aplicação de HNN para Recuperar Valores Hash </a>

## Experimento de Visão Computacional
### 💻 Base de Imagens para os Experimentos

<p align="center">
  <img src="Anexos/image_database.jpeg" alt="Cloud Computing">
</p>

Para o desenvolvimento do experimento, foram selecionadas 5 bases de Imagens.
Todas as bases possuem uma imagem Original e outras variações da imagem Original.
O Objetivo do experimento foi Recuperar o valor Hash das Imagens Alteradas com as Redes Neurais de Hopfield. Por exemplo:

- Hash Original: ABC01234
- Hash Alterado: ABC01222

O Treinamento das Redes Neurais de Hopfield foi realizado com os Valores Originais, para que assim, quando um valor alterado fosse fornecido como entrada, a saída fosse o valor correto do Hash.

- Hash Original: ABC01234
- Hash Alterado: ABC01222
- Hash Recuperado com Hopfield: ABC01234

Todas as bases de imagens utilizadas nesse experimento estão disponíveis [nesse repositório](https://github.com/jrafa1607/HNN-to-Content-Based-Hash-Retrieval/tree/main/Image%20Database)

####  LennaDatabase e WashingtonDatabase
As Bases LennaDatabase e WashingtonDatabase foram selecionadas da publicação: <b> Images from Digital Image Processing, 3rd ed, by Gonzalez and Woods.</b> Disponível no Link: https://imageprocessingplace.com/root_files_V3/image_databases.htm
- [x] Lenna Database (20 Imagens)
- [x] Washington Database (07 Imagens)

#### PalaceDatabase e MountainDatabase
As Bases PalaceDatabase e MountainDatabase foram selecionadas na Base de Imagens: <b> SUID: Synthetic Underwater Image Dataset.</b> Disponível no Link: https://ieee-dataport.org/open-access/suid-synthetic-underwater-image-dataset
- [x] PalaceDatabase (31 Imagens)
- [x] MountainDatabase (30 Imagens)

#### ParkDatabase
A Base ParkDatabase foi selecionada na Base de Imagens: <b> CoMoFoD - Image Database for Copy-Move Forgery Detection.</b> Disponível no Link: https://www.vcl.fer.hr/comofod/download.html
- [x] ParkDatabase (11 Imagens)


## Sobre a Automação de Visão Computacional
### 📊📝 HNN-to-Content-Based-Hash-Retrieval

- [x] Importação das Bibliotecas </b>
- [x] Definição da Função de Ativação da Rede Neural de Hopfield (Bipolar: 0 e 1) 
- [x] Definição da Matriz de Recuperação de Informação da Rede Neural de Hopfield
- [x] Definição do total de neurônios utilizados (128)
- [x] Criação da Estrutura da HNN (Fases de Treinamento e a Chamada da Matriz de Recuperação de Informação)
- [x] Criação das Funções para converter os valores Hash: 

#### Exemplo de Conversão: Hash -> ASCII Binário
"6470795b33135a38" -> "00110110 00110100 00110111 00110000 00110111 00111001 00110101 01100010 00110011 00110011 00110001 00110011 00110101 01100001 00110011 00111000"

#### Exemplo de Conversão: ASCII Binário -> Hash
"00110110 00110100 00110111 00110000 00110111 00111001 00110101 01100010 00110011 00110011 00110001 00110011 00110101 01100001 00110011 00111000" -> "6470795b33135a38"

- [x] Lista dos Valores Hash Diferencial das 5 Imagens Originais de cada Base.

| Database | D-Hash |
| ---      | ---       |
| Lenna Database | 7670795b33135a38 |

- "7670795b33135a38" #Lenna Database
- "d3d85833daeab5a9" #Washington Database
- "e6ce8e991c149694" #Palace Database
- "402416531b191a1f" #Mountain Database
- "4659d98bcbcb9639" #Park Database

- [x] Conversão do Texto do Hash para Binário
- [x] Treinamento da Rede Neural de Hopfield com o Hash em Binário
- [x] Input de uma Informação com Ruído
- [x] Recuperação da Informação Original

### 📈 Informações sobre o Experimento
- A pasta Dados contém o valor das distâncias de Hamming entre o Hash Perceptivo e a Imagem Original.
- A pasta Resultados contém os resultados do Hash Convencional, do Hash Perceptivo e dos cálculos de distância.
- A pasta Anexos contém as imagens com as fórmulas e anotações sobre as Distâncias de Hamming, Euclidiana, Manhattan e Minkovski.

To validate this experiment, we have the Hamming Distance:
https://www.geeksforgeeks.org/hamming-distance-two-strings/