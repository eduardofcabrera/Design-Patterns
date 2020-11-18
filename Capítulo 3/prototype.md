Prototype:

    Intensão:
        Especificar os tipos de objetos a serem criados usando uma intância-protótipo e criar novo objetos pela cópia desse protótipo.

    Aplicabilidade:
        Sistema tiver que ser independente de como os seus produtos são criados, compostos e representados;
        As classes a instanciar forem especificadas em tempo de execução;
        Evitar a construção de uma hierarquia de classes de fábricas paralelas à hierarquia de classes de produto;
        Intâncias de uma classe puderem ter uma dentre poucas combinações diferenetes de estados. Pode ser mais convincente instalar um número correspondente de protótipos e cloná-los, ao invés de instanciar a classe manualmente, cada vez com um estado apropriado.

    Participantes:
        Prototype:
            declara uma interface para clonar a si próprio;
        Concrete Prototype:
            implementa uma operação para clonar a si próprio;
        Client:
            cria um novo objeto solicitando a um protótipo que clone a si próprio.

    Colaborações:
        Um cliente solicita a um protótipo que este clone a si próprio.

    Consequências:
        Oculta as classes de produtos concretas do cliente, desta forma reduzindo, o número de nomes que o cliente necessita saber;
        Permitem a um cliente trabalhar com classes específicas de uma aplicação sem necessidade de modificação;
        Acrescenta e remove produtos em tempo de execução -> permite incorporar uma nova classe concreta de produto a um sistema, simplismente registrando uma instância protótipo com o cliente;
        Especifica novos objetos pela variação de valores -> sistemas altmente dinâmicos permitem definir novos comportamentos através da composição de objetos -> especificação de valores para as variáveis de um objeto -> efetivamente define novos tipo de objetos pela instanciação das classes existentes e registrando instâncias como protótipos dos objetos-clientes  -> um cliente pode exibir um novo comportamento através da delegação de responsabilidades para o protótipo;
        Especifica novoso objetos pela variação da estrutura -> construir objetos com partes e subpartes -> instanciar estruturas complexas -> implemente um clone por replicação (deep copy);
        Reduz o número de subclasses -> permite clonar um protótipo em vez de pedir a um método fábrica para construir esse objeto -> não necessita de nenhuma hierarquia de classe Creator;
        Configura dinamicamente uma aplicação com classes -> não entendi muito bem a explicação;
        O principal ponto fraco -> para cada subclasse de Prototype -> implementar operação Clone.

    Implementação:
        Protoype é particularmente útil em linguagens estáticas como C++, na qual classes não são objetos e há poucas informações sobre tipos no tempo de execução. 
        Gerenciador de protótipos -> quando o número de protótipos não é fixo (dinâmico) -> manter um sistema de registro dos protótipos disponíveis -> chave e valor;
        Operação clone -> parte mais difícil, principalmente quando as estruturas dos objetos contêm referências circulares -> a pergunta: clonar objetos significa clonar suas variáveis de instância, ou o clone e o original simplismente compartilham variáveis -> para estruturas complexas -> clone e original indepentes -> apontam para lugares distintos (suas variáveis). Obs: Caso o objeto tiver as operações salvar e carregar não necessita de Clone;
        Iniciar clones -> dependendo do prototype necessita passar variáveis na iniciação do objeto -> pode ser por meio do Clone() ou até por algum método como o Constructor();

    Padrões relacionados:
        AbstractFactory, Composite e Decorator;
        
