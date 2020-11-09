Builder:

    Intenção:
        Separar a construção de um objeto complexo da sua representação de modo que o mesmo processo de construção possa criar diferentes representações.
    
    Aplicabilidade:
        O algoritmo para criação de um objeto complexo deve ser independete das paretes que compõem o objeto e de como elas são montadas;
        O processo de construção deve permitir diferentes representações para o objeto que é construído.
    
    Participantes:
        Builder:
            especifica uma interface abstrata para a criação de partes de um objeto-produto;
        Concrete Builder:
            constrói e monta partes do produto pela implementação da interface de Builder;
            define e mantém a representação que cria;
            fornece uma interface para recuperação do produto (Get);
        Director:
            constrói um objeto usando a interface de Builder;
        Product:
            representa o objeto complexo em construção. Concrete Builder constrói a representação interna do produto e define o processo pelo qual ele é montado;
            inclui classes que definem as partes constituintes, inclusive as interfaces para a montagem das partes no resultado final.

    Colaborações:
        O cliente cria o objeto Director e o configura com o objeto Builder desejado;
        Director notifica o construtor sempre que uma parte do produto deve ser construída;
        Builder trata solicitações do diretor e acrescenta partes ao produto;
        O cliente recupera o produto do construtor.

    Consequências:
        Permite variar a representação interna de um produto:
            O objeto Builder fornece ao diretor uma interface absrata para a construção do produto. A interface permite ao construtor ocultar a representação, estrutura interna e como é montado o produto. -> Tudo o que se precisa fazer para mudar a sua representação interna é definir um novo tipo de construtor.
        Isola o código para construção e representação:
            Melhora a modularidade pelo encapsulamento da forma como um objeto complexo é construído e representado. 
        Oferece um controle mais fino sobre o processo de construção:
            O Builder constrói o produto passo a passo sob o controle do diretor. Somente quando o produto está terminado o diretor o recupera do construtor.
    
    Implementação:
        Existe uma classe abstrata Builder que define uma operação para cada componente que um diretor pedir -> uma classe Concrete Builder redefine as operações para os componentes que lea está interessada em criar.
        Interface de montagem e construção:
            Os Builder constroem seus produtos de forma gradual -> a interface Builder deve ser geral o bastante para permitir a construção de produtos para todos os tipos de construtores concretos -> um modelo onde os resultados das solicitações de construção são simplismente acrescentados ao produto é normalmente suficiente.
        Por que não classes abstratas para produtos?
            Em casos comuns, os produtos produzidos pelos construtores conretos diferem tão grandemente na sua representação que há pouco a ganhar ao dar diferentes produtos uma classe-pai comum -> o cliente está em posição de saber quais subclasses concretas de Builder estão em uso e pode tratar os seus produtos de acordo.

    Padrões relacionados:
        Abstract Factory, Composite.
        