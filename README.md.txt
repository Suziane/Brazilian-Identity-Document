# Repositório da Dissertação de Mestrado  

Este repositório faz parte da dissertação de mestrado **“EXTRACTING FIELDS IN BRAZILIAN NATIONAL DRIVER’S LICENSE: A STUDY FOCUSING ON DEEP LEARNING TEXT RECOGNITION METHODS”**, cujo objetivo é investigar métodos de reconhecimento de texto baseados em *deep learning* aplicados à extração de campos na Carteira Nacional de Habilitação (CNH) brasileira.  

O repositório reúne os conjuntos de dados, modelos, anotações, resultados e scripts utilizados ao longo do trabalho, permitindo a reprodutibilidade dos experimentos apresentados na dissertação.  

---

## 📂 Estrutura do Repositório  

O repositório está organizado em diferentes diretórios, cada um com uma função específica no processo experimental:  

- **`novas_anotacoes/`**  
  Contém a adaptação dos *ground truth* de referência oriundos do **BID dataset** [^1], utilizados como base para validação e comparação dos resultados.  

- **`yolo/`**  
  Reúne os arquivos de *labels* normalizados, bem como o modelo YOLO treinado, empregado na etapa de detecção de regiões de interesse.  

- **`referencia/`**  
  Inclui os arquivos de referência utilizados na comparação dos resultados de OCR, funcionando como conjunto de apoio para a avaliação dos experimentos.  

- **`ocr/`**  
  Abriga os resultados e métricas obtidos em cada amostra para os diferentes modelos de OCR considerados:  
  - TrOCR Small  
  - TrOCR Base  
  - TrOCR Large  
  - Tesseract  
  - GPT-4o  
  - GPT-4o-mini  

- **`algoritmo/`**  
  Contém os scripts responsáveis pelas principais etapas do experimento, incluindo:  
  - Correção da rotação das imagens  
  - Recorte das regiões de interesse  
  - Criação das novas anotações (*ground truth* adaptados)  
  - Treinamento do modelo YOLO  
  - Execução do OCR em cada um dos métodos avaliados  
  - Formatação dos resultados do GPT  
  - Cálculo das métricas de desempenho  
  - Aplicação do teste estatístico de Wilcoxon  

---

## 📖 Referência  

[^1]:  
```bibtex
@inproceedings{sibgrapi_estendido,
  author    = {Álysson Soares and Ricardo das Neves Junior and Byron Bezerra},
  title     = {BID Dataset: a challenge dataset for document processing tasks},
  booktitle = {Anais Estendidos da XXXIII Conference on Graphics, Patterns and Images},
  location  = {Evento Online},
  year      = {2020},
  keywords  = {},
  issn      = {0000-0000},
  pages     = {143--146},
  publisher = {SBC},
  address   = {Porto Alegre, RS, Brasil},
  doi       = {10.5753/sibgrapi.est.2020.12997},
  url       = {https://sol.sbc.org.br/index.php/sibgrapi_estendido/article/view/12997}
}
