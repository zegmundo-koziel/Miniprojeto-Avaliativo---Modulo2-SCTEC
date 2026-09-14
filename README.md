# Pipeline de Pré-Processamento de Imagens — Indústria 4.0 (Mini-Projeto Módulo 2)

## 🛠️ Descrição do Projeto
Este projeto consiste no desenvolvimento de um pipeline automatizado de Visão Computacional utilizando **Python** e **OpenCV** para preparar as imagens para o treinamento de modelos de Machine Learning. 

O projeto utiliza o dataset público [Casting Product Image Data for Quality Inspection](https://drive.google.com/file/d/1K5gNxQ7RXA-nb4boNzPYQTJlRvJyYBD1/view), que contém imagens reais de peças de fundição metálicas com e sem defeitos estruturais (ranhuras e fendas). O objetivo principal é limpar, filtrar e padronizar o lote de imagens antes de enviá-lo para os modelos preditivos.

## 🚀 Estrutura das Sprints Realizadas
- **Sprint 1: Configuração e Versionamento** -> Inicialização do repositório Git, criação do ambiente virtual `.venv`, isolamento com `.gitignore` e setup da branch `development`.
- **Sprint 2: Estruturação de Dados e Leitura** -> Criação das pastas de entrada/saída e desenvolvimento do algoritmo de leitura em lote (Batch Processing).
- **Sprint 3: Pipeline de Pré-processamento Base** -> Conversão automática para Escala de Cinza (Grayscale) e redução de ruídos de superfície com filtro matemático Gaussian Blur.
- **Sprint 4: Segmentação e Destaque** -> Aplicação de Limiarização Adaptativa de Otsu para binarização e Detector de Bordas Canny para extração dos contornos físicos das ranhuras.
- **Sprint 5: Refinamento Morfológico e Padronização** -> Uso de operações morfológicas para fechamento de lacunas de segmentação e redimensionamento fixo de todo o lote para o padrão de 256x256 pixels.
- **Sprint 6: Gravação e Documentação** -> Salvamento automatizado em lote estruturado por classes no diretório de saída e consolidação do versionamento Git.

## 📦 Como Executar o Projeto

### 1. Clonar o Repositório e Configurar Ambiente
Abra o terminal na pasta do projeto e execute:
```cmd
# Ative o ambiente virtual:
.venv\Scripts\activate.bat

# Instale as dependências necessárias:
pip install opencv-python numpy matplotlib ipykernel
```

### 2. Download e Configuração do Dataset
Para que o script rode corretamente em lote, siga os passos abaixo para estruturar as imagens:
1. Faça o download do arquivo compactado clicando em [Casting Product Image Data](https://drive.google.com/file/d/1K5gNxQ7RXA-nb4boNzPYQTJlRvJyYBD1/view).
2. Descompacte o arquivo `.zip` extraindo o seu conteúdo.
3. Localize as pastas contendo as fotos originais (`def_front` e `ok_front`).
4. Mova ou copie essas duas pastas com todas as imagens para dentro do diretório **`raw_images/`** na raiz do seu projeto. 

A estrutura de diretórios local deve ficar exatamente assim:
```text
Miniprojeto-Avaliativo---Modulo2-SCTEC/
├── raw_images/
│   ├── def_front/  <- (Imagens originais com defeito)
│   └── ok_front/   <- (Imagens originais sem defeito)
├── processed_images/ <- (Será preenchida automaticamente pelo script)
├── main.ipynb
└── README.md
```

### 3. Execução
Abra o arquivo `main.ipynb` utilizando o VS Code, certifique-se de selecionar o Kernel do ambiente virtual (`.venv`) no canto superior direito e execute as células em sequência para rodar o pipeline em lote.

## 🎓 Informações de Entrega (Semana 07)
Conforme os requisitos do projeto estabelecidos pela instituição, a documentação complementar foi organizada e disponibilizada através dos links abaixo:
- **Vídeo de Apresentação e Demonstração:** https://drive.google.com/drive/folders/1_QBAH2NFfE1t8FtgUmfewNdDVil-AaTb?usp=sharing

