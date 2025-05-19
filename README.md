# Sistema de Análise Patológica 

### Identificação do Grupo - 2ESR (CodeBreakers)
- **558385** - Alexia Ramalho Izidio Dos Santos
- **554746** - Beatriz Vieira de Novais
- **559008** - Hellen Aparecida Moura Silva
- **557397** - Lorenzo Adinolfi Acquesta
- **558859** - Wendell Dos Santos Silva

## Descrição do Projeto

Este projeto foi desenvolvido como parte da Sprint 1 da disciplina de Dynamic Programming da FIAP orientada pelo professor Francisco Elanio Bezerra. Nossa equipe optou pelo desafio 2 proposto pela DASA, que consiste em desenvolver um sistema de análise patológica.
Desenvolvemos uma solução para análise de exames patológicos, permitindo o armazenamento e processamento de dados de amostras patológicas, sinais e cistos, com foco particular nas dimensões (altura, largura e comprimento) e características patológicas.

## Explicação das Hipóteses e Dados Considerados

### Base de Dados
Desenvolvemos uma estrutura de dados para representar análises patológicas de cinco pacientes hipotéticos sendo os membros da equipe: Hellen, Alexia, Wendell, Lorenzo e Beatriz. Cada exame inclui informações sobre lesões com suas respectivas características e dimensões. Os dados usados são fictícios, simulando o que seria obtido por visão computacional, como ainda estamos construindo o nosso sistema ainda não foi possível capturar esses dados para essa primeira entrega por isso optamos por usar dados fictícios para simular.


### Hipóteses Assumidas
1. **Parâmetros Relevantes**: Características como diâmetro, assimetria e bordas são indicadores importantes para avaliação de lesões de pele, baseando-nos na regra ABCDE usada por dermatologistas (Assimetria, Bordas, Cor, Diâmetro, Evolução).

2. **Valores de Referência**: Estabelecemos limiares para identificar lesões potencialmente problemáticas:
   - Diâmetro > 0.6cm como indicador de atenção
   - Assimetria > 0.5 (escala 0-1) como indicador de atenção
   - Volume > 0.5cm³ como indicador de atenção

3. **Categorização de Lesões**: Dividimos as lesões em diferentes tipos (pinta, cisto, sinal, mancha) com características distintas para permitir análise comparativa entre casos.

4. **Priorização Clínica**: Implementamos um sistema de prioridade (1-5) para organizar a análise dos casos por urgência, assumindo que características específicas exigem avaliação mais rápida.

## Técnicas de Programação Utilizadas

1. **Estruturas de Dados Aninhadas**: Utilizamos dicionários e listas aninhados para representar a hierarquia de informações médicas.

2. **Programação Dinâmica/Memorização**: Implementada para otimizar o processamento de dados recorrentes.

3. **Algoritmos de Busca Binária**: Aplicados para busca eficiente de pacientes por faixa etária.

4. **Estruturas de Fila**: Utilizadas para implementar uma fila de prioridade para análise de exames.

5. **Estruturas de Pilha**: Aplicadas para manter histórico de alterações de diagnósticos.

## Funcionalidades Implementadas

1. **Estrutura de Dados Aninhada**: Implementação de uma estrutura hierárquica para representar dados de pacientes e exames.

2. **Dicionário com Valores de Referência**: Criação de dicionário que compara valores examinados com valores de referência clínica.

3. **Extração de Exames por Paciente**: Função para extrair todos os exames de um paciente específico e criar um segundo dicionário.

4. **Fila de Prioridade**: Implementação de fila para organizar exames pendentes de acordo com sua urgência clínica.

5. **Busca Binária por Faixa Etária**: Algoritmo otimizado para buscar pacientes dentro de intervalos de idade específicos.

## Documentação de Código

### Normas de Codificação Seguidas
- **Padrões PEP 8**: Seguimos as diretrizes de estilo do Python Enhancement Proposal 8
- **Nomenclatura**: Utilizamos snake_case para variáveis e funções, CamelCase para classes
- **Docstrings**: Todas as funções e classes possuem docstrings explicativas
- **Comentários**: Adicionamos comentários em trechos complexos para facilitar entendimento
- **Organização**: Estruturamos o código em blocos funcionais para melhor legibilidade

### Estrutura do Código
- **Estrutura de Dados Base**: Definição do `database` com dados dos pacientes e exames
- **Funções de Processamento**: Funções para extrair, analisar e processar dados
- **Classes para Estruturas Específicas**: Implementações de fila de prioridade e outras estruturas
- **Funções de Demonstração**: Código para demonstrar o funcionamento das funcionalidades

## Requisitos Técnicos

- Python 3+
- pandas
- matplotlib
- numpy
- datetime

## Como Executar

1. Abra o código no Google Colab ou Jupyter Notebook (recomendado)
2. Execute as células em ordem
3. As funções de demonstração mostram o funcionamento de cada componente

## Conclusão

O sistema desenvolvido demonstra a aplicação prática de estruturas de dados e algoritmos eficientes para gerenciar e analisar informações de exames patológicos. Aplicamos com sucesso os conceitos aprendidos na disciplina, criando uma solução escalável e eficiente para o problema proposto.

As estruturas e algoritmos implementados permitem:
- Organização eficiente dos dados médicos
- Comparação entre valores examinados e de referência
- Priorização de casos por gravidade
- Busca otimizada de pacientes
- Extração e manipulação de dados específicos por paciente

Este sistema serve como base para futuros desenvolvimentos, incluindo a integração com visão computacional para automatizar a análise de imagens patológicas.

## Referências

1. Elder, D. E., Massi, D., Scolyer, R. A., & Willemze, R. (2018). *WHO Classification of Skin Tumours (4th ed.)*. Lyon: International Agency for Research on Cancer.

2. Swetter, S. M., Tsao, H., Bichakjian, C. K., et al. (2019). "Guidelines of care for the management of primary cutaneous melanoma." *Journal of the American Academy of Dermatology*, 80(1), 208-250. https://doi.org/10.1016/j.jaad.2018.08.055

3. Goodrich, M. T., Tamassia, R., & Goldwasser, M. H. (2021). *Data Structures and Algorithms in Python (2nd ed.)*. Wiley.

4. Van Rossum, G., Warsaw, B., & Coghlan, N. (2001). *PEP 8 – Style Guide for Python Code*. Python.org. https://peps.python.org/pep-0008/

5. VanderPlas, J. (2023). *Python Data Science Handbook (2nd ed.)*. O'Reilly Media.
