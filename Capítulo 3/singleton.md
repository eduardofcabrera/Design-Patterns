Singleton

    Intensão:
        Garantir que uma classe tenha somente uma instância e fornecer um ponto global de acesso para a mesma.

    Aplicabilidade:
        Preciso haver apenas uma instância de uma classe, e essa instância tiver que dar acesso aos clientes através de um ponto bem conhecido;
        A única instância tiver de ser extensível através de subclasses, possibilitando aos seus clientes usar uma instância estentida sem alterar o seu código.

    Participantes:
        Singleton:
            define uma operação Instance que permite aos clientes acessarem sua única instânciam Instance é uma operação de classe;
            pode ser responsável pela criação da sua própria intância única.

    Colaborações:
        Os clientes acessam uma instância Singleton unicamente pela operação Instance do Singleton.

    Consequências:
        Acesso controlado à instância única:
            encapsula a sua única instância, possui controle total sobre como e quando os clientes a acessam;
        Espaço de nomes reduzidos:
            representa uma melhoriaem relação ao uso de variáveis globais -> evita a poluição do espaço de nomes com variáveis globais que armazenam instâncias úicas;
        Permite um refinamento de operações e da representação:
            pode ter subclasses e é facil configurar uma aplicação com uma instância dessa classe estendida -> em tempo de execução;
        Permite um número variável de instâncias:
            permite mais de uma instância para a classe Singleton -> controlar o número de instâncias -> Instance necessita ser mudada;
        Mais flexível do que operações de classe.

    Implementação:
        Garantindo um única implementação:
            classe deve ser escrita de maneira que somente uma instância possa ser criada;
            ex:
                Singleton* Singleton::_instance = 0;
                Singleton* Singleton::Instance() {
                    if (_instance == 0) {
                        _instance = new Singleton;
                    }
                    return _instance;
                }
        Criando subclasse da classe Singleton:
            em essência, a variável que referencia a instância do singleton dever ser iniciada com um instância da subclasse (não entendi muito bem).

    Padrões relacionados:
        Abstract Factory, Builder e Prototype.
        

    
