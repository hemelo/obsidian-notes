
## Documentação de Casos de Uso

Cenário Fictício: Ecommerce de Cervejas


<table class="on-table on-table-primary">
  <thead>
	<tr>
	  <th colspan="3">Caso de Uso 01</th>
	</tr>
  </thead>
  <tbody>
	<tr>
	  <td>
		<b>Título do caso de uso</b>
	  </td>
	  <td colspan="2"><b>Pesquisar tipo de cerveja</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Código identificador</b>
	  </td>
	  <td colspan="2">DCUS01
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Sumário</b>
	  </td>
	  <td colspan="2">Este requisito permite que o usuário consulte a cerveja desejada, obtendo informações sobre o nome, o fabricante e o preço da cerveja.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator primário</b>
	  </td>
	  <td colspan="2">Cliente
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator secundário</b>
	  </td>
	  <td colspan="2">Sistema
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pré-condição</b>
	  </td>
	  <td colspan="2">Cervejas cadastradas no sistema.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Principal</b>
	  </td>
	  <td>
		<b>Ator</b>
	  </td>
	  <td>
		<b>Sistema</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP01 - O cliente seleciona Consultar cerveja.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP02 - Exibir a página de consulta de cerveja.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP01 - Seleciona o fabricante ou o nome ou a faixa de preço da cerveja <b>- FA01.</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP02 - Receber o fabricante, nome ou a faixa de preço - <b>FE01.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP03 - Exibir dados: nome, fabricante e preço da cerveja - <b>FE02.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Alternativo</b>
	  </td>
	  <td colspan="2"><b>FA01 </b>- Cancela a consulta.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">a) O cliente seleciona a opção "Limpar dados".
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">b) O caso de uso retorna à tela inicial.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">c) O caso de uso termina.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo de Exceção</b>
	  </td>
	  <td colspan="2"><b>FE01 </b>- Receber o fabricante, nome ou a faixa de preço da cerveja. - <b>RN01.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">Se o fabricante, nome ou faixa de preço da cerveja não for selecionado, o sistema exibe a mensagem: "Selecione uma opção: fabricante, nome ou faixa de preço".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		Retorna ao FP01.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2"><b>FE02 - </b>Nenhuma cerveja encontrada.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se não houver nenhuma cerveja cadastrada com o nome, fabricante ou faixa de preço será apresentada a mensagem “Nenhuma cerveja cadastrada".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">b) Encerra o caso de uso.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pós-condição</b>
	  </td>
	  <td colspan="2">Não há.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Regras de Negócio</b>
	  </td>
	  <td colspan="2">RN01 - A consulta da cerveja pode ser pelo fabricante, nome ou faixa de preço.
	  </td>
	</tr>
  </tbody>
</table>


