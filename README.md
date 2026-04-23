# Doutorado UFLA — Geração e Validação de Base de Dados Sintética para Análise de Potencial Hídrico

> **Tese de Doutorado** — Programa de Pós-Graduação em Engenharia Agrícola  
> Universidade Federal de Lavras (UFLA)

---

## 📋 Sobre a pesquisa

Esta pesquisa desenvolveu uma metodologia estatística para **geração e validação de bases de dados sintéticas** a partir exclusivamente de **estatísticas descritivas agregadas** (médias, desvios padrão, quartis e matrizes de correlação), com aplicação ao monitoramento do **potencial hídrico de plantas** em Engenharia Agrícola.

A abordagem permite reproduzir bases de dados estatisticamente equivalentes às originais **sem acesso aos dados brutos**, o que abre caminho para pesquisa reproduzível, preservação de privacidade e redução de custos com coleta de campo.

---

## 🎯 Resultados principais

| Métrica | Resultado |
|---|---|
| Similaridade KS (média) | **89,71 %** |
| Similaridade de Correlação | **81,28 %** |
| Variáveis com similaridade ≥ 90 % | 61 de 102 (59,8 %) |
| Variáveis com baixa discrepância (KS ≤ 0,15) | 78 de 102 (76,5 %) |

---

## 📁 Estrutura do repositório

```
Doutorado_UFLA/
│
├── notebooks/
│   ├── 01_geracao_dados_sinteticos.ipynb   # Pipeline de geração da base sintética
│   └── 02_validacao_estatistica.ipynb      # Cálculo das métricas de validação
│
├── data/
│   ├── sintetica/                          # Base sintética gerada (disponível publicamente)
│   └── estatisticas_descritivas/           # Estatísticas descritivas utilizadas como input
│
└── README.md
```

> **Nota:** Os dados originais não estão disponíveis neste repositório, mas podem ser acessados [Neste Site](http://www.aia.ufla.br/home/filesdatasets/). A base sintética gerada está disponível livremente na pasta `data/sintetica/`.

---

## 🚀 Como usar

### Pré-requisitos

```bash
Python >= 3.9
```

### Instalação das dependências

```bash
pip install numpy pandas scipy scikit-learn matplotlib seaborn
```

### Executar no Google Colab

Clique no badge abaixo para abrir diretamente no Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/zolpy/Doutorado_UFLA/blob/main/notebooks/01_geracao_dados_sinteticos.ipynb)

### Executar localmente

```bash
git clone https://github.com/zolpy/Doutorado_UFLA.git
cd Doutorado_UFLA
jupyter notebook notebooks/
```

---

## 🔬 Metodologia resumida

1. **Input:** estatísticas descritivas publicadas (média, desvio padrão, quartis, matriz de correlação)
2. **Geração:** amostras multivariadas via decomposição de Cholesky com ajuste de momentos
3. **Validação:** comparação com as estatísticas originais por meio de KS Similarity, Correlation Similarity e Frobenius Norm

A metodologia é uma alternativa viável a métodos neurais generativos (GANs, VAEs) para situações em que **apenas estatísticas resumidas estão disponíveis**.

---

## 📊 Base sintética

A base sintética gerada está disponível publicamente e pode ser utilizada para:

- Testes e benchmarks de algoritmos
- Validação de modelos de machine learning
- Ensino e capacitação em análise de dados
- Desenvolvimento de novas metodologias sem acesso a dados sensíveis

---

## 📄 Citação

Se você utilizar este código ou a base sintética em sua pesquisa, por favor cite:

```bibtex
@phdthesis{zolpy2025sintetica,
  title     = {Geração e Validação de Base de Dados Sintética para Análise
               de Potencial Hídrico a partir de Estatísticas Descritivas
               em Engenharia Agrícola},
  author    = {Luiz Carlos Brandão Junior},
  school    = {Universidade Federal de Lavras},
  year      = {2025},
  type      = {Tese (Doutorado em Engenharia Agrícola)},
  url       = {https://github.com/zolpy/Doutorado_UFLA}
}
```

---

## 🌱 Alinhamento com os ODS da ONU

Este trabalho contribui diretamente para:

- **ODS 4** — Educação de Qualidade: democratização do acesso a dados para ensino e pesquisa
- **ODS 6** — Água Potável e Saneamento: monitoramento do potencial hídrico e uso eficiente da água
- **ODS 9** — Inovação e Infraestrutura: desenvolvimento de metodologia e software aberto
- **ODS 12** — Consumo e Produção Responsáveis: reutilização de dados já publicados
- **ODS 17** — Parcerias: compartilhamento aberto de metodologia e código

---

## 📬 Contato

**Autor:** [Luiz Carlos Brandão Junior]  
**Instituição:** Universidade Federal de Lavras — UFLA  
**Programa:** Pós-Graduação em Engenharia Agrícola  
**GitHub:** [@zolpy](https://github.com/zolpy)
**Site:** [Site](https://www.uflaniano.com.br/)
---

## 📝 Licença

Este projeto está licenciado sob a licença [MIT](LICENSE) — sinta-se livre para usar, modificar e distribuir com atribuição.
