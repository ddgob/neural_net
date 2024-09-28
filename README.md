# neural_net

## Este projeto implementa uma rede neural de 3 camadas para reconhecer dígitos do dataset MNIST. O notebook explora os efeitos de vários hiperparâmetros no desempenho do modelo, incluindo o número de unidades na camada oculta, o algoritmo de otimização e a taxa de aprendizagem.

## Estrutura do Projeto

- `neural_net.ipynb`: O notebook principal contendo a implementação da rede neural, treinamento e avaliação.

## Ajuste de Hiperparâmetros

Os seguintes hiperparâmetros foram ajustados para avaliar seu impacto na performance do modelo:

1. **Número de Unidades na Camada Oculta:**
    - 25 unidades
    - 50 unidades
    - 100 unidades
2. **Algoritmo de Otimização:**
    - Gradiente Descendente (Batch Completo)
    - Gradiente Descendente Estocástico (SGD)
    - Gradiente Descendente por Mini-Batch
        - Tamanhos de mini-batch: 10, 50
3. **Taxa de Aprendizagem:**
    - 0.5
    - 1
    - 10

## Resultados

Os resultados mostraram que o modelo selecionado, com os seguintes hiperparâmetros, obteve o melhor desempenho:

- **Unidades Ocultas:** 50
- **Tamanho do Mini-Batch:** 10
- **Taxa de Aprendizagem:** 1

## Métricas de Desempenho

- **Precisão de Teste:** 93,73%
- **Perda de Teste:** 0.3278
- **Perda de Treinamento:** 0.0005

## Principais Descobertas

- **Unidades Ocultas:** Um equilíbrio entre poucas (25 unidades) e muitas (100 unidades) unidades proporcionou os melhores resultados.
- **Tamanho do Mini-Batch:** O Mini-Batch (10) ofereceu um bom balanço entre descida ruidosa (SGD) e descida menos generalizada (Batch Completo).
- **Taxa de Aprendizagem:** Uma taxa de aprendizagem de 1 evitou divergência (alta taxa de aprendizagem) e convergência lenta (taxa de aprendizagem baixa).

## Como Usar

1. Clone este repositório.
2. Abra o notebook `neural_net.ipynb` no Jupyter Notebook ou Jupyter Lab.
3. Execute as células para treinar e avaliar a rede neural.

## Dependências

Certifique-se de ter as seguintes dependências instaladas:

- Python 3.x
- Jupyter Notebook
- NumPy
- Pytorch
- Matplotlib

Instale as dependências usando:

```sh
pip install numpy torch matplotlib jupyter