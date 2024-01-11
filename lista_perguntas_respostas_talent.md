## Junior:

- O que é uma linguagem Tipada? Consegue dar exemplos?
    - **R:** São linguagens que obrigam o desenvolvedor definir o tipo da variável. Por exemplo: int custo = 10. Estou obrigando que a minha variável custo tem que se do tipo INT se em algum lugar do código eu tentar colocar custo = "andré” o compilador ou interpretador vai dar um erro!
- Qual a diferença entre uma linguagem Compilada e Interpretada?
    - **R:** Em uma linguagem compilada, a máquina de destino traduz o programa diretamente. Em uma linguagem interpretada, o código fonte não é traduzido diretamente pela máquina de destino. Em vez disso, um programa diferente, o interpretador, lê e executa o código. Exemplos de algumas linguagens interpretada: Python, R e Javascript. Compiladas: C, C++, Rust e GO… Java
- O que são classes e objetos e qual a sua relação?
    - **R:** A classe é um modelo, um template. O objeto seria a classe materializada, ou seja, um objeto com os devidos atributos deste modelo (template): uma casa azul, térrea, com garagem, construída em 2015, com valor venal de $ 100.000,00, com área construída de 60m2, etc.
    - **R:** De forma mais baixo nível. Classe é um template o objeto é sua instancia. A classe não está alocada em memória o objeto está!
- O que é um framework? Consegue dar exemplos?
    - **R:** Uma biblioteca que oferece uma gama de funcionalidades pré prontas. Geralmente usamos frameworks para facilitar a vida do desenvolvedor. Ao invés de criar coisas do zero, usamos frameworks que já possuem as funcionalidades que desejamos para desenvolvermos mais rapidamente. Exemplos: OpenCV, Flask, dotnet, FastAPI, React, Angular…
- O que é uma API? De um exemplo de API que você já trabalhou?
    - **R:** O conceito de API nada mais é do que uma forma de comunicação entre sistemas. Ou seja, elas permitem a integração entre dois sistemas, em que um deles fornece informações e serviços que podem ser utilizados pelo outro, sem a necessidade de algum dos sistemas conhecer detalhes de implementação do software. Exemplos: Criação de Rest API usando algum framework existente (Flask, FastAPI, AspNet Core, Springboot…)

## Pleno

- Ja ouviu falar de SOLID? Poderia explicar o conceito?
    - **R:** SOLID são cinco princípios da programação orientada a objetos que facilitam no desenvolvimento de softwares. É um facilitador  que torna o código mais coeso, além de mais fácil de manter, estender, adaptar e ajustar conforme alterações de escopo. Além disso, ele faz com que o código seja testável e de fácil entendimento, extensível e forneça o máximo de reaproveitamento.
- O que são design patterns e quais já usou?
    - **R:** Design patterns ou padrões de design são soluções já testadas para problemas recorrentes no desenvolvimento de software, que deixam seu código mais manutenível e elegante, pois essas soluções se baseiam em um baixo acoplamento.
        - Exemplos de DP:
            - Singleton
            - Mediator
            - Observer
            - Factory
            - Abstract Factory
            - Facade
- O que é um cache? Quais os seus benefícios?
    - **R:** Cache serve como armazenamento temporário e geralmente é usado para trazer ganhos de performance. Por exemplo, vc pode ter um cache de requisição onde a resposta destas são armazenadas nesse armazenamento temporário e quando uma requisição futura chega ao invés de executar ela novamente por completo vc busca nesse cache. Se existir vc pega do cache. Isso traz ganhos de performance. Vc pode ter cache de banco de dados… a idéia é a mesma… evitar reprocessamento iguais…
- É comum comprimirmos a respostas das nossas API, quais as vantagens disto? E as desvantagens?
    - **R:** Os benefícios é que a requisições comprimidas tem um tamanho (mb…kb) reduzido e isso faz o usuário trafegar menos dados ao abrir uma aplicação web. Ou seja, o usuário tem a percepção das coisas "abrirem mais rapidamente”. A maior desvantagem é que o processo de compressão acontece no backend e isso gera mais processamento e mais custos $$.

## Senior

- SQL Puro ou ORM? Quando usar cada um?
    - **R:** Depende! SQL Puro é performático, porém é mais complexo de lidar pois o código fonte do projeto fica muito mais poluído. ORM você tem um código menos poluído porém a legibilidade do seu código fica muito melhor, porém ele gasta mais recursos para ser processado.
        - Usaria SQL Puro em um projeto voltado para performance ou com relações nos dados bastante complexa. Pois no ORM relações complexa são difíceis de ser mapeadas.
        - ORM em projetos com um banco de dados com tabelas com relações mais simples.
        - E podemos usar os dois juntos 😄!
- Qual a diferença entre VMs (Virtual Machines) e Containers.
    - **R:** A virtualização dá garantia de recursos para sua aplicação em nível de hardware, algo que não ocorre na conteinerização. Ou seja, quando criamos a VM precisamos especificar quanto de memória ela irá ter, qual o processador, qual a interface de rede…
- O que é o Kubernetes? E por que usamos?
    - **R:** Kubernetes é um orquestrador de containers. Ele facilita a vida no gerenciamento dos containers de forma que podemos escalar nossas aplicação de uma forma muito rápida com pouca interação manual.
- Sua API está com uma baixa performance. O que vc avalia pra melhorá-la?
    - **R:** Monitora a api usando algumas ferramenta tipo Elastic, Datadog ou New Relic. Avalia througput, número de erros dos endpoints (rotas, urls)… E baseado nessa análise (profile) vai identificando quais endpoints estão mais "pesados” (onerosos) para melhorá-los.  A melhoria pode ser feita de várias formas:
        - Complexidade do algoritmo O(n), O(nˆ2)…
        - Melhoria das consultas no banco
        - Melhorias de "hardware” (Escalabilidade Vertical), tanto no banco quanto no servidor da API
        - Escalar a API horizontal, mas se for uma API muito vinculada a Banco de Dados, isso pode ser tornar um problema.
