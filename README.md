# Pizzaria
Trabalho final de linguagens de programação. 

Tópicos:

Introdução 
Requisitos do sistema 
Estrutura 
   - Principais Classes e métodos. 
   - Views 
Código Fonte 

--> Introdução 
  
  O projeto foi desenvolvido em JAVA.
  
  O sistema é desenvolvido para uma pizzaria mas abstrai qualquer estabelecimento comercial que permite ao cliente fazer pedidos e somente retirar ou pedir que seu pedido seja entregue em sua residência. O sistema apresenta views práticas e objetivas e uma ágil função de busca para clientes já cadastrados desobrigando o cliente a passar o endereço todas as vezes que realizar um pedido. Foi implementado um sólido sistema de gerenciamento de produtos e funcionários e um breve organizador de entregas de acordo com a disponibilidade de cada entregador. 


--> Requisitos 

1. O sistema ira permitir ao cliente fazer um pedido pessoalmente ou pelo telefone. 
  1. Um atendente irá registrar/buscar o cliente pela interface. 
    1. Se o pedido for para entrega o cliente deverá fornecer um endereço caso não tenha cadastro prévio. 
    2. O atendente irá inserir os produtos pedidos e suas quantidades. 
    3. Um entregador será selecionado para realizar a entrega. 
    4. O atendente então deverá perguntar pela forma de pagamento e se for em dinheiro o cliente de informar para quanto precisa de troco. 
    5. Após finalizar o pedido o produto entrara na fila para o preparo. 
2. O sistema irá permitir ao atendente exibir o cardápio organizado por categorias sempre que solicitado. 
3. O sistema irá permitir ao atendente acompanhar o pedido pelo sistema. 
4. O sistema irá permitir ao atendente mudar os status dos pedidos para: na fila, preparo, entrega, entregue, cancelado. 
5. O sistema irá permitir ao gerente criar/editar/remover produtos e seus respectivos ingredientes assim como as categorias de cada um. 
6. O sistema irá permitir listar/cadastrar/editar/remover clientes. 
7. O sistema irá permitir listar a todos os produtos. 
8. Ao gerente, listar/cadastrar/editar/remover funcionários. 

4) Estrutura 

--> UML 
	
![UML](https://raw.githubusercontent.com/dcresnitzky/LCP/master/Uml_final.PNG)


--> Principais Classes e métodos.

  O sistema é composto por 3 classes principais: Pessoa, Pedido e Produto.
  
  Para a classe Pessoa há apenas 1 atributo, o nome da pessoa que é do tipo String. 
  
  Há 2 classes-filha de pessoa, Cliente e Funcionário. Para a classe Cliente há 2 atriutos, um ArrayList de Endereços - uma classe com atributos como rua, número, bairro, entre outros - e o telefone do tipo int. Na classe Funcionário, há 3 atributos, o registro do funcionário, que é uma variável do tipo int. Os outros atributos são login e senha do tipo int. O login e senha explicam-se pelo fato do sistema usar diferentes tipos de autenticação para cada classe de usuário. Para efetuar o login no sistema, as classes Atendente e Gerente, que são filhas de funcionário, implementam a interface Autenticável que fornece os métodos para a autenticação. A classe Atendente tem 1 atributo, o ramal do telefone do atendente. Uma terceira classe filha de funcionário foi criada, a classe Motoboy. Essa classe tem 1 atributo, do tipo String: a placa da moto.
  
  A classe Produto é a classe que abstrai os produtos vendidos pela pizzaria. Ela possui os atributos: código do tipo int, nome do tipo String, categoria do tipo Categoria, preço do tipo double e ingredientes que é um ArrayList do tipo Ingrediente. As classes Categoria e Ingrediente, mencionadas na classe Produto, possuem apenas 1 atributo cada uma: nome do tipo String.
  
  Há um classe que se relaciona com a classe Produto que se chama ProdutoPedido. Essa classe possui 3 atributos: produto do tipo Produto, quantidade do tipo int e obs(observacoes) do tipo String. ProdutoPedido existe para relacionar adequadamente a quantidade de cada produto dentro dos Pedido bem como suas respectivas observações. Caso um cliente queira uma pizza de calabresa sem tomate, essa nota será armazenada no campo observação.
  
   A terceira classe principal é a classe Pedido. Essa classe possui 14 atributos: cliente do tipo Cliente, produtos que é um ArrayList de ProdutoPedido, atendente do tipo Funcionario, entregador do tipo Funcionario, endereço do tipo endereço, entrega do tipo boolean, desconto, taxaEntrega e valor do tipo double, formaPagamento do tipo int, troco do tipo double, data e hora do tipo Date e status do tipo int. Caso o pedido seja falso a variável endereço pode estar vazia.
  
   A variável formaPagamento é do tipo int pois se o cliente escolher a dinheiro como forma de pagamento, a variável formaPagamento será definida com o valor 0. Se a forma de pagamento escolhida não for dinheiro, a variável troco receberá valor 0 e a variável formaPagamento será setada com valor 1 para cartão de débito, 2 para cartão de crédito, 3 para vale refeição, e assim por diante. 


iii) Views

Login

![Login](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/Login.PNG)

MainView

![MainView](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/MainView.PNG)

Novo Pedido

![NovoPedido](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/NovoPedido.PNG)

Clientes

![Clientes](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/Clientes.PNG)

Produtos

![Produtos](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/Produtos.PNG)

Cardapio

![Cardapio](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/Cardapio.PNG)

Funcionarios

![Funcionarios](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/Funcionarios.PNG)

Novo Produto

![NovoProduto](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/NovoProduto.PNG)

Detalhes Do Produto

![DetalhesDoProduto](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/DetalhesDoProduto.PNG)

Confirmacao

![Confirmacao](https://raw.githubusercontent.com/dcresnitzky/LCP/master/views/Confirmacao.PNG)

5) Código fonte 

Nos arquivos. 
