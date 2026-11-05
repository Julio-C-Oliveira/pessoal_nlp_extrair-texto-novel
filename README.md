# pessoal_nlp_extrair-texto-novel

Pipeline em Python para **Processamento de Linguagem Natural (NLP Heurístico)** e saneamento de fluxos de texto brutos extraídos de digitalizações e OCR de livros e light novels.

---

## 📝 Engenharia de Regras e Saneamento

- **Detecção de Códigos ASCII/Unicode:** Classificação de caracteres via funções lambda sobre faixas numéricas de código, preservando diacríticos e acentuações da língua portuguesa (códigos 224 a 382).
- **Remoção de Caracteres Espúrios:** Eliminação de quebras de página de OCR (`\x0c`) e símbolos de controle inválidos.
- **Reconstrução Inteligente de Parágrafos:**
  - Fusão de linhas quebradas artificialmente caso a sentença anterior termine em vírgula ou caso a linha seguinte inicie com letra minúscula.
  - Reconexão de translineações silábicas por hífen (código ASCII 45).
- **Proteção Estrutural de Cabeçalhos:**
  - Preservação e formatação padronizada de títulos de capítulos e seções (*Parte n*, *Capítulo n*, *Volume n*).

---

## 🛠️ Tecnologias

- **Python 3.9+** (Expressões Regulares, Manipulação de Encodings e I/O de Streams)

---

## 📦 Como Executar

```bash
python3 Extrair_Texto_de_Novel.py
```

---

## 📄 Licença
Distribuído sob a licença MIT. Veja `LICENSE` para mais detalhes.
