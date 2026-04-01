# levantamento_requisitos e-commerce Mercado Livre
Levantamento de requisitos, desenvolvimento de uma narrativa de caso de uso e a criação do diagrama de uso, do e-commerce Mercado Livre.

# LEVANTAMENTO DE REQUISITOS:  E-COMERCE MERCADO LIVRE

#FUNCIONAIS
+ Cadastrar;
+ Logar;
+	Comprar;
+ Devolver;
+	Colocar no carrinho;
+	Excluir do carrinho;
+	Colocar na lista de favoritos;
+	Avaliar o produto;
+	Postar um produto;
+	Acompanhar a solicitação;
+	Pedir suporte;
+	Contatar o vendedor;
+	Área de recomendações em base da pesquisa;
+	Compartilhar publicações em outras redes via link;
+	Acessar streaming;
+	Selecionar categorias;
+	Filtrar dados;
+	Navegar pelo menu;

#NÃO FUNCIONAIS
+	Segurança
+	Salvar sessão
+	Desempenho
+	Usabilidade
+	Portabilidade
+	Transações financeiras
+	Login

## Narrativa do caso de uso

Primeira Narrativa:
## Fluxo Principal: Comprar
+	Cliente acessa o item;
+	Seleciona o modelo e a quantidade;
+	Sistema calcula o frete;
+	Sistema calcula o valor total;
+	Cliente confere o pedido;
+	Sistema requisita a forma de pagamento;
+	Cliente realiza o pagamento;
+	Sistema confirma o pedido.
## Fluxo Alternativo: Pedido modificado após pagamento final
+	Cliente cancela o pedido;
+	Sistema estorna o dinheiro;
+	Cliente adiciona/remove o item da sacola;
+	Cliente confere o pedido;
+	Sistema requisita a forma de pagamento;
+	Cliente realiza o pagamento;
+	Sistema confirma o pedido.
## Fluxo de Exceção: Item Indisponível 
+ Sistema verifica estoque
+ Se indisponível: alerta cliente
+ Cliente escolhe substituto ou remove
+ Sistema atualiza pedido
  
====================================================

Segunda Narrativa:
## Fluxo Principal: Postar Produto
+	Cliente realiza o pedido;
+	O administrador recebe o pedido;
+	O administrador recebe o pagamento;
+	Valida o estoque
+	Emite a NFC-E
+	O administrador envia o produto;
+	Emite o código de rastreio
+	O administrador atualiza o sistema sobre o status do pedido;
+	Sistema fornece informações do pedido.
## Fluxo Alternativo: Devolução do produto
+	Cliente negocia na plataforma;
+	Sistema fornece o código do produto para rastreio.
+	Cliente posta o produto nos correios;
+	Produto chega a um posto de logística;
+	Produto é devolvido ao administrador.
+	Administrador envia o valor do produto para o sistema;
+	Sistema estorna o valor para o cliente.

## Fluxo de Exceção: Envio incorreto
+	O cliente abre o site;
+	Procura o produto;
+	Realizou o pedido;
+	Sistema validou;
+	Ocorreu um erro: O sistema direcionou um pedido com número repetido por conta de uma função mal testada no código, resultando em dois produtos no mesmo pedido, quando o usuário comprou apenas um;
+	O sistema liberou o pagamento apenas do valor de um produto;
+	O usuário fez o pagamento;
+	O sistema validou;
+	O produto foi liberado para envio no centro logístico;
+	O sistema gerou a NFC-E;
+	O produto foi despachado;
+	O código de rastreio foi gerado;
+	O cliente recebeu dois produtos;
+	PROBABILIDADE 1:Prejuízo financeiro, pois o cliente agiu de forma desonesta;
+	PROBABILIDADE 2:  Fluxo alternativo de devolução.
  
==============================================

Terceira Narrativa:
## Fluxo Principal: Adicionar ao carrinho
+	Cliente acessa o item;
+	Seleciona o modelo e a quantidade;
+	Cliente adiciona o produto ao carrinho.
## Fluxo Alternativo: Item Indisponível 
+ Sistema verifica estoque
+ Se indisponível: alerta cliente
+ Cliente escolhe substituto ou remove
## Fluxo de Exceção: 
+	Cliente adiciona o produto no carrinho;
+	Um bug faz com que o produto desapareça do carrinho após o usuário fechar a página;
+	Usuário é forçado a comprar diretamente sem conseguir acumular itens para comprar junto.

## Diagrama de Caso de Uso

<img width="700" height="630" alt="diagrama de uso" src="https://github.com/user-attachments/assets/6fa373cf-5437-4fd9-9623-97bcef4380b1" />


