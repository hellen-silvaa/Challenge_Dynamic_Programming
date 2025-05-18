# Sistema de Análise Patológica com Visão Computacional

## Descrição do Projeto

Este projeto foi desenvolvido como parte da Sprint 1 da disciplina de Dynamic Programming da FIAP orientada pelo professor Francisco Elanio Bezerra. Nossa equipe optou pelo desafio 2 proposto pela DASA, que consiste em desenvolver um sistema de análise patológica.

Desenvolvemos uma solução completa para análise de exames patológicos, permitindo o armazenamento e processamento de dados de amostras patológicas, sinais e cistos, com foco particular nas dimensões (altura, largura e comprimento) e características patológicas. Para isso, construímos:

1. Uma estrutura de dados utilizando dicionários e listas aninhados para representar as informações relevantes dos pacientes e seus exames
2. Funções específicas em Python para processar esses dados de maneira eficiente
3. Um sistema de dicionários representando exames de pacientes, com valores examinados e de referência
4. Funcionalidades para extrair todos os exames de um mesmo paciente e montar um segundo dicionário específico para cada paciente

A solução implementa técnicas avançadas de estrutura de dados e algoritmos para fornecer análises precisas e eficientes. É importante ressaltar que os dados utilizados nesta etapa são fictícios, pois estamos paralelamente desenvolvendo o módulo de visão computacional com OpenCV, que futuramente será responsável pela leitura e análise automática das amostras patológicas.

## Explicação das Hipóteses e Dados Considerados

### Base de Dados
Desenvolvemos uma estrutura de dados para representar análises patológicas de cinco pacientes: Hellen, Alexia, Wendell, Lorenzo e Beatriz. Cada exame inclui informações sobre lesões com suas respectivas características e dimensões (altura, largura e comprimento). Os dados usados foram fictícios pois ainda estamos desenvolvendo a parte de visão computacional que será capaz de realizar as medições com precisão.

### Hipóteses Assumidas
1. **Estrutura de Dados**: Utilizamos dicionários e listas aninhados para representar a hierarquia paciente → exames → características.

2. **Métricas de Análise**: Incluímos valores numéricos (0-1) para representar características como assimetria, irregularidade de bordas e heterogeneidade de cores, seguindo critérios médicos.

3. **Tipos de Exames**: Selecionamos diferentes tipos de lesões para cada paciente:
   - Pinta/Nevo (Hellen e Beatriz)
   - Cisto (Alexia)
   - Sinal potencialmente maligno (Wendell)
   - Mancha na pele (Lorenzo)

4. **Status de Alteração**: Indicamos explicitamente para cada exame se houve alteração patológica, complementando a análise das características individuais.

## Técnicas de Programação Utilizadas

1. **Programação Dinâmica/Memorização**: Implementada nas funções `extrair_exames_paciente` e `calcular_volume_dinamico` para evitar processamento repetido e aumentar a eficiência.

2. **Estruturas de Dados Aninhadas**: Utilizamos dicionários e listas aninhados para representar a complexidade dos dados patológicos.

3. **Algoritmos de Busca Binária**: Implementado na função `busca_pacientes_por_faixa_etaria` para busca eficiente.

4. **Análise Estatística**: Incorporamos cálculos estatísticos para comparação entre pacientes e identificação de padrões.

5. **Visualização de Dados**: Utilizamos bibliotecas como Matplotlib para representar visualmente os dados.

## Funcionalidades Implementadas

1. **Extração de Dados de Pacientes**: Obtém informações específicas de um paciente e cria um segundo dicionário apenas com seus dados, utilizando memorização para otimização.

2. **Verificação de Alterações**: Identifica características que superam os limiares de alerta estabelecidos.

3. **Análise de Dimensões**: Calcula volume (altura × largura × comprimento) e estatísticas sobre as dimensões das lesões.

4. **Busca por Faixa Etária**: Implementa busca binária para encontrar pacientes dentro de uma faixa de idade específica.

5. **Análise de Volume com Programação Dinâmica**: Calcula volumes otimizando o processamento através de memorização.

6. **Geração de Relatórios**: Produz relatórios completos para cada paciente, combinando todas as análises.

7. **Comparação entre Pacientes**: Permite comparar métricas e identificar padrões entre diferentes pacientes.

8. **Visualização Gráfica**: Cria gráficos para análise visual das dimensões, alterações e diagnósticos.

## Requisitos Técnicos

- Python 3.6+
- pandas
- matplotlib

## Como Executar

1. Abra o código no Google Colab ou jupter (recomendado) ou em um ambiente Python
2. Execute as células em ordem
3. A função `main()` demonstra todas as funcionalidades implementadas

## Grupo CodeBreakers - 2ESR
- **Integrantes:**
  - 558385 - Alexia Ramalho Izidio Dos Santos
  - 554746 - Beatriz Vieira de Novais
  - 559008 - Hellen Aparecida Moura Silva
  - 557397 - Lorenzo Adinolfi Acquesta
  - 558859 - Wendell Dos Santos Silva
## Conclusão

O sistema desenvolvido demonstra a aplicação de estruturas de dados aninhadas e algoritmos eficientes para gerenciar e analisar informações de exames patológicos. As técnicas de programação dinâmica, busca binária e outros conceitos vistos em aula foram aplicados com sucesso.

A estrutura de dados permite fácil expansão e adaptação para incluir novos tipos de análises ou pacientes, sendo uma solução escalável para o problema proposto. No futuro, a integração com técnicas reais de visão computacional permitirá a automação completa das análises patológicas.

## Referências

1. Elder, D. E., Massi, D., Scolyer, R. A., & Willemze, R. (2018). *WHO Classification of Skin Tumours (4th ed.)*. Lyon: International Agency for Research on Cancer.

2. Swetter, S. M., Tsao, H., Bichakjian, C. K., et al. (2019). "Guidelines of care for the management of primary cutaneous melanoma." *Journal of the American Academy of Dermatology*, 80(1), 208-250. https://doi.org/10.1016/j.jaad.2018.08.055

3. National Comprehensive Cancer Network (NCCN). (2023). *NCCN Clinical Practice Guidelines in Oncology: Melanoma*. Retrieved from https://www.nccn.org/professionals/physician_gls/pdf/cutaneous_melanoma.pdf

4. Esteva, A., Kuprel, B., Novoa, R. A., et al. (2017). "Dermatologist-level classification of skin cancer with deep neural networks." *Nature*, 542(7639), 115-118. https://doi.org/10.1038/nature21056

5. Navarrete-Dechent, C., Liopyris, K., & Marghoob, A. A. (2022). "Artificial Intelligence and Dermoscopy of Melanocytic Lesions." *Dermatologic Clinics*, 40(3), 361-371. https://doi.org/10.1016/j.det.2022.03.006

6. Goodrich, M. T., Tamassia, R., & Goldwasser, M. H. (2021). *Data Structures and Algorithms in Python (2nd ed.)*. Wiley.

7. VanderPlas, J. (2023). *Python Data Science Handbook (2nd ed.)*. O'Reilly Media.
