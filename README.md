# 📘 Caderno Temático: Fundamentos de Redes Neurais

## 🎯 Contexto e Objetivos
**Assunto escolhido**: Redes neurais artificiais – conceitos básicos, perceptron, backpropagation e aplicações práticas.

**Objetivos de estudo**:
- Compreender o funcionamento de um neurônio artificial.
- Diferenciar as principais arquiteturas (Perceptron, MLP, redes convolucionais).
- Implementar mentalmente um fluxo de treinamento com backpropagation.
- Criar prompts reutilizáveis para revisão rápida do tema.

## 📚 Curadoria de Fontes (3 a 5 links/PDFs)
Usei estes materiais abertos no NotebookLM:

1. **Capítulo de livro** – *Neural Networks and Deep Learning* (Michael Nielsen)  
   → [http://neuralnetworksanddeeplearning.com/chap1.html](http://neuralnetworksanddeeplearning.com/chap1.html)

2. **Artigo científico introdutório** – *A Gentle Introduction to Neural Networks* (Analytics Vidhya)  
   → [https://www.analyticsvidhya.com/blog/2021/04/a-gentle-introduction-to-neural-networks/](https://www.analyticsvidhya.com/blog/2021/04/a-gentle-introduction-to-neural-networks/)

3. **PDF didático** – *Redes Neurais: Conceitos e Aplicações* (UNICAMP – material de apoio)  
   → [Link para PDF público](https://www.dca.fee.unicamp.br/cursos/EA080/redesneurais.pdf)

4. **Vídeo transcrito** (converti para PDF) – *But what is a neural network?* (3Blue1Brown)

> ⚠️ Todos os arquivos foram carregados no NotebookLM como fonte para responder perguntas.

## 🧪 Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

### ✔️ Prompts que funcionaram bem
| Prompt | Resposta obtida | O que aprendi |
|--------|----------------|----------------|
| "Explique o conceito de função de ativação como se eu tivesse 15 anos, usando analogias." | A IA usou a analogia de um interruptor com intensidade variável (não só liga/desliga). | Pedir nível de escolaridade ou analogia funciona muito bem. |
| "Compare ReLU e Sigmoid em uma tabela: vantagens, desvantagens e quando usar." | Tabela clara, com exemplos de uso (sigmoid para saída binária, ReLU para camadas internas). | Prompt pedindo formato tabela + critérios específicos é eficiente. |

### ❌ Dificuldades / Cicatrizes (troubleshooting)
**Problema 1**: Ao pedir "mostre a fórmula do backpropagation", a IA deu uma fórmula muito genérica e sem contexto.

- **O que tentei**: Reformulei para: "Com base apenas nos PDFs carregados, explique passo a passo a backpropagation para uma rede de 2 camadas, mostrando as equações e o que cada símbolo significa."
- **Resultado**: Resposta muito melhor, com referência direta às fontes e variáveis explicadas.

**Problema 2**: A IA começou a inventar um exemplo de código em Python que não estava nos materiais.

- **Solução**: Usei o comando: "Ignore qualquer conhecimento prévio. Responda **exclusivamente** com base no conteúdo dos arquivos enviados. Se não encontrar, diga 'não disponível nas fontes'."
- **Liçao**: Sempre explicitar a restrição de fontes quando quiser fidelidade total.

## 📖 Miniguia de Estudo (Entrega Final)

### 🔹 Resumos estruturados
**Perceptron**  
- Modelo mais simples de neurônio artificial.  
- Entradas (x) multiplicadas por pesos (w), somadas, passadas por uma função degrau.  
- Usado para classificação linearmente separável (AND, OR, mas não XOR).

**Backpropagation em 3 frases**  
1. Calcula o erro da saída final.  
2. Propaga esse erro para trás, ajustando os pesos camada por camada usando a regra da cadeia (cálculo).  
3. Repete por várias épocas até o erro ser pequeno.

### 🔹 Glossário
| Termo | Definição (fonte: materiais) |
|-------|------------------------------|
| **Época** | Uma passagem completa de todos os exemplos de treinamento pela rede. |
| **Gradiente descendente** | Algoritmo que minimiza o erro ajustando os pesos na direção oposta ao gradiente. |
| **Overfitting** | Quando a rede decora os dados de treino, mas não generaliza para novos dados. |

### 🔹 Conjunto de Prompts Reutilizáveis (para revisão futura)
```text
1. "Me dê um resumo de uma página sobre [conceito] baseado nos materiais carregados."
2. "Crie 5 perguntas estilo 'flashcard' sobre [tópico] com respostas curtas e diretas."
3. "Explique a diferença entre [termo A] e [termo B] usando uma analogia com uma situação do dia a dia."
4. "Mostre um exemplo numérico passo a passo de [algoritmo/cálculo] com números pequenos."
5. "Quais são os 3 erros mais comuns de iniciantes ao aprender [assunto]? Liste com explicações."
