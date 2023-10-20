# Relatório de Projeto: Modificações no Projeto Azure Company

## Introdução

Neste relatório, são descritas as modificações feitas no projeto "Azure Company". O projeto envolve a criação de uma estrutura de banco de dados e inclui várias tabelas e transformações nos dados. Abaixo, detalhamos as modificações realizadas em cada tabela.

## Modificações em Todas as Tabelas

- **Remoção de Colunas com Metadados**: Foram removidas colunas que continham metadados ou informações não relevantes para a análise.

- **Checagem de Nulos e Valores Zerados**: Foi feita uma verificação completa de nulos e valores zerados para garantir a integridade dos dados.

- **Checagem de Cabeçalhos e Tipos de Dados**: Verificamos os cabeçalhos das colunas e os tipos de dados para garantir que estejam corretos e bem definidos.

- **Remoção de Colunas Desnecessárias**: Colunas desnecessárias foram eliminadas para simplificar a estrutura e reduzir a complexidade do banco de dados.

## Tabela "azure_company employee"

- **Divisão da Coluna 'Address'**: A coluna "Address" foi dividida em "Number", "Street", "City" e "State" para melhor organização e análise.

- **Mescla de Nomes**: As colunas "Fname" (Nome), "Minit" (Letra do Meio) e "Lname" (Sobrenome) foram mescladas usando uma função especial "= [Fname] & " " & [Minit] & ". " & [Lname]" para criar uma coluna "Full Name" (Nome Completo).

- **Alteração da Coluna 'Salary'**: A coluna "Salary" foi convertida para um tipo de dados decimal fixo para melhor representação de valores financeiros.

## Tabela "azure_company dept_locations"

- **Mescla de Cidade e Departamento**: As informações de cidade e departamento foram mescladas usando uma função especial "= [azure_company dept_locations.Dlocation] & " " & [Dname])" para criar uma coluna "Location" (Localização).

## Criação de Novas Tabelas

- Foram criadas duas novas tabelas, "azure_company manager_employee" e "azure_company employee_per_department," para atender a requisitos específicos do projeto.

## Resposta ao Ponto 14 das Instruções do Projeto:

A mesclagem dos nomes de departamentos e localizações cria uma coluna única que reflete combinações exclusivas, simplificando a criação de um modelo estrela. Isso é fundamental para estabelecer chaves de dimensão únicas e eficazes, permitindo a ligação precisa dos dados da tabela de fatos às informações dimensionais. Essa abordagem é direta e garante a unicidade das combinações, tornando-a a escolha apropriada para otimizar a modelagem estrela.

## Conclusão

As modificações realizadas no projeto "Azure Company" visaram melhorar a qualidade dos dados, otimizar a estrutura do banco de dados e atender aos requisitos específicos do projeto. Essas modificações contribuem para a criação de um modelo de dados mais eficiente e preparado para análises futuras.
