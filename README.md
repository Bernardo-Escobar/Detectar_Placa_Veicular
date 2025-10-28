# Detectar_Placa_Veicular

## 🚗 Detectar Placa Veicular — Localização de Caracteres
Repositório desenvolvido como parte da **Avaliação M2** da disciplina de **Processamento de Imagens** da **Universidade do Vale do Itajaí (UNIVALI)**.


## 🎯 Objetivo
Aplicar **métodos clássicos de segmentação de imagens** para **localizar caracteres em placas veiculares** sem o uso de modelos de **deep learning** ou **redes neurais**.

O projeto busca identificar e isolar os **7 caracteres alfanuméricos** das placas, utilizando apenas técnicas tradicionais de processamento digital de imagens.


## 🧠 Abordagem
O código foi desenvolvido em **Python (Jupyter Notebook / Google Colab)**, utilizando **OpenCV**, **NumPy** e **Matplotlib**, e implementa um *pipeline* completo de processamento para segmentação dos caracteres.

### 🧩 Etapas do pipeline
1. **Pré-processamento:**
    - Conversão para tons de cinza (cv2.cvtColor)
    - Remoção de ruídos com GaussianBlur
    - Equalização do histograma
      
2. **Detecção de bordas:**
    - Operadores Canny para destacar contornos relevantes
  
3. **Limiarização:**
    - Aplicação de limiar Otsu e limiar adaptativo
    - Geração de máscara binária para separação fundo/objeto
    
4. **Rotulagem e filtragem:**
    - Detecção de componentes conectados
    - Filtro por área e proporção para eliminar falsos positivos
      
5. **Extração dos caracteres:**
    - Delimitação por bounding boxes (retângulos)
    - Exibição das regiões dos caracteres segmentados

6. **Avaliação de desempenho:**
    - Cálculo de IoU (Intersection over Union) para comparar detecções com as anotações reais
    - Comparação com o método base fornecido (≈60% IoU)

## 🧰 Tecnologias Utilizadas
- **Python 3.x**
- **Google Colab / Jupyter Notebook**
- **OpenCV (cv2)**
- **NumPy**
- **Matplotlib**

## ⚙️ Como Executar
1. Acesse o notebook do projeto:
👉 [Abrir no Google Colab](https://colab.research.google.com/drive/15Xywwfl_f4fRrv6t0JjUtbPGHHIloKqI?usp=sharing)

2. Faça o upload do conjunto de imagens de placas:
[📦 Dataset — placas veiculares](https://drive.google.com/file/d/1Q1oebfpr_3uf6Raiu88D9G5fBmqdhQsB/view?usp=drive_link)

3. Execute todas as células sequencialmente.

4. O notebook gerará:
    - Máscaras segmentadas das placas;
    - Bounding boxes dos caracteres detectados;
    - Métricas de desempenho (IoU, precisão e recall).
      
## 🧪 Resultados Obtidos
- **Média de IoU:** superior ao método base de referência (~60%)
- **Precisão e Recall:** indicam boa consistência na segmentação dos 7 caracteres
- **Visualização:** exibição clara das regiões segmentadas em cada placa

## ⚖️ Restrições
- 🚫 Não utilizar deep learning, redes neurais ou modelos pré-treinados (ex: YOLO, OCR, etc.)
- ✅ Apenas métodos clássicos são permitidos:
    - Limiarização (Otsu, adaptativa)
    - Detecção de bordas (Sobel, Canny)
    - Segmentação (Watershed, Superpixels, Region Growing)
    - Operações morfológicas
    - Clusterização (K-Means, se aplicável)

## 📄 Estrutura do Repositório
```bash
Detectar_Placa_Veicular/
├── Trabalho_M2.ipynb      # Código principal (notebook)
├── Readme.md             # Este arquivo (documentação)
```

## 👨‍💻 Autoria
Projeto desenvolvido por alunos da Universidade do Vale do Itajaí (UNIVALI)

Disciplina: Processamento de Imagens – M2 (2025/1)

Professor: MSc. George de Borba Nardes

## 📝 Licença
Uso acadêmico e educacional. Livre para consulta e aprendizado.
