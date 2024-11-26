### README: Análise de Dados Textuais e Redes Semânticas

#### Visão Geral
Este repositório contém um script em Python desenvolvido para realizar análises exploratórias e visualizações de dados textuais. Ele foi projetado para processar, limpar e analisar respostas abertas de um conjunto de dados em Excel, gerando insights por meio de visualizações como nuvens de palavras e redes semânticas.

#### Funcionalidades
O código realiza as seguintes etapas:
1. **Limpeza de Texto**:
   - Remoção de stop words (palavras comuns irrelevantes) e caracteres não alfabéticos.
   - Conversão de texto para letras minúsculas e normalização de espaços.

2. **Análise de Frequência**:
   - Identifica as palavras mais frequentes em cada coluna de texto.
   - Exibe as 10 palavras mais comuns por coluna.

3. **Visualização com Nuvem de Palavras**:
   - Gera visualizações para representar graficamente as frequências das palavras.

4. **Agrupamento de Respostas Similares (Clusters)**:
   - Utiliza o algoritmo KMeans para agrupar respostas em categorias com base na similaridade semântica.

5. **Análise de Similitude e Redes Semânticas**:
   - Calcula a similaridade entre termos utilizando a métrica de cosseno.
   - Cria redes semânticas ajustadas com base nas co-ocorrências, destacando termos mais fortemente conectados.

#### Pré-requisitos
Certifique-se de ter os seguintes pacotes instalados no seu ambiente Python:
- `pandas`
- `re`
- `collections`
- `scikit-learn`
- `matplotlib`
- `wordcloud`
- `networkx`

Você pode instalar os pacotes necessários executando:
```bash
pip install pandas scikit-learn matplotlib wordcloud networkx
```

#### Como Usar
1. **Preparar os Dados**:
   - O script espera um arquivo Excel (`.xlsx`) contendo colunas com respostas abertas.
   - Atualize o caminho do arquivo no código para o local correto: `file_path = 'caminho/do/arquivo.xlsx'`.

2. **Executar o Código**:
   - Execute o script para processar os dados, gerar análises e criar visualizações.

3. **Saída**:
   - **Nuvens de palavras**: Uma nuvem para cada coluna de texto.
   - **Clusters**: As respostas serão agrupadas e categorizadas.
   - **Redes Semânticas**: Gráficos que destacam as relações entre os termos.

#### Estrutura do Script
1. **Limpeza de Texto**:
   - Função `clean_text`: Remove caracteres indesejados e aplica regras de limpeza.
2. **Análise de Frequência**:
   - Contagem das palavras mais comuns em cada coluna processada.
3. **Visualização com WordCloud**:
   - Gera nuvens de palavras para visualização rápida das palavras predominantes.
4. **Clusters com KMeans**:
   - Função `cluster_responses`: Agrupa respostas com base em seus vetores TF-IDF.
5. **Rede Semântica**:
   - Calcula a similaridade de cosseno entre os termos e exibe a rede com `NetworkX`.

#### Personalização
- **Stop Words**: As stop words podem ser ajustadas na variável `basic_stop_words`.
- **Número de Clusters**: Pode ser configurado na chamada da função `cluster_responses`.
- **Limiar de Similitude**: Ajuste a variável `higher_threshold` para refinar a criação das redes semânticas.

#### Exemplos de Aplicação
Este script pode ser usado em diversas áreas, incluindo:
- Análise de feedbacks qualitativos.
- Descoberta de padrões em respostas abertas de pesquisas.
- Visualização de redes semânticas em análises textuais.

#### Contribuições
Sinta-se à vontade para abrir *issues* ou enviar *pull requests* com melhorias ou sugestões.

#### Licença
Este repositório está sob a licença MIT. Sinta-se livre para utilizá-lo e modificá-lo conforme necessário.
