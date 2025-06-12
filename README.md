# Sistema de Análise Patológica 

### Identificação do Grupo - 2ESR (CodeBreakers)
- **558385** - Alexia Ramalho Izidio Dos Santos
- **554746** - Beatriz Vieira de Novais
- **559008** - Hellen Aparecida Moura Silva
- **557397** - Lorenzo Adinolfi Acquesta
- **558859** - Wendell Dos Santos Silva

## Descrição do Projeto

Este projeto foi desenvolvido como parte da Sprint 1 e 2 da disciplina de Dynamic Programming da FIAP orientada pelo professor Francisco Elanio Bezerra. Nossa equipe optou pelo desafio 2 proposto pela DASA, que consiste em desenvolver um sistema de análise patológica.
Desenvolvemos uma solução para análise de exames patológicos, permitindo o armazenamento e processamento de dados de amostras patológicas, sinais e cistos, com foco particular nas dimensões (altura, largura e comprimento) e características patológicas.

## Explicação das Hipóteses e Dados Considerados

### Base de Dados
Desenvolvemos uma estrutura de dados para representar análises patológicas de cinco pacientes hipotéticos sendo os membros da equipe: Hellen, Alexia, Wendell, Lorenzo e Beatriz. Cada exame inclui informações sobre lesões com suas respectivas características e dimensões. Os dados usados são fictícios, simulando o que seria obtido por visão computacional, como ainda estamos construindo o nosso sistema ainda não foi possível capturar esses dados para essa primeira entrega por isso optamos por usar dados fictícios para simular.


### Hipóteses Assumidas
1. **Parâmetros Relevantes**:
   - **Assimetria**: Fator crítico para detecção de malignidade (escala 0-1)
   - **Diâmetro**: Tamanho da lesão como indicador de crescimento
   - **Volume**: Cálculo tridimensional para análise de progressão  
   - **Localização**: Área anatômica para análise de risco específico

3. **Valores de Referência**: Estabelecemos limiares para identificar lesões potencialmente problemáticas:
   - Diâmetro > 0.6cm como indicador de atenção
   - Assimetria > 0.5 (escala 0-1) como indicador de atenção
   - Volume > 0.5cm³ como indicador de atenção

4. **Categorização de Lesões**: Dividimos as análises em diferentes tipos (pinta, cisto, sinal) com características distintas para permitir análise comparativa entre casos e também foi o recomendado no Kickoff da DASA usar estas que são as mais comuns.

5. **Priorização Clínica usando fila**: Implementamos uma função de prioridade para organizar a análise dos casos por urgência, assumindo que características específicas exigem avaliação mais rápida.

## Técnicas de Utilizadas

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
- Padrões PEP 8: Seguimos as diretrizes de estilo do Python
- Nomenclatura: snake_case para variáveis, CamelCase para classes
- Comentários: Trechos explicados

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

1. Abra o código no Google Colab | Jupyter Notebook (recomendado) ou em um ambiente python
2. Execute as células em ordem
3. As funções de demonstração mostram o funcionamento de cada componente


Este sistema serve como base para futuros desenvolvimentos, incluindo a integração com visão computacional para automatizar a análise de imagens patológicas.

## Referências
1.  SALVETTI, Dirceu Douglas; BARBOSA, Lisbete Madson. Algoritmos. Pearson, 2004.
2.  MENEZES, Nilo. Introdução à Programação em Python. São Paulo: Novatec, 2019.
3.  CORMEN, Thomas H. et al. Algoritmos: Teoria e Prática. 3ª ed. Elsevier, 2012.
4.  DASA. Diretrizes para Análise Patológica Digital. 2023.

