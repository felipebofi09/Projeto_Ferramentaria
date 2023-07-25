<!DOCTYPE html>
<html>
<head>
  <title>Principais Scripts do Projeto da Ferramentaria</title>
</head>
<body>

<h2>1. Consultar todos os itens do Estoque:</h2>
<pre>
SELECT * FROM estoque_pecas;
</pre>

<h2>2. Atualizar a quantidade de itens no estoque:</h2>
<pre>
UPDATE estoque_pecas
SET quantidade = 100
WHERE id = 1;
</pre>

<h2>3. Atualizar o preço unitário de um item no estoque:</h2>
<pre>
UPDATE estoque_pecas
SET preco_unitario = 25.00
WHERE nome = 'Filtro de Ar';
</pre>

<h2>3.1. Aumentar 10% o Valor de todos os itens da categoria Freio:</h2>
<pre>
UPDATE Estoque_pecas
SET preco_unitario = preco_unitario * 1.10
WHERE categoria = 'Freio';
</pre>

<h2>4. Excluir um item específico do estoque:</h2>
<pre>
DELETE FROM estoque_pecas
WHERE id = 1;
</pre>

<h2>4.1. Excluir todos os produtos com quantidade menor ou igual a 30.</h2>
<pre>
DELETE FROM Estoque_pecas
WHERE quantidade <= 30;
</pre>

<h2>5. Consultar a quantidade total de itens da categoria "Filtro" e "Freio" por marca, de forma a mostrar primeiro os itens categorizados como "Freio":</h2>
<pre>
SELECT marca, categoria, SUM(quantidade) AS quantidade_total
FROM Estoque_pecas
WHERE categoria IN ('Freio', 'Filtro')
GROUP BY marca, categoria
ORDER BY CASE WHEN categoria = 'Freio' THEN 1 ELSE 2 END;
</pre>

<h2>6. Consultar itens no estoque com quantidade menor que 50:</h2>
<pre>
SELECT * FROM estoque_pecas 
WHERE quantidade < 50;
</pre>

<h2>6.1. Consultar itens no estoque com quantidade menor que 50, na categoria Freio:</h2>
<pre>
SELECT *
FROM estoque_pecas
WHERE quantidade < 50 AND categoria = 'Freio';
</pre>

<h2>6.2. Consultar itens no estoque com quantidade menor que 50, na categoria Freio, mostrando apenas o nome, preço unitário e filial de origem do item:</h2>
<pre>
SELECT id, nome, preco_unitario, filial_origem
FROM estoque_pecas
WHERE quantidade < 50 AND categoria = 'Filtro';
</pre>

<h2>7. Consultar itens em estoque de uma filial específica:</h2>
<pre>
SELECT * FROM estoque_pecas
WHERE filial_origem = 'Filial A';
</pre>

<h2>8. Consultar itens em estoque de uma determinada categoria:</h2>
<pre>
SELECT * FROM estoque_pecas 
WHERE categoria = 'Freio';
</pre>

<h2>9. Consultar o valor total em estoque de um item específico:</h2>
<pre>
SELECT categoria, SUM(quantidade * preco_unitario) AS valor_total 
FROM estoque_pecas 
GROUP BY categoria;
</pre>

<h2>10. Consultar o valor total em estoque por categoria:</h2>
<pre>
SELECT categoria, SUM(quantidade * preco_unitario) AS valor_total 
FROM estoque_pecas 
GROUP BY categoria;
</pre>

</body>
</html>
