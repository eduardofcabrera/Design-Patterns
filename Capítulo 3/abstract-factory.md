Abstract Factory (kit):

    Intenção:
        Fornecer uma interface para a criação de famílias de objetos relacionados ou dependentes sem especificar suas classes concretas.

    Aplicabilidade:
        Um sistema deve ser independente de como seus produtos são criados, compostos ou representados;
        Um sistema deve ser onfigurado como um produto de uma família de múltiplos produtos;
        Uma família de objetos-produtos for projetada para ser usada em conjunto, e você necessita garantir essa restrição;
        Você quer fornecer uma biblioteca de classes de produtos e quer revelar somente suas interfaces, não suas implementações.

    Participantes:
        Abstract Factory:
            declara uma interface para operações que criam objetos-produto abstratos;
        Concrete Factory:
            implementa operações que criam objetos-produto concretos;
        Abstract Product:
            declara uma interface para um tipo de objeto-produto;
        Concrete Product:
            define um objeto-produto a ser criado pela correspondente fábrica concreta;
            implementa a interface Abstract Product;
        Client:
            usa somente as interfaces delcares pela ABstract Factory e Abstract Product.

    Colaborações:
        Normalmente uma única instância de uma classe ConcreteFactory é criada em tempo de execução. Essa fábrica concreta cria objetos-produtos que têm uma implementação particular. Para criar diferentes objetos-produtos -> diferentes fábricas concretas''
        Abstract Factory adia a criaçãodos objetos-produtos para as suas subclasses Concrete Factory.

    Consequências:
        Isola as classes concretas -> encapsula a responsabilidade e o processo de criar objetos-produtos, isola os clientes das classes de implementação;
        Torna fácil a troca de famílias de produtos -> a classe de uma família só aparece quando é instanciada;
        Promove a harmonia entre os produtos;
        É difícil de suportar novos tipos de produtos -> a interface da Abstract Factory fixa o conjunto de produtos que podem ser criados -> exige estender a interface sempre que for suportar outro tipo de produto.

    Dicas de implementação:
        Fábricas como Singleton:
            Necessita somente de uma instância de uma Concrete Factory por família de produto;
        Criando os produtos:
            Fica a cargo das subclasses de Concrete Products criá-los efetivamente, a maneira mais comum de fazer isso é criar um Factory Method -> exige criar uma nova subclasse de uma fábrica concreta para cada família de produtos;
            Ou pode-se utilizar o Prototype para não haver a necessidade de criar uma nova subclasse de uma fábrica concreta para cada família de produtos;
        Definindo fábricas extensíveis:
            O acréscimo de um novo tipo de produto exige a mudança da interface de Abstract Factory e de todas as classes que dependem dela;
            Um modo flexível, mas menos seguro -> acrescentar um parâmetro às operações que criam objetos que identifica o tipo de produto;
            Porém mesmo com isso, todos os produtos retornados ao cliente com a mesma interface abstrata conforme especificado pelo tipo de retorno -> não saberá identificar.

    Padrões relacionados:
        Factory Method, Prototype, Singleton.

        

