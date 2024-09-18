# Processamento de Dados Biológicos |<br> Reconhecimento de Padrões

Este repositório destina-se a conter todos os artefatos desenvolvidos durante a disciplina optativa intitulada Reconhecimento de Padrões (OPT020) ministrada pelo professor [Dr. Rodrigo Hübner](https://github.com/rodrigohubner). A disciplina compreendeu majoritariamente processamento de sinais biológicos. As bases de dados utilizadas foram obtidas em um [experimento](#o-experimento), por meio de equipamentos de eletroencefalograma (EEG).

## O Experimento
O experimento realizado teve como objetivo comparar os níveis de foco de alunos de graduação enquanto assistiam a uma aula ministrada com a metodologia de ensino ativa e a outra aula com a metodologia de ensino tradicional.

Cada aluno assistiu a duas aulas, cada uma correspondente a uma das metodologias de ensino supracitadas, com um intervalo de 1 a 3 dias entre elas. Enquanto assistiam, um equipamento de eletroencefalograma (EEG) de 8 canais (eletrodos) capturava os sinais cerebrais do aluno e os registrava em um arquivo. Os [dados obtidos](https://drive.google.com/drive/u/1/folders/1nq-1CJqpru-UfAU-ycd4OKLC7uQVizU9) podem ser acessados com um _e-mail_ institutional da UTFPR.

## Artefatos e seus objetivos
Durante a primeira etapa de trabalho (`roteiro.ipynb`) buscou-se desenvolver um algoritmo denominado _Janela Deslizante_ que determina a porcentagem de tempo em que cada banda de frequência cerebral é dominante ao longo de uma janela de tempo específica. Os resultados obtidos são plotados em gráficos de barras respectivos a cada seção (conjunto de dados de um participante) do experimento.

Por meio da análise dos dados do experimento no _software_ [OpenBCI GUI](https://docs.openbci.com/Software/OpenBCISoftware/GUIDocs/), foram identificados trechos que apresentam picos de potência em bandas de frequência cerebrais específicas. Nesse sentido, o segundo produto desta disciplina (`sliced_analysis.ipynb`) visou observar e identificar essas proeminências de potência através do algoritmo de janela de tempo deslizante citado anteriormente.

Por fim (`feature_snr.ipynb`), empregou-se a relação sinal-ruído (SNR, _signal-to-noise ratio_) para tentar realçar a presença dos ritmos cerebrais relacionados ao foco. Nesse contexto, em linhas gerais, foi utilizado um sinal cerebral basal para (através do SNR) "subtraí-lo" dos dados de interesse.

## Como executar o projeto

### 1 - Clone este repositório

```bash
git clone https://github.com/GustavoMartinx/Biological-Data-Processing.git
```

### 2 - Obtenha as bases de dados utilizadas
Acesse o diretório `Dataset S7` disponível [neste Google Drive](https://drive.google.com/drive/folders/1uNLWT2wJ3S6a3Sw7Oht0_Wd8AQmIAr-E?usp=sharing) e realize o _download_ do arquivo `dataset-s7.zip`:

Descompacte o arquivo `dataset-s7.zip` baixado e insira-o no diretório `Dataset-Foco-Atencao`, de modo que a estrutura do projeto fique assim:

```console
Dataset-Foco-Atencao/
├── dataset-s7/
│   ├── GT/
│   │   ├── MinutagemGT.docx
│   │   └── OpenBCI-RAW_GT.txt
│   ├── IA/
│   │   ├── MinutagemIA.docx
│   │   └── OpenBCI-RAW_IA.txt
│   ├── TF/
│   │   ├── MinutagemTF.docx
│   │   └── OpenBCI-RAW_TF.txt
└── src/
```

### 3 - Crie um ambiente virtual

    python -m venv ./nome-do-venv
    
Em seguida, **ative-o**:

- Linux

    ```
    source ./nome-do-venv/bin/activate
    ```

- Windows (Prompt de Comando)

    ```
    .\nome-do-venv\Scripts\activate
    ```

- Windows (Terminal Integrado do VSCode)

    ```
    source ./nome-do-venv/Scripts/activate
    ```

### 4 - Instale as dependências

    pip install -r requirements.txt

### 5 - Execute o projeto

Para executar os _jupyter notebooks_, basta selecionar qual _kernel_ Python você deseja utilizar. Selecione o ambiente virtual recém criado que contém as dependências necessárias instaladas e execute as células do _notebook_.