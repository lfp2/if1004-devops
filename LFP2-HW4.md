# Continuous delivery and continuous deployment

Continuous delivery são práticas que garantem que o código está pronto para entrega, mas o deployment ainda é feito manualmente - ao contrário do continuous deployment. Uma das implicações técnicas necessárias para o continuous deployment é a capacidade de rollbacks e feature toggles - garantindo a existência de desativar features cujo o comportamento é inesperado. Apesar de no continous delivery a submissão da feature para produção não estar sendo feita, o código deve estar pronto para isto - passando por testes de QA, UAT, Smoke e nonfunctional. Mesmo com todos esses testes, não é garantido a experiência da feature em produção - causando possíveis acidentes. 
É necessária uma boa estratégia com logging, para poder gerar tracebility - a capacidade de saber a origem dos erros - durante incidentes, é necessário principalmente no continous delivery. Uma das vantagens dessa abordagem é a proximidade com o usuário final e rápida detecção de erros. A vantagem do continous deployment é ser mais simples de implementar na cultura da empresa e pode gerar datas de release específicas, com maior controle da visão do usuário final.

# Branch versus trunk-based approaches

