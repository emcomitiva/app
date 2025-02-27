Este notebook implementa uma solução completa para análise estatística e visualização de dados educacionais, com foco na comparação entre grupos de estudantes. O código realiza testes estatísticos (teste t de Welch) e gera visualizações estilizadas em tema escuro com elementos neon para melhor interpretação dos resultados.

## Funcionalidades

O notebook inclui as seguintes funcionalidades principais:

- Integração com Google Drive para armazenamento persistente de resultados
- Carregamento de dados de uma planilha online
- Análise estatística comparativa entre dois grupos
- Geração automatizada de múltiplos tipos de visualizações:
  - Boxplots
  - Gráficos de violino (violin plots)
  - Gráficos de densidade KDE (Kernel Density Estimation)
  - Gráficos de linha

## Variáveis Analisadas

O código está configurado para analisar as seguintes métricas educacionais:

- Satisfação
- Pertencimento
- Participação em fóruns
- Interações com colegas
- Desempenho
- Centralidade de grau (análise de redes)
- Nível de interesse
- Horas de estudo

## Aspectos Técnicos

### Pré-requisitos

O notebook requer as seguintes bibliotecas Python:
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- google.colab

### Estrutura de Funções

1. `mount_google_drive()`: Monta o Google Drive no ambiente Colab
2. `ensure_directory_exists_on_drive()`: Garante que um diretório específico exista no Drive
3. `create_figure()`: Cria uma figura matplotlib com tema escuro personalizado
4. `save_fig()`: Salva uma figura no Google Drive com alta resolução
5. `plot_boxplot()`: Cria e salva boxplots comparativos
6. `plot_violin()`: Cria e salva violin plots para análise de distribuição
7. `plot_kde()`: Cria e salva gráficos de densidade Kernel (KDE)
8. `plot_line()`: Cria e salva gráficos de linha para análise de tendências
9. `analisar_dados()`: Função principal que coordena a análise estatística e geração de visualizações

### Design Visual

As visualizações são criadas com um tema escuro (#282828) e elementos em cores neon (ciano #00FFFF para textos e verde #00FF00 para linhas), proporcionando contraste visual e estética moderna. Os gráficos são gerados com alta resolução (300 dpi) e salvos automaticamente no Google Drive.

### Tratamento de Erros

O código implementa tratamento robusto de erros, incluindo:
- Verificação da existência de colunas
- Tratamento de tipos de dados (conversão de string para numérico)
- Substituição de vírgulas por pontos em valores decimais
- Remoção de valores ausentes
- Captura e reporte de exceções

## Uso

1. Execute o notebook em um ambiente Google Colab
2. O código montará automaticamente o Google Drive
3. Os dados serão carregados da URL especificada
4. As análises estatísticas serão realizadas e impressas no console
5. As visualizações serão salvas no diretório 'data' no Google Drive

## Resultados

Para cada variável analisada, o notebook gera:
- Resultados do teste t de Welch (estatística t, valor p, graus de liberdade)
- Boxplot comparativo entre os grupos
- Violin plot para análise da distribuição
- Gráfico KDE para visualização da densidade de probabilidade

## Autor

Hélio Craveiro Pessoa Júnior
