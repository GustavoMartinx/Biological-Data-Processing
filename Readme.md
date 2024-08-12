# Processamento de Dados Biológicos |<br> Reconhecimento de Padrões

Este repositório destina-se a conter todos os artefatos desenvolvidos durante a disciplina optativa intitulada Reconhecimento de Padrões na qual abrange majoritariamente processamento de sinais biológicos obtidos por meio de equipamentos como eletroencefalograma (EEG), eletromiograma (EMG), entre outros.


## Como executar o projeto

### 1 - Clone este repositório

```bash
git clone https://github.com/GustavoMartinx/Biological-Data-Processing.git
```

### 2 - Obtenha as bases de dados utilizadas
Com um _e-mail_ institucional da UTFPR, acesse a pasta `s7` disponível no Google Drive e realize seu download:

https://drive.google.com/drive/folders/1wqzoCOL-teKerb75jyvQk7b9XW72eg78

- Lembre-se de descompactar a pasta e inserí-la no diretório correto do projeto.

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