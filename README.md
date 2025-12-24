# 👥 People Analytics: Dashboard de Gestão de Capital Humano

Este projeto utiliza dados de RH para analisar o perfil dos colaboradores, níveis de satisfação e fatores que influenciam o desempenho e a retenção de talentos dentro da organização.

## 🎯 Objetivos da Análise
* **Perfil Demográfico**: Analisar a distribuição por idade, gênero e estado civil.
* **Remuneração e Carreira**: Avaliar a relação entre salário mensal, anos de experiência e promoções.
* **Qualidade de Vida e Engajamento**: Monitorar índices de satisfação no trabalho e envolvimento.
* **Educação e Treinamento**: Verificar o investimento em capacitação técnica e acadêmica.

## 🛠️ Tecnologias Utilizadas
* **Power BI**: Desenvolvimento das visualizações interativas.
* **Power Query**: Tratamento de dados (ex: categorização de faixas etárias).
* **DAX**: Criação de medidas para cálculo de médias salariais, taxa de satisfação e tempo médio de casa.

## 📊 Estrutura dos Dados (DatasetRH)
Os dados explorados neste projeto incluem:
* **Funcional**: Departamento (Data Science), Função (Cientista de Dados, Engenheiro, etc.) e Salário.
* **Comportamental**: Índice de Envolvimento, Satisfação no Trabalho e Disponibilidade para Hora Extra.
* **Histórico**: Anos na empresa, anos na função atual e tempo desde a última promoção.

## 💡 Sugestões de Métricas (DAX)
Para o seu portfólio, considere incluir estas fórmulas:
1. **Média Salarial** = `AVERAGE(DatasetRH[Salario_Mensal])`
2. **Índice Médio de Satisfação** = `AVERAGE(DatasetRH[Nivel_Satisfacao_Trabalho])`
3. **Total de Funcionários** = `COUNTROWS(DatasetRH)`
4. **Percentual de Hora Extra** = `DIVIDE(CALCULATE(COUNT(DatasetRH[Id_Funcionario]), DatasetRH[Disponivel_Hora_Extra] = "S"), [Total de Funcionários])`

## 🚀 Como Executar
1. Clone o repositório.
2. Abra o arquivo `.pbix` localizado na pasta `/pbix`.
3. Caso os dados não carreguem, aponte a fonte para o arquivo `DatasetRH.csv` na pasta `/data`.

---
*Este dashboard foi criado para auxiliar gestores de RH a tomar decisões baseadas em dados (Data-Driven).*
