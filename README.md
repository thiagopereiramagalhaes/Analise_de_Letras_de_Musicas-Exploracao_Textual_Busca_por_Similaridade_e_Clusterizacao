# Análise de Letras de Músicas: Exploração Textual, Busca por Similaridade e Clusterização com TF-IDF e UMAP

## 1. O que é este projeto?

Este projeto utiliza ferramentas de Inteligência Artificial e Análise de Dados para explorar, pesquisar e organizar uma vasta coleção de letras de músicas. Ler e interpretar milhares de canções manualmente seria uma tarefa demorada e cansativa. Para resolver isto, este projeto cria um sistema capaz de ler todas as letras automaticamente, entender quais as palavras e sentimentos mais presentes, e organizar as músicas de forma inteligente.

O projeto divide-se em três grandes objetivos:
* **Exploração:** Descobrir as tendências do mundo da música, como quais são os artistas mais produtivos ou quais as palavras mais utilizadas nas composições (como "love" ou "time").
* **Buscador Inteligente:** Criar um mecanismo de pesquisa que consegue encontrar músicas não apenas pelo título, mas pela similaridade do texto, funcionando como um motor de busca de letras.
* **Agrupamento (Clusterização):** Organizar as músicas em "grupos" (clusters) com base nos seus temas. Em vez de organizar por género musical, o sistema junta músicas que "falam sobre a mesma coisa", descobrindo padrões líricos.

Em suma, este projeto resolve o problema de desorganização e excesso de informação em grandes volumes de texto, permitindo que amantes de música, produtores ou plataformas de *streaming* possam entender melhor o seu catálogo, criar recomendações baseadas no significado das letras e explorar tendências musicais de forma visual e intuitiva.

## 2. Como o fiz?

Todo o desenvolvimento foi realizado em linguagem Python, utilizando um documento interativo (*Jupyter Notebook*). O processo seguiu várias etapas para transformar o texto puro em informações úteis:

1. **Limpeza e Organização dos Dados:**
   * Recebemos uma base de dados contendo milhares de letras de músicas.
   * A primeira etapa consistiu em "limpar a casa": removemos registos incompletos ou duplicados para garantir que os algoritmos apenas iriam analisar dados de qualidade.
2. **Exploração Visual:**
   * Utilizámos ferramentas visuais, como uma "Nuvem de Palavras" (*Word Cloud*), para identificar de forma rápida quais as palavras mais cantadas.
   * Fizemos análises curiosas, como descobrir qual artista e qual música repetem mais vezes uma palavra específica (por exemplo, a palavra "know").
3. **Buscador de Similaridade:**
   * Desenvolvemos um sistema que calcula a "distância matemática" entre textos. Isto permite procurar por um trecho de letra e encontrar as músicas no catálogo que têm a letra mais parecida com a pesquisa.
4. **Agrupamento de Músicas por Tema (Clusterização):**
   * **Tradução de Texto para Números:** Como os computadores não entendem palavras, usámos uma técnica (*TF-IDF*) que transforma as letras em números, dando maior peso às palavras mais raras e significativas, e ignorando palavras comuns de ligação.
   * **Simplificação:** Reduzimos a complexidade desses números para que a Inteligência Artificial conseguisse focar-se apenas na informação mais importante.
   * **Criação dos Grupos:** Aplicámos um algoritmo chamado *K-Means* que agrupou automaticamente as músicas em 5 categorias distintas com base nas suas semelhanças temáticas.
   * **Visualização:** Por fim, utilizámos uma técnica avançada (*UMAP*) para comprimir toda essa informação num mapa visual 2D, permitindo-nos ver de forma clara como os diferentes grupos de músicas se separam e relacionam entre si num gráfico.
