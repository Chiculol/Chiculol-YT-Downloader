# Chiculol-YT-Downloader
YT downloader para aqueles que tem preguiça de ir em sites esquisitos ou programas esquisitos (Se bem que o meu é esquisito mas é pq é meu pimeiro mas vai da certo tlgd), epero que seja útil! ^^

# Downloader de Vídeos e Áudios do YouTube 

Este é um script de console em Python desenvolvido para baixar vídeos e áudios do YouTube, oferecendo controle sobre a qualidade desejada. O projeto utiliza a biblioteca `yt-dlp` para uma interação robusta e atualizada com o YouTube.

## ✨ Funcionalidades

* **Listagem de Formatos:** Exibe uma lista detalhada de todas as qualidades de vídeo e áudio disponíveis para um determinado link.
* **Seleção de Qualidade:** Permite ao usuário escolher um formato específico de vídeo, áudio, ou uma combinação de ambos para obter a melhor qualidade.
* **Download Inteligente:** Utiliza o FFmpeg para juntar os melhores streams de vídeo e áudio que o YouTube oferece separadamente.
* **Tratamento de Links:** Foca no vídeo principal e ignora playlists automaticamente para evitar downloads indesejados.
* **Nomenclatura Automática:** Salva os arquivos com o título original do vídeo, removendo caracteres inválidos.

## 📋 Pré-requisitos

Antes de executar este projeto, certifique-se de que você tem os seguintes softwares instalados em seu sistema:

1.  **Python:** Versão **3.9 ou superior** é recomendada.
2.  **FFmpeg:** Uma ferramenta essencial que o `yt-dlp` usa para juntar (mux) os arquivos de vídeo e áudio.
    * **Download:** [FFmpeg Official Builds](https://www.gyan.dev/ffmpeg/builds/)
    * **Instalação:** É crucial que o `ffmpeg` esteja no PATH do seu sistema para que o script possa encontrá-lo.

## 🚀 Instalação e Configuração

Siga os passos abaixo para configurar o ambiente e rodar o projeto.

1.  **Clone ou baixe os arquivos** para uma pasta em seu computador.

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

## 💻 Como Usar

Para executar o script, siga os passos abaixo no seu terminal (como o Terminal do PyCharm ou o Prompt de Comando do Windows).

1.  **Navegue até a pasta do projeto:**
    ```bash
    # Exemplo: se a pasta está na sua Área de Trabalho
    cd Desktop/downloader_youtube_final
    ```

2.  **Ative o ambiente virtual** (se ainda não estiver ativo):
    ```bash
    .\venv\Scripts\activate
    ```

3.  **Execute o script principal:**
    ```bash
    python baixar_video.py
    ```

4.  **Siga as instruções na tela:**
    * O programa irá primeiro pedir o link do vídeo. Cole a URL e pressione `Enter`.
    * Em seguida, ele analisará o vídeo e exibirá uma lista de todos os formatos e qualidades disponíveis, cada um com um `ID`.
    * Analise a lista e decida qual formato baixar. As instruções na tela te guiarão sobre como fazer a escolha (baixar apenas um ID, combinar um ID de vídeo e áudio, ou simplesmente pressionar `Enter` para a melhor qualidade).
    * Após fazer sua escolha, o download começará automaticamente.

### Exemplo de uma Sessão no Terminal

Abaixo está um exemplo de como será a interação, do início ao fim.

```text
(venv) C:\Users\Chiculol\Desktop\downloader_youtube_final> python baixar_video.py
--- Bem-vindo ao baixador de vídeos do Chiculol ^^ (Versão 3.1) ---
Por favor, cole o link do vídeo: [https://www.youtube.com/watch?v=dQw4w9WgXcQ](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

Analisando o vídeo: 'Rick Astley - Never Gonna Give You Up (Official Music Video)'

--- Formatos de vídeo e áudio disponíveis ---
ID: 249   | Ext: webm   | Resolução: Áudio           | Tamanho: ~548.33 KB
ID: 250   | Ext: webm   | Resolução: Áudio           | Tamanho: ~711.53 KB
ID: 140   | Ext: m4a    | Resolução: Áudio           | Tamanho: ~1.33 MB
ID: 251   | Ext: webm   | Resolução: Áudio           | Tamanho: ~1.34 MB
ID: 18    | Ext: mp4    | Resolução: 640x360         | Tamanho: ~6.59 MB
ID: 22    | Ext: mp4    | Resolução: 1280x720        | Tamanho: ~12.28 MB
ID: 136   | Ext: mp4    | Resolução: 1280x720        | Tamanho: ~11.02 MB
ID: 137   | Ext: mp4    | Resolução: 1920x1080       | Tamanho: ~21.78 MB

--- Como Escolher ---
1. Para a melhor qualidade, escolha um ID de vídeo e um ID de áudio (ex: 137+140).
2. Para um arquivo único com vídeo e áudio (qualidade até 720p), digite um ID (ex: 22).
3. Para apenas o áudio, escolha um ID que tenha 'Áudio' na resolução.
4. Para deixar o programa escolher a melhor qualidade, apenas pressione ENTER.

Digite o(s) ID(s) desejado(s): 137+140

Você escolheu o formato: 137+140

Iniciando o download... Isso pode demorar.
[youtube] Extracting URL: [https://www.youtube.com/watch?v=dQw4w9WgXcQ](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
[info] dQw4w9WgXcQ: Downloading 1 format(s): 137+140
[download] Destination: Rick Astley - Never Gonna Give You Up (Official Music Video).f137.mp4
[download] 100% of   21.78MiB in 00:00:02 at 8.79MiB/s
[download] Destination: Rick Astley - Never Gonna Give You Up (Official Music Video).f140.m4a
[download] 100% of    1.33MiB in 00:00:00 at 5.76MiB/s
[Merger] Merging formats into "Rick Astley - Never Gonna Give You Up (Official Music Video).mp4"
Deleting original file Rick Astley - Never Gonna Give You Up (Official Music Video).f137.mp4 (pass -k to keep)
Deleting original file Rick Astley - Never Gonna Give You Up (Official Music Video).f140.m4a (pass -k to keep)

--- Download concluído com sucesso! ---
O arquivo foi salvo na pasta do projeto.

(venv) C:\Users\Chiculol\Desktop\downloader_youtube_final>

---
_Gerado em 17 de Agosto de 2025._