<table>
  <thead>
	<tr>
	  <th colspan="3">Caso de Uso 02</th>
	</tr>
  </thead>
  <tbody>
	<tr>
	  <td>
		<b>Título do caso de uso</b>
	  </td>
	  <td colspan="2"><b>Registrar a compra</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Código identificador</b>
	  </td>
	  <td>
		<b>DCUS02</b>
	  </td>
	  <td>
		<b>&nbsp;</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Sumário</b>
	  </td>
	  <td colspan="2">Este requisito permite que o usuário registre a compra da cerveja.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator primário</b>
	  </td>
	  <td colspan="2">Cliente
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator secundário</b>
	  </td>
	  <td colspan="2">Sistema
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pré-condição</b>
	  </td>
	  <td colspan="2">Cervejas cadastradas no sistema.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Principal</b>
	  </td>
	  <td>
		<b>Ator</b>
	  </td>
	  <td>
		<b>Sistema</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP01 - O cliente seleciona "Comprar".
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP02 - Exibir a página de compra de cerveja.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP03 - O cliente seleciona a cerveja.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP04 - Receber a cerveja - <b>FE01.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP5 - O cliente informa a quantidade desejada.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP06 - Receber a quantidade - <b>FE02.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP07 - Validar a quantidade disponível em estoque - <b>FE03</b> - <b>FA01.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP08 - Executar o caso de uso Calcular valor da compra.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP09 - Informa dados do cliente.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP10 - Receber o cliente.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP11 - Cadastrar o cliente -<b> FA02</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Alternativo</b>
	  </td>
	  <td colspan="2"><b>FA01 </b>- Cancela o registro da compra.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">a) O cliente seleciona a opção "Limpar dados".
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">b) O caso de uso retorna à tela inicial.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">c) O caso de uso termina.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2"><b>FA02 </b>- Cadastrar o cliente.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">a) O sistema executa o caso de uso "Cadastrar cliente".
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">b) Retorna ao FP09.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo de Exceção</b>
	  </td>
	  <td colspan="2"><b>FE01 </b>- Receber a cerveja.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se a cerveja não for selecionada, o sistema exibe a mensagem: "selecione a cerveja desejada".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		b) Retorna ao FP03.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2"><b>FE02 - </b>Receber a quantidade.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">Se a quantidade não for informada, o sistema exibe a mensagem: "Informe a quantidade desejada".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">b) Retorna ao FP05.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2"><b>FE03 </b>- Quantidade do produto registrada na compra
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se a quantidade do produto informada para a compra for maior que a quantidade em estoque, o sistema exibe a mensagem: "Quantidade indisponível".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">b) Retorna ao FP05.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">c) Se o cliente não aceitar a quantidade disponível, encerra o caso de uso.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pós-condição</b>
	  </td>
	  <td colspan="2">Produtos baixados no estoque.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Regras de Negócio</b>
	  </td>
	  <td colspan="2">RN03 - A compra poderá ser feita somente por clientes maiores de 18 anos. RN08 - O pedido de compra está relacionado a um cliente.
	  </td>
	</tr>
  </tbody>
</table>


<table>
  <thead>
	<tr>
	  <th colspan="3">Caso de Uso 03</th>
	</tr>
  </thead>
  <tbody>
	<tr>
	  <td>
		<b>Título do caso de uso</b>
	  </td>
	  <td colspan="2"><b>Calcular valor da compra</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Código identificador</b>
	  </td>
	  <td>
		<b>DCUS03</b>
	  </td>
	  <td>
		<b>&nbsp;</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Sumário</b>
	  </td>
	  <td colspan="2">Este requisito calcula o valor total da compra.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator primário</b>
	  </td>
	  <td colspan="2">Cliente
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator secundário</b>
	  </td>
	  <td colspan="2">Sistema
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pré-condição</b>
	  </td>
	  <td colspan="2">Registrar a compra e cervejas cadastradas.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Principal</b>
	  </td>
	  <td>
		<b>Ator</b>
	  </td>
	  <td>
		<b>Sistema</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP01 - Calcular valor da compra - <b>FE01.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP02 - Exibir valor da compra.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Alternativo</b>
	  </td>
	  <td colspan="2">Não há.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo de Exceção</b>
	  </td>
	  <td colspan="2"><b>FE01 </b>- O valor da cerveja não está cadastrado.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se o valor da cerveja não estiver cadastrado, o sistema exibe a mensagem: "Atualize o cadastro do produto".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		b) Retorna ao FP01.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pós-condição</b>
	  </td>
	  <td colspan="2">Não há.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Regras de Negócio</b>
	  </td>
	  <td colspan="2">RN11 – O valor da compra deve ser calculado: (quantidade * preço unitário).
	  </td>
	</tr>
  </tbody>
  <tfoot>
	<tr>
	  <td colspan="2">
		Documentação de caso de uso – Calcular valor da compra
	  </td>
	</tr>
  </tfoot>
</table>

