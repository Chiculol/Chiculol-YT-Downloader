# Chiculol-YT-Downloader
YT downloader para aqueles que tem preguiça de ir em sites esquisitos ou programas esquisitos (Se bem que o meu é esquisito ams é pq é meu pimeiro ams vai da certo tlgd), epero que seja útil! ^^

# Downloader de Vídeos e Áudios do YouTube (Projeto Chiculol)

Este é um script de console em Python desenvolvido para baixar vídeos e áudios do YouTube, oferecendo controle sobre a qualidade desejada. O projeto utiliza a biblioteca `yt-dlp` para uma interação robusta e atualizada com o YouTube.

##  Funcionalidades

* **Listagem de Formatos:** Exibe uma lista detalhada de todas as qualidades de vídeo e áudio disponíveis para um determinado link.
* **Seleção de Qualidade:** Permite ao usuário escolher um formato específico de vídeo, áudio, ou uma combinação de ambos para obter a melhor qualidade.
* **Download Inteligente:** Utiliza o FFmpeg para juntar os melhores streams de vídeo e áudio que o YouTube oferece separadamente.
* **Tratamento de Links:** Foca no vídeo principal e ignora playlists automaticamente para evitar downloads indesejados.
* **Nomenclatura Automática:** Salva os arquivos com o título original do vídeo, removendo caracteres inválidos.

##  Pré-requisitos

Antes de executar este projeto, certifique-se de que você tem os seguintes softwares instalados em seu sistema:

1.  **Python:** Versão **3.9 ou superior** é recomendada.
2.  **FFmpeg:** Uma ferramenta essencial que o `yt-dlp` usa para juntar (mux) os arquivos de vídeo e áudio.
    * **Download:** [FFmpeg Official Builds](https://www.gyan.dev/ffmpeg/builds/)
    * **Instalação:** É crucial que o `ffmpeg` esteja no PATH do seu sistema para que o script possa encontrá-lo.

##  Instalação e Configuração

Siga os passos abaixo para configurar o ambiente e rodar o projeto.

1.  **Coloque todos os arquivos do projeto** em uma pasta em seu computador.

2.  **Crie e ative um ambiente virtual** (altamente recomendado):
    ```bash
    # Cria o ambiente virtual
    python -m venv venv
    
    # Ativa o ambiente no Windows
    .\venv\Scripts\activate
    
    # Ativa o ambiente no macOS/Linux
    source venv/bin/activate
    ```

3.  **Instale as dependências** a partir do arquivo `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```

##  Como Usar

1.  Abra um terminal (como o terminal do PyCharm).
2.  Certifique-se de que seu ambiente virtual está ativado.
3.  Execute o script principal:
    ```bash
    python baixar_video.py
    ```
4.  Siga as instruções na tela: cole a URL, analise as qualidades e faça sua escolha.
5.  O arquivo será salvo na mesma pasta do projeto.

---
_Gerado em 17 de Agosto de 2025._
