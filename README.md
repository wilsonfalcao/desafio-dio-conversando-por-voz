# Desafio: Conversando por Voz com o ChatGPT via Whisper (OpenAI) e Python

Bem-vindo(a)! Este repositório contém a entrega do desafio de implementação de uma interface de voz utilizando o modelo **Whisper** da OpenAI para transcrição de áudio, integrado ao ambiente do Google Colab.

## 🎯 Objetivo
O foco principal deste projeto é a **transcrição de áudio em texto**, explorando a capacidade de processamento de linguagem natural do modelo Whisper. A implementação utiliza como base os conceitos e a estrutura de código fornecida por **Venilton**, adaptando-os para capturar áudio diretamente do navegador e processá-lo via Python.

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

Para que a comunicação entre o hardware (microfone) e o modelo de IA funcionasse perfeitamente no ambiente Cloud, foram implementadas as seguintes bibliotecas:

* **`whisper`**: O motor principal da OpenAI para o reconhecimento e transcrição da fala.
* **`IPython.display (Javascript, Audio)`**: Utilizados para injetar scripts que permitem ao navegador gravar áudio.
* **`google.colab.output`**: Essencial para a comunicação entre o back-end do Python e o front-end do notebook.
* **`base64`**: Para decodificar os dados de áudio capturados via JavaScript.
* **`IPython.core.interactiveshell`**: Para ajustes na execução das células do ambiente.

### Trecho de Importação Base:
```python
from IPython.core.interactiveshell import InteractiveShell
from IPython.display import Javascript, Audio
from google.colab import output
from base64 import b64decode
import whisper
