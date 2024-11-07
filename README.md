# Momento-Database
Você está prestes a explorar o banco de dados da empresa "Momento"! Com essa base de dados, vamos treinar consultas SQL e responder algumas perguntas intrigantes que vão revelar como a empresa está organizada. Vamos lá?<br>

## Departamento de Tecnologia<br>
Inclua suas próprias informações no departamento de Tecnologia da empresa.<br>

Agora diga, quantos funcionários temos ao total na empresa?<br>
R: 42 <br>
select count(*) from funcionarios;<br>

E quanto ao Departamento de Tecnologia?<br>
R: 6<br>
select * from funcionarios where departamento_id = 6;<br>

## Departamento de Vendas<br>
Quantos funcionários trabalham no Departamento de Vendas? Use uma consulta para descobrir o número total de funcionários alocados nesse departamento.<br>
R: 5<br>
 select * from funcionarios where departamento_id = 8;<br>

Salários no Departamento de Vendas<br>
R: 10000.00, 20000.00, 6000.00, 12000.00<br>
select * from cargos;<br>

Qual é o custo total dos salários do pessoal de Vendas? Isso nos ajuda a entender o orçamento do departamento!<br>
R: 51500.00<br>
select sum(salario) from funcionarios where departamento_id = 8;<br>

Quanto o departamento de Vendas gasta em salários?<br>
R: 51500.00<br>
select sum(salario) from funcionarios where departamento_id = 8;<br>

Quais são os produtos mais vendidos e quais têm pouca ou nenhuma saída?<br>
R: 1	Uniforme do Superman	300.13<br>
select * from vendas order by quantidade_vendida desc;<br>
select * from produtos;<br>

Qual é o produto mais caro no inventário da empresa?<br>
R: 8	Sabre de Luz (Mace Windu)	990.29<br>
select * from produtos;<br>

## Departamento de Inovações<br>
Um novo departamento foi criado. O departamento de Inovações. Ele será locado no Brasil. Por favor, adicione-o no banco de dados da empresa colocando quaisquer informações que você achar relevantes.<br>
INSERT INTO momento.escritorios(escritorio_nome, endereco, cep, cidade, estado_provincia, pais_id) VALUES ('Omar silvestre', 'Rua Casa do caixa prego', '08537150', 'São Paulo', 'São Paulo', 'BR');<br>
INSERT INTO momento.departamentos(departamento_nome, escritorio_id) VALUES('Inovação', 3901);<br>

O departamento de Inovações está sem funcionários. Inclua alguns colegas de turma nesse departamento.<br>
INSERT INTO funcionarios(funcionario_id,primeiro_nome,sobrenome,email,senha,telefone,data_contratacao,cargo_id,salario,gerente_id,departamento_id) VALUES (100,'Victoria','Toledo','victoria.toledo@momento.org','@4@8@15@16','515.123.5828','1997-09-17',4,58000.00,NULL,6);<br>
INSERT INTO funcionarios(funcionario_id,primeiro_nome,sobrenome,email,senha,telefone,data_contratacao,cargo_id,salario,gerente_id,departamento_id) VALUES (101,'Kochywon','Kochhar','kochywon.kochhar@momento.org','@48@15@16','515.123.1918','1982-05-15',5,5800.00,NULL,6);<br>
INSERT INTO funcionarios(funcionario_id,primeiro_nome,sobrenome,email,senha,telefone,data_contratacao,cargo_id,salario,gerente_id,departamento_id) VALUES (102,'Dennis',"França",'dennis.franca@momento.org','@4@8@5@16','515.123.1948','1985-02-16',5,5800.00,NULL,6);<br>

## Funcionários<br>
Quantos funcionários da empresa Momento possuem conjuges?<br>


Qual o funcionário contratado há mais tempo na empresa?<br>

Qual o funcionário contratado há menos tempo na empresa?<br>

Quem são os funcionários com mais tempo na empresa, considerando a data_contratacao?<br>

Como a média salarial dos funcionários da "Momento" evoluiu nos últimos anos? Dica: utilize a função AVG() para calcular a média salarial dos funcionários. e GROUP BY para agrupar os resultados por ano.<br>

## Médias salariais<br>
Qual a média salarial dos funcionários da empresa Momento, excluindo-se o CEO, CMO e CFO?<br>

Qual a média salarial do departamento de tecnologia?<br>

Qual o departamento com a maior média salarial?<br>

Qual o departamento com o menor número de funcionários?<br>

## Produtos<br>
Pensando na relação quantidade e valor unitario, qual o produto mais valioso da empresa?<br>

Qual o produto mais vendido da empresa?<br>

Qual o produto menos vendido da empresa?<br>

## Escritórios<br>
Quantos escritórios a "Momento" possui em cada região? (Dica: relacione as tabelas regioes e escritorios).<br>

Qual é o custo total de suprimentos em cada escritório? Que tal ordenar os resultados para ver qual escritório possui os suprimentos mais caros?<br>
