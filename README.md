**English version**

<div align="center">

# Hello there! 👋

## I'm here to share another project!! 🥳🥳
</div>

Some information about the project:

+ Where did I get the original dataset?
    - I got it from [GitHub](https://github.com/julianazanelatto/power_bi_analyst/tree/main) by Juliana Mascarenhas, an instructor at DIO.

+ Which programming language and visualization software were used?
    - I used:<div align="center">![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white) ![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black).</div>

+ What can you find in this repository?
    - You will find an SQL file and Power BI used in this project.

___ 


<div align="center">

### **Project Objective!**

The goal of this project was to enhance my knowledge of using the Azure cloud computing platform, in conjunction with Power BI and MySQL. During the process, I learned how to create and manage a cloud database and connect this database to different software, such as the ones mentioned. Below, I outline the key steps I followed during the project development, with a particular focus on data cleaning and preparation.


</div>

___ 


1. Database creation:
+ I created a MySQL database on Azure and then created a schema named azure_company, where I built the tables and added the data.


2. Integration with Power BI:
+ I connected the MySQL database on Azure to Power BI for visualization.


3. Data cleaning:
+ I renamed and changed the types of several columns to improve understanding.
a.	Dname -> Nome_Departamento
b.	Dnumber, Dno, Dnum -> Numero_departamento (Mudei o tipo para Texto)
c.	Mgr_ssn, Super_ssn -> Numero_da_carteira_Gerente
d.	Essn, Ssn -> Numero_da_carteira
e.	Mgr_start_date - > Data_Inicio_Gerente
f.	Dept_create_date -> Data_Criacao_Departamento
g.	Sex -> Genero
h.	Dependent_name - > Nome_do_dependente
i.	Bdate -> Data_de_aniversario
j.	Relationship -> Relacao
k.	Dlocation -> Localizacao_Departamento
l.	Fname -> Nome
m.	Minit -> Inicial_nome_meio
n.	Lname -> Sobrenome
o.	Address - > Endereco 
p.	Salary -> Salario (Mudei o tipo para Decimal Fixo)
q.	Pname -> Nome_Projetos 
r.	Pnumber, Pno -> Numero_Projetos (Mudei o tipo para Texto)
s.	Plocation -> Local_Projetos
t.	Hours -> Horas

4. Standardization of table names:
+ I renamed the tables to make them easier to read.
a.	azure_company department -> Departamentos
b.	azure_company dependente -> Dependentes 
c.	azure_company dept_locations -> Localizacao_Departamentos
d.	azure_company employee -> Funcionarios 
e.	azure_company Project -> Projetos
f.	azure_company works_on -> Horas_Trabalhadas

5. Handling null values:
+ After analyzing the data, I identified that the null value in the 'Superior_SSN' column of the 'Funcionarios' table occurs because the employee in question is the department manager. As a result, there is no one hierarchically superior to them within the department. To resolve this, I chose to assign the employee's own SSN to the field.


6. Splitting complex columns:
+ The Address column was split into three: Numero_Endereco, Cidades e Estado.


7. Data merging:
+ I combined the Funcionarios and Departmentos tables, deleted redundant columns, and merged first and last names into a single column.


8. Geographic adjustments:
+ I merged the Departmentos table with the Localizacao_Departamentos table and combined the Nome_Departamento with its location to create unique combinations. I also added "Texas" to avoid geographic conflicts in Power BI.

9. Explanation of the use of the merge function:
+ I used the “merge” function in Power BI instead of “append” because when we merge, we create a single table where information from different tables is connected by a key column. On the other hand, the “append” function just adds the rows of one table to another, which can generate null values if a column is missing in either base table. Therefore, to create more consistent and error-free reports and dashboards, the merge function is the best choice.

10. Counting employees per manager:
+ I duplicated the Employees table and grouped the data to calculate how many employees each manager supervises.

11. I merged the Projetos table with Horas_Trabalhadas to create a table where we have the hours worked per project.

12. I renamed the new tables to Funcionario_Departamento, Departamento_Local, Agrupamento_Colaboradores_Gerentes e Projetos_Horas.

13. Final report:
+ I created a report to test and ensure that the database was working as expected.




**Versão PT-BR**

<div align="center">

# Olá! 👋

## Estou aqui para compartilhar mais um projeto !!🥳🥳

</div>

Algumas informações sobre o projeto: 

+ De onde obtive o conjunto de dados original?
    - Eu peguei no [GitHub](https://github.com/julianazanelatto/power_bi_analyst/tree/main) da Juliana Mascarenhas uma instrutora do DIO.
+ Qual linguagem de programação e software de visualização foram utilizados?
    - Eu usei:  <div align="center">![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white) ![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black).</div>

+ O que posso encontrar nesse repositório?
    - Voce encontrara um arquivo sql e Power BI que foram usados nesse projeto. 

___ 


<div align="center">

### **Objetivo do projeto!**

O objetivo deste projeto foi aprimorar meu conhecimento no uso da plataforma de computação em nuvem Azure, em conjunto com o Power BI e o MySQL. Durante o processo, aprendi a criar e gerenciar um banco de dados na nuvem, além de conectar esse banco a diferentes softwares, como os mencionados. A seguir, apresento os principais passos que segui ao longo do desenvolvimento do projeto, com foco especial no tratamento e limpeza de dados.

</div>

___


1. Criação do banco de dados:
+ Criei um banco de dados MySQL na Azure e depois criei a schema com nome azure_company. Onde construí as tabelas e coloquei as informações.


2.	Integração com Power BI:
+ Conectei o banco de dados MySQL do Azure ao Power BI para visualização.


3.	Limpeza de dados:
+ Renomeei e alterei os tipos de várias colunas para melhorar a compreensão.
a.	Dname -> Nome_Departamento
b.	Dnumber, Dno, Dnum -> Numero_departamento (Mudei o tipo para Texto)
c.	Mgr_ssn, Super_ssn -> Numero_da_carteira_Gerente
d.	Essn, Ssn -> Numero_da_carteira
e.	Mgr_start_date - > Data_Inicio_Gerente
f.	Dept_create_date -> Data_Criacao_Departamento
g.	Sex -> Genero
h.	Dependent_name - > Nome_do_dependente
i.	Bdate -> Data_de_aniversario
j.	Relationship -> Relacao
k.	Dlocation -> Localizacao_Departamento
l.	Fname -> Nome
m.	Minit -> Inicial_nome_meio
n.	Lname -> Sobrenome
o.	Address - > Endereco 
p.	Salary -> Salario (Mudei o tipo para Decimal Fixo)
q.	Pname -> Nome_Projetos 
r.	Pnumber, Pno -> Numero_Projetos (Mudei o tipo para Texto)
s.	Plocation -> Local_Projetos
t.	Hours -> Horas


4.	Padronização de nomes de tabelas:
+ Renomeei as tabelas para facilitar a leitura.
a.	azure_company department -> Departamentos
b.	azure_company dependente -> Dependentes 
c.	azure_company dept_locations -> Localizacao_Departamentos
d.	azure_company employee -> Funcionarios 
e.	azure_company Project -> Projetos
f.	azure_company works_on -> Horas_Trabalhadas


5.	Tratamento de valores nulos:
+ Após a análise dos dados, identifiquei que o valor nulo na coluna 'Carteira_do_Superior', da tabela 'Employee', ocorre porque o funcionário em questão é o gerente do departamento. Dessa forma, não há uma pessoa hierarquicamente superior a ele dentro do departamento. Para resolver essa questão, optei por atribuir o número da carteira do próprio funcionário. 


6.	Divisão de colunas complexas: 
+ A coluna Endereco foi dividida em três: Numero_Endereco, Cidades e Estado.


7.	Mesclagem de dados:
+ Combinei as tabelas de funcionários e departamentos, eliminei colunas redundantes, e juntei os nomes e sobrenomes em uma única coluna.


8.	Ajustes geográficos:
+ Mesclei a tabela Departamentos com a tabela Localizacao_Departamentos e juntei as colunas com o nome do departamento e a sua localização para criar combinações únicas. Também adicionei "Texas" para evitar conflitos geográficos no Power BI.


9. Explicação do uso da função mesclar:	
+ Utilizei a função de "mesclar" no Power BI em vez de "acrescentar" porque, ao mesclar, criamos uma tabela única em que as informações de diferentes tabelas são conectadas por uma chave de coluna. Em contrapartida, a função "acrescentar" apenas adiciona as linhas de uma tabela a outra, o que pode gerar valores nulos caso alguma coluna não esteja presente nas duas tabelas bases. Dessa forma, para a criação de relatórios e dashboards mais consistentes e sem falhas, a função "mesclar" é a mais indicada.


10.	Contagem de colaboradores por gerente:
+ Dupliquei a tabela de funcionários e agrupei os dados para calcular quantos colaboradores cada gerente supervisiona.


11.	Mesclei a tabela Projetos com Horas_Trabalhadas para criar uma tabela onde temos as horas trabalhadas por projeto.


12.	Alterei os nomes das novas tabelas para Funcionario_Departamento, Departamento_Local, Agrupamento_Colaboradores_Gerentes e Projetos_Horas.


13.	Relatório final:
+ Criei um relatório para testar e garantir que o banco de dados estivesse funcionando conforme esperado.
