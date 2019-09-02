# Continuous delivery and continuous deployment

Continuous delivery são práticas que garantem que o código está pronto para entrega, mas o deployment ainda é feito manualmente - ao contrário do continuous deployment. Uma das implicações técnicas necessárias para o continuous deployment é a capacidade de rollbacks e feature toggles - garantindo a existência de desativar features cujo o comportamento é inesperado. Apesar de no continous delivery a submissão da feature para produção não estar sendo feita, o código deve estar pronto para isto - passando por testes de QA, UAT, Smoke e nonfunctional. Mesmo com todos esses testes, não é garantido a experiência da feature em produção - causando possíveis acidentes. 
É necessária uma boa estratégia com logging, para poder gerar tracebility - a capacidade de saber a origem dos erros - durante incidentes, é necessário principalmente no continous delivery. Uma das vantagens dessa abordagem é a proximidade com o usuário final e rápida detecção de erros. A vantagem do continous deployment é ser mais simples de implementar na cultura da empresa e pode gerar datas de release específicas, com maior controle da visão do usuário final.

# Branch versus trunk-based approaches

Repositórios baseados em trunks são utilizados como uma "fonte" única, que é sincronizada diariamente para garantir que não há problemas em unir o código, enquanto repositórios baseados em branches são separadas por features. No trunk0based, cada commit durante o desenvolvimento exige uma série de testes de pre-submit, mas reaproveita builds de códigos que não foram alterados no espaço de tempo - realizando uma otimização - e evitando o uso de 'clean'. 

Porém, isso trunk-based exigem um supercomputador para realizar os builds e commits, o que torna o trunk custoso, mas avisa erros de integração o mais breve possível na hora de unir o código. Outro ponto negativo é na hora de submeter, é necessária a autorização dos "donos do código", gerando um processo mais burocrático e a dependência dessa autorização. Além disso, também existe o fato que serviços diferentes devem ter a mesma versão de um código como dependência, precisando de commits de update desses serviços.

# Heavily baked and lightly baked images

Heavy baked images não podem ser alteradas a partir do momento que a VM é criada, garantindo que a mesma versão é utilizada em testes e em produção - garantindo consistência e encapsulando packages instalados. Lightly baked images permitem certas alterações em runtime, onde pode custar muito tempo buildar e testar uma nova imagem para o sistema. Além disso, imagens geralmente são pesadas e podem ser difíceis de serem transferidas.
