# 🧠 llm-comparison-huggingface
## Análise Comparativa de Eficiência em LLMs Open-Source: Gemma 2B vs. Mistral 7B

Este repositório contém o código e os resultados de uma atividade acadêmica focada em **Benchmark e Análise de Desempenho (Performance)** de Modelos de Linguagem Grande (LLMs) abertos usando a biblioteca **Hugging Face Transformers** em Python.

O objetivo é avaliar o *trade-off* entre **custo computacional (latência)** e **qualidade da resposta** ao comparar um modelo leve (Gemma 2B) com um modelo de tamanho médio (Mistral 7B) em tarefas de raciocínio e codificação.

---

## 🎯 Objetivo e Metodologia

### Modelos Comparados

| Modelo | Tamanho (Parâmetros) | Arquitetura | Características Principais |
| :--- | :--- | :--- | :--- |
| **Gemma 2B** | $2.5 \text{ Bilhões}$ | Google (Arquitetura Gemini) | Leve, rápido e otimizado para inferência eficiente. |
| **Mistral 7B Instruct** | $7.3 \text{ Bilhões}$ | Mistral AI | Alto desempenho, conhecido por ser o melhor modelo em sua classe de tamanho. |

### Stack Tecnológico

* **Linguagem:** Python
* **Frameworks:** PyTorch, Pandas
* **Biblioteca LLM:** Hugging Face Transformers
* **Otimização:** **BitsAndBytes** para carregamento em **4-bit Quantization** (necessário para rodar o Mistral 7B na GPU T4 do Colab).
* **Ambiente de Execução:** Google Colab (GPU T4)

### Métricas de Avaliação

1.  **Latência (Tempo de Inferência):** Tempo gasto (em segundos) para gerar a resposta para cada *prompt*.
2.  **Qualidade da Resposta:** Avaliação qualitativa da coerência, precisão e completude das respostas (em especial para *prompts* de código e lógica).

---

## 🛠️ Como Executar

O projeto foi desenvolvido para rodar no **Google Colab**.

1.  **Configuração de GPU:** Certifique-se de que o ambiente de execução (Runtime) está configurado para **T4 GPU** (Menu Runtime -> Change runtime type).
2.  **Autenticação:** O modelo Gemma é *gated* (restrito). É necessário possuir uma conta no Hugging Face, aceitar a licença do modelo e inserir seu **Access Token** na célula de login.
3.  **Execução:** Abra o arquivo `comparacao_llm.ipynb` e execute todas as células sequencialmente.

---

## 📂 Conteúdo do Repositório

* `comparacao_llm.ipynb`: O Notebook Python com todo o código de instalação, carregamento, inferência e *benchmark*.
* `apresentacao.pdf`: Slides resumindo o problema, a solução e os resultados.
* `benchmark_resultados.csv`: (Gerado após a execução) Tabela com os tempos de latência e as respostas truncadas de cada modelo.

---

## 👥 Integrantes do Projeto (Caso seja em Grupo)

* Fábio Stampone Miranda *
* Rafael Souza de Mello *
* Pedro Alves de Matos *
