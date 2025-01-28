# 📹 YouTube2Frames

## 📝 Descrição
Este projeto foi desenvolvido para realizar o download de vídeos do YouTube, extrair frames, aplicar filtros de nitidez, identificar objetos em frames utilizando o YOLOv3, e selecionar os melhores frames com base em cenas únicas. Por fim, os resultados são compactados e disponibilizados para download.

---

## ⚙️ Funcionalidades
1. **Download de vídeos do YouTube**:
   - Utiliza `yt_dlp` para baixar vídeos na resolução configurada.
   - Mantém a estrutura de diretórios organizada e limpa.

2. **Extração de frames**:
   - Extrai frames do vídeo baixado utilizando OpenCV.
   - Permite configuração do intervalo de frames a serem extraídos.

3. **Filtragem por nitidez**:
   - Calcula a nitidez de cada frame e descarta aqueles com baixa qualidade.
   - Salva apenas os frames nítidos em um diretório separado.

4. **Detecção de objetos com YOLOv3**:
   - Utiliza a biblioteca YOLOv3 para detectar objetos em frames filtrados.
   - Salva frames contendo objetos detectados em um diretório específico.

5. **Seleção de frames únicos**:
   - Compara frames consecutivos utilizando histogramas para identificar cenas únicas.
   - Seleciona o frame mais nítido de cada cena.

6. **Compactação e download**:
   - Compacta os resultados (frames únicos) em arquivos `.zip` para download.

---

## 📂 Estrutura de Diretórios
- `project/downloaded`: Armazena os vídeos baixados.
- `project/frames/frames_extraidos`: Frames extraídos do vídeo.
- `project/frames/frames_filtrados`: Frames filtrados com base na nitidez.
- `project/frames/frames_com_objetos`: Frames contendo objetos detectados.
- `project/frames/frames_unicos`: Frames selecionados como únicos com base nas cenas.
- `project/yolo`: Diretório para os arquivos de configuração e pesos do YOLOv3.
- `project/zipped`: Arquivos compactados com os resultados.

---

## 🛠️ Configuração e Dependências
### 📚 Bibliotecas Necessárias
- `yt_dlp`: Para download de vídeos do YouTube.
- `cv2` (OpenCV): Para processamento de imagens e vídeos.
- `numpy`: Para cálculos de diferença entre frames.
- `shutil`: Para manipulação de diretórios e compactação.
- `os`: Para manipulação de arquivos e diretórios.

### 🧩 Instalação das Dependências
```bash
pip install yt-dlp opencv-python numpy
