Facotry Method(Virtual Constructor):

    Intenção:
        Definir uma interface para criar um objeto, mas deixar as subclasses decidirem que classes instanciar. O Factory Method permite adiar a instanciação para subclasses.

    Aplicabilidade:
        Uma classe não pode antecipar a classe de objetos que devem criar;
        Uma classe quer que suas subclasses especifiquem os objetos que criam;
        Classes delegam responsabilidades para uma dentre várias subclasses auxiliares, e você quer localizar o conhecimento de qual subclasse auxiliar que é a delegada.

    Participantes:
        Product:
            define a interface de objetos que o método fábrica cria;
        Concrete Procuct:
            implementa a interface product;
        Creator:
            declara o método fábrica, o qual retorna um objeto do tipo Product. Creator pode também definir uma implementação por omissão do método factory que retorna por omissão um objeto Concrete Product.
            pode chamar o método factory para criar um objeto Product;
        ConcreteCreator:
            redefine o método fábrica para retornar a uma instância de um Concrete Product.

    Colaborações:
        Creator depende das suas subclasses para definir o método fábrica de maneira que retorne uma instância de um Concrete Product.

    Consequências:
        Os Factory Methods eliminam a necessidade de anexar classes específcas das aplicações no código. O código lida somente com a interface de Product, portanto, ele pode trabalhar com quaisquer classes Concrete Product definidas pelo usuário;
        Uma desvanagem -> os clientes podem ter que forncer subclasses da classe Creator somente para criar objeto Concrete Product em particular;
        Fornece ganchos para subclasses:
            Criar objetos dentro de uma classe dentro de uma classe com um método fábrica é sempre mais flexível do que criar um objeto diretamente -> dá às subclasses um gancho para forncer uma versão extendida de um objeto;
        Conecta hierarquias de classes paralelas**:
            Não necessariamente os métodos fábricas precisam ser chamados apenas pelo Creator -> pode ser por hierarquia de classes paralelas;
            **Hierarquia de classes paralelas: quando uma classe delega alguma das suas responsabilidades para uma classe separada.

    Implementação:
        Duas variedades principais:
            (1)Caso em que a classe Creator é uma classe abstrata e não fornece uma implementação para o método fábrica que ela declara:
                Exige subclasses para definir uma implementação porque não existe uma omissão razoável;
            (2)Caso quando o Creator é uma classe concreta e fornece uma implementação por omissão para o método fábrica:
                Concrete Creator usa o método fábrica principalmente por razões de flexibilidade;
        Métodos Fábrica parametrizados:
            Permite ao método fábrica criar múltiplos tipos de produtos -> o parâmetro idntifica o produto a ser criado;
        Convenções de nomeclatura:
            DoMakeClass();

    Padrões relacionados:
        Abstract Factory, Templates Methodos, Prototypes.