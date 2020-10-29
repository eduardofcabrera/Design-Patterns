Introdução:

    _______________________________________________________________________________________________

    |Encapsulamento: 
        Separar o programa em partes, o mais isolado possível.
        O encapsulamento serve para controlar o acesso aos atributos e métodos de uma classe.
        Sempre utilizar private, a menos que seja constantes. 
        Ao utilizar public tende-se a ligar-se a uma implementação em particular o que dificulta
        na reutilização e na flexibilização.
        Nível de classe: determinar o acesso de uma classe inteira que pode ser public ou 
        Package-private (padrão java)
        Nível de membro: determinar o acesso de atributos ou métodos de uma classe que podem
        ser public, private, protected ou Package-private.
        Para ter um método encapsulado utiliza-se um modificador de acesso que geralmente é
        público, além do tipo de retorno dele (GET e SET).
     
    |Herança:
        Criar novas classes a partir de classes já existentes, aproveitando-se de características
        já existentes na classe a ser estendida.
        Permite o reuso.
        Superclasses -> mais genéricas.
        Subclasses -> mais especializadas.
        As subclasses herdam todas as características das suas superclasses (variáveis e métodos)

    |Polimorfismo:
        Duas ou mais classes derivadas de uma mesma superclasse podem invocar métodos que
        têm a mesma identificação, assinatura, mas comportamentos distindos, especializados 
        para cada classe derivada, usando para tanto uma referência a um objeto do tipo da
        superclasse.
        Implica, também, que uma operação de uma classe pode ser implementada por mais de 
        método.
        Métodos finais, portanto private também, são impedidos de polimorfismo.
        O método a ser aplicado só será "escolhido" na execução -> dynamic binding.

    |Instância:
        Objeto cujo comportamento e estado são definidos pela classe.
        As instâncias de uma classe compartilham o mesmo conjunto de atributos, embora sejam 
        diferentes quanto ao conteúdo desses atributos.
        Instância é a concretização de uma classe -> criação de um objeto.

    |Interface: 
        Cada operação declarada por um objeto especifica o nome da operação, os objetos que
        ela aceita como parâmetros e o valor retornado por ela, isso é chamado de assinatura.
        O conjunto de todas as assinaturas definido pelas operações de um objeto é a interface.
        A interface de um objeto caracteriza o conjunto completo de solicitações que lhe podem
        ser enviadas.
        A interface de um objeto nada diz sobre sua implementação.

    _______________________________________________________________________________________________

    Uma coisa que os melhores projetistas sabem que não devem fazer é resolver cada problema
    a partir de princípios elementares ou do zero -> "Reinventar a roda" -> reutilizar 
    soluções que funcionaram no passado.

    Padrões de projetos são descrições de objetos e classes comunicantes que precisam ser
    personalizadas para resolver um problema geral de projeto num contexto particular.

    A parte difícil sobre o projeto orientado a objetos é a decomposição de um sistema em objetos.
    As abstrações que surgem durante um projeto são as chaves para torná-lo flexível.

    Uma classe abstrata é uma classe cuja finalidade principal é definir uma interface comum
    para suas subclasses.
    Uma classe abstrata não pode ser instanciada -> postergará parte de, ou toda, sua implementação
    para operações definidas em subclasses.
    As operações que uma classe abstrata declara, mas não implementa, são chamdas 
    operações abstratas.

    Uma classe mixin é aquela cuja intenção é oferecer uma interface ou funcionalidade opcional
    a outras classes -> não pode ser implementada.
    Exigem herança múltipla.

    A classe de um objeto define como ele é implementado. A classe define o estado interno do
    objeto e a implementação de suas operações. Em contraste a isso, o tipo de um objeto se
    refere somente à sua interface - o conjunto de solicitações às quais ele pode responder.
    Um objeto pode ter muitos tipos, e objetos de diferentes classes podem ter o mesmo tipo.
    A classe define o tipo do objeto -> ela o instancia. 

    A herança de classe define a implementação de um objeto em termos da implementação de um 
    outro objeto.
    A herança de interface descreve quando um objeto pode ser usado no lugar de outro.

    Quando a herança é usada apropriadamente todas as classes derivadas de uma classe abstrata
    compartilharão sua interface. Isto implica que uma subclasse meramente acrecenta ou substitui
    operações da classe-mãe, e não oculta operações dela. Todas as subclasses podem então 
    responder a solicitações na interface da classe abstrata, tornando-se, todas, subtipos dela.
    Programe para uma interface, não para uma implementação.
    Benefícios:
        1. Os clientes permanecem sem conhecimento dos tipos específicos dos objetos que eles
        usam, contando que os objetos tenham adrência à interface que os clientes esperam.
        2. Os clientes permanencem sem conhecimento das classes que implementam estes objetos.
        Os clientes somente têm conhecimento das classes abstradas que definem a interface.
    Abstrair o processo de criação.

    Herança versus composição:
        Herança: caixa branca -> os anteriores das classes ancestrais são frequentemente 
        visíveis para as subclasses.
            Definida estaticamente em tempo de compilação e é simples de usar;
            É mais fácil modificar a implementação que está sendo reutilizada;
            Não pode mudar as implementações herdadas das classes ancestrais em tempo 
            de execução;
            Herança viola o encapsulamento -> as classes ancestrais frequentemente definem 
            pelo menos parte da representação física das suas subclasses -> as implementações
            são agarradas;
        Composiçao de objetos: caixa preta -> detalhes internos dos objetos não são visíveis.
            Obtida pela montagem ou composição de objetos -> funcionalidades mais complexas;
            Requer interfaces bem definidas;
            Definida dinamicamente em tempo de execução pela obtenção de referências a outros 
            objetos através de um determinado objeto;
            Requer que os objetos respeitem as interfaces uns dos outros;
            Não viola o encapsulamento;
            Menos dependências de implementação;
        Dar prefeência à composição de objetos ajuda a manter cada classe encapsulada e
        focalizada em uma única tarefa -> existirão mais objetos.
        Prefira a composição de objeto à herança de classe.

    Delegação:
        Maneira de potencializar a composição de objetos;
        Dois objetos são envolvidos no tratamento de uma solicitação, um objeto receptor 
        delega operações para o seu delegado;
        O receptor passa a si mesmo para o delegado para o delegado para permitir à operação
        delegada referenciar o receptor;
        Torna fácil compor objetos em tempo de execução -> traz ineficiência de tempo de execução;
        Software altamente parametrizado e dinâmico -> mais difícil de entender;

    A estrutura em tempo de execução de um programa orientado a objetos frequentemente
    apresenta pouca semelhança com sua estrutura de código. A estrutura de código é
    congelada em tempo de compilação; ela consiste de classe de relacionamento de herança
    fixo. A estrutura de tempo de execução de um programa consiste de redes em rápidas mudança
    de objetos comunicantes.
    Agregação -> objeto possui, ou é responsável por, outro objeto -> idêntico tempo de vida;
    Assosiação -> objeto meramente tem conhecimento de outro objeto -> mais fraco -> baixo acoplamento
    Em geral, as estruturas de tempo de execução não estão claras no código.

    A chave para a maximização da reutilização está na antecipação de novos requisitos e 
    mudanças nos requisitos existentes e em projetar sistemas de modo que eles possam evoluir de acordo.
    Não criar objetos pela especificação explícita de uma classe.
    Evitar solicitações codificadas inflexivelmente (hard-coded).
    Limite ao máximo as dependências de plataforma.
    Oculte as informações: como o objeto é representado, armazenado, localizado ou implementado.
    Algoritmos que provavelmente mudarão, deve ser isolado.
    Classes que são altamentes acopladas são difíceis de se reutilizar, uma vez que são
    dependentes uma das outras.
    Definir uma subclasse exige uma compreensão profunda da classe-mãe.
                                        


        




