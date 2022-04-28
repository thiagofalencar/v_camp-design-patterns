# v_camp-design-patterns
Este exercício tem o objetivo exercitar a aplicar os conceitos de Design Patterns, SOLID e Teste Unitário em um cenário que todos nós conhecemos, sabemos que alguns dos exemplos abaixo é um exemplo clássico de *_overengineering_* utilizando os padrões, mas com certeza ajudará bastante na consolidação dos conhecimentos.


## Requisitos
- [ ] Clone esse repositório para o seu usuário de forma pública
- [ ] Compartilhe o exercício no grupo *V_Camp* após conclusão.
- [ ] Adicione no repositório um passo a passo para execução deste projeto.
- [ ] Envie imagens da atividade sendo executada para exemplificação do funcionamento.
- [ ] Ter concluído os cursos da Udemy:
  - [ ] [Java Design Patterns & SOLID Design Principles](https://valtech.udemy.com/course/design-patterns-in-java-concepts-hands-on-projects/).
  - [ ] [Testes unitários em JAVA: Domine JUnit, Mockito e TDD](https://valtech.udemy.com/course/testes-unitarios-em-java/).

## Atividade:

### Builder: Catálogo de Produtos.
Utilize o padrão `Builder` para construir classe chamada `Catalog` de objetos para uma loja virtual voltada para um Outlet. Onde deverão ter 4 tipos diferentes de produtos que devem possuir pelo menos 3 características comuns (Peso, Preço e SKU) a todos e outras 2 individuais que você pode decidir a seu critério, o método `getAllProducts` deve publico para expor a listagem de produtos carregados. Todas as instâncias desses produtos devem ser adicionadas a classe `ProductInventory`.

### Singleton: Inventário de produtos
Utilize o padrão `Singleton` para criar classe chamada `ProductInventory` que faça o gerenciamento de estoque de produtos. Deverão ser criada threads de instâncias da classe `Cart` onde essas instâncias do carrinho posso consultar(`getProductQuantity`), diminuir(`removeProductFromStock(Int: quantity)`) e reservar(`blockProductsFromStock`).

Notes: *Para esse exercício, podemos armazenar os estoques em propriedades nessa classe, para que não exista a necessidade de uma integração com o banco de dados. Por padrão, cada produto cadastrado, deve ter 10 itens em estoque.*

### Composite: Carrinho de compra
Utilize o padrão `Composite` para criar uma classe chamada `Cart` que simula um carrinho de compras, onde instâncias dos produtos serão compartilhadas pela classe `Catalog` serão utilizados por essa classe que deverá ter a opção de adicionar produtos(`addItem(Int: quantity)`), remover produtos(`removeItem(Int: quantity)`), quantidade de produtos(`getProducts`), preço total(`getTotal`), peso total(`getWeight`) e a Classe `Shipping` e que também possui instâncias de `Aero` e `Road`.


### Factory: Frete
Crie as classes `Shipping`, `Aero` and `Road` and utilize o padrão Factory para criar instâncias de classes de frete(`Road` e `Aero`), onde a classe `Road` deverá ser instanciadas para compras com peso acima de 10 kg e o aéreo para pesos inferiores. Para o cálculo, deverá ser utilizada a classe `Cart`, que deve expor o método com o `getProducts`, `getTotal` and `getWeight`. O valor do frete deve ser 10% do valor da compra onde o valor mínimo deve ser `R$ 7.99`. Também deve ser somado ao valor do frete `R$ 1` para cada produto.

### Iterator: Listagem de compras
Crie uma classe chamada `OrderList` que utilize o padrão `Iterator` e `Singleton` para armazenar uma lista de instâncias da classe `Order`, que irá ser consumida pela classe `Backoffice` para varrer a listagem de pedidos e exibir os dados referente aos pedidos.

### Facade: Order
Crie a classe chamada `Order` que irá receber uma classe do tipo `Cart` and `Shipping` e irá expor os métodos para alteração do status do pedido([`pending`, `paid`, `completed`, `shipped` and `cancelled`]), expondo os métodos referente a essas alterações. Essa classe deve ser utilizada para realizar todas as mudanças do pedido.

### Observer: Backoffice
Crie uma classe chamada `Backoffice` que irá exibir os dados do pedido a equipe de despacho de pedido, onde sempre que o status do pedido, frete e carrinho forem alterados, o método `renderOrderList` precisa estar inscrito para ser chamado e exibir a listagem de pedidos. 

---

### Importante:
- [ ] Crie testes unitários para todo o projeto.
- [ ] Utilize os princípios do SOLID no desenvolvimento do seu código.
- [ ] Crie um exemplo de chamada de todas as classes simulando o processo de uma loja virtual.
- [ ] Sempre use termos em inglês para definição de variáveis, classes e etc...

### Observações: 
- Fique a vontade para implementar classes, métodos, propriedades ou qualquer características que julgar necessário para melhor funcionamento deste exercício e adequação ao cenário proposto.
- O projeto pode ser feito em linha de comando ou um serviço Web simples.
- Não deixe de seguir o escopo acima ou implementar algum requisito.
 
