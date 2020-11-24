Padrões de criação:

    Os padrões de criação abstraem o processo de instanciação. Eles ajudam a tornar um sistema independente de como seus objetos são criados, compostos e representados -> difinir um conjunto menor de comportamentos fundamentais.
    Se torna importante à medida que os sistemas evoluem no sentido de depender mais da composição de objetos do que da herança de classes.
    Todos encapsulam conhecimento sobre quais classes concretas são usadas pelo sistema.
    Ocultam o modo com as instâncias destas classes são criadas e compostas.
    Podem ser tanto estáticos (compilação) quanto dinâmicos (execução).
    
    Discussão do final do capítulo sobre os padrões de criação:
        Existem duas maneiras comuns de parametrizar um sistema pelas calsses de objetos que ele cria. Uma é criar subclasses da classe que cria os objetos -> Facrory Method -> desvantagem: pode gerar uma cascata de modificações encadeadas -> as pessoas normalmente usam Factory Method como a maneira padrão de criar objetos, mas não é necessãrio quando a classe que é instanciada nunca muda ou quando a instanciação ocorre em uma operação que subclasses podem facilmente redefinir, tal como uma operação de inicialização;
        A outra forma baseia-se mais na composição de objetos: defina um objeto que seja responsável por comhecer a classe dos objetos-produto e torne-o parâmetri do sistema -> Abstract Factory (o objeto-fábrica produz objetos de várias classes), Builder (o objeto-fábrica constrói incrementalmente um objeto complexo usando um protocolo) e Prototype (objeto-fábrica constrói um objeto-produto copiando um objeto prototípico).
        Projetos que usam Abstract Factory, Builder e  Prototype são ainda mais flexíveis do que aqueles que utilizam Facotry Method, porém, eles são mais complexos.