<table>
  <thead>
	<tr>
	  <th colspan="3">Caso de Uso 03</th>
	</tr>
  </thead>
  <tbody>
	<tr>
	  <td>
		<b>Título do caso de uso</b>
	  </td>
	  <td colspan="2"><b>Calcular valor da compra</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Código identificador</b>
	  </td>
	  <td>
		<b>DCUS03</b>
	  </td>
	  <td>
		<b>&nbsp;</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Sumário</b>
	  </td>
	  <td colspan="2">Este requisito calcula o valor total da compra.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator primário</b>
	  </td>
	  <td colspan="2">Cliente
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator secundário</b>
	  </td>
	  <td colspan="2">Sistema
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pré-condição</b>
	  </td>
	  <td colspan="2">Registrar a compra e cervejas cadastradas.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Principal</b>
	  </td>
	  <td>
		<b>Ator</b>
	  </td>
	  <td>
		<b>Sistema</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP01 - Calcular valor da compra - <b>FE01.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP02 - Exibir valor da compra.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Alternativo</b>
	  </td>
	  <td colspan="2">Não há.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo de Exceção</b>
	  </td>
	  <td colspan="2"><b>FE01 </b>- O valor da cerveja não está cadastrado.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se o valor da cerveja não estiver cadastrado, o sistema exibe a mensagem: "Atualize o cadastro do produto".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		b) Retorna ao FP01.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pós-condição</b>
	  </td>
	  <td colspan="2">Não há.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Regras de Negócio</b>
	  </td>
	  <td colspan="2">RN11 – O valor da compra deve ser calculado: (quantidade * preço unitário).
	  </td>
	</tr>
  </tbody>
</table>
      


<table>
  <thead>
	<tr>
	  <th colspan="3">Caso de Uso 4</th>
	</tr>
  </thead>
  <tbody>
	<tr>
	  <td>
		<b>Título do caso de uso</b>
	  </td>
	  <td colspan="2"><b>Cadastrar cliente</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Código identificador</b>
	  </td>
	  <td>
		<b>DCUS04</b>
	  </td>
	  <td>
		<b>&nbsp;</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Sumário</b>
	  </td>
	  <td colspan="2">Este requisito permite que o usuário cadastre o cliente.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator primário</b>
	  </td>
	  <td colspan="2">Cliente
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Ator secundário</b>
	  </td>
	  <td colspan="2">Sistema
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pré-condição</b>
	  </td>
	  <td colspan="2">Registrar a compra.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Principal</b>
	  </td>
	  <td>
		<b>Ator</b>
	  </td>
	  <td>
		<b>Sistema</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP01 - O cliente seleciona "Cadastrar cliente".
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP02 - Exibir a página "Dados do cliente".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP03 - O cliente informa o nome.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP04 - Receber o nome - <b>FE01.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP05 - O cliente informa o endereço de entrega.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP06 - Receber o endereço de entrega - <b>FE02.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP07 - O cliente informa o telefone.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP08 - Receber o telefone - <b>FE03.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		FP9 - O cliente informa o CPF.
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		FP10 - Receber o CPF - <b>FE04.</b>
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td>
		&nbsp;
	  </td>
	  <td>
		&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo Alternativo</b>
	  </td>
	  <td colspan="2"><b>FA01 </b>- Cancela o cadastro do cliente.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">a) O cliente seleciona a opção "Limpar dados".
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">b) O caso de uso retorna à tela inicial.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">c) O caso de uso termina.
	  </td>
	</tr>
	<tr>
	  <td>
		&nbsp;
	  </td>
	  <td colspan="2">&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Fluxo de Exceção</b>
	  </td>
	  <td colspan="2"><b>FE01 </b>- Receber o nome.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se o nome não for informado, o sistema exibe a mensagem: "Informe o nome".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">b) Retorna ao FP03.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2"><b>FE02 - </b>Receber o endereço de entrega.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se o endereço de entrega não for informado, o sistema exibe a mensagem: "Informe o endereço de entrega".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">b) Retorna ao FP05.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2"><b>FE03 </b>- Receber o telefone.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se o telefone não for informado, o sistema exibe a mensagem: "Informe o telefone".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">b) Retorna ao FP07.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2"><b>FE04 </b>- Receber o CPF.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">a) Se o CPF não for informado, o sistema exibe a mensagem: "Informe o CPF ".
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">b) Retorna ao FP09.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>&nbsp;</b>
	  </td>
	  <td colspan="2">&nbsp;
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Pós-condição</b>
	  </td>
	  <td colspan="2">Não há.
	  </td>
	</tr>
	<tr>
	  <td>
		<b>Regras de Negócio</b>
	  </td>
	  <td colspan="2">RN03 – A compra poderá ser feita somente por clientes maiores de 18 anos.
	  </td>
	</tr>
  </tbody>
</table>



