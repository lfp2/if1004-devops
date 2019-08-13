# Learning Git
![alt text](https://drive.google.com/open?id=1W3LvwU3zn99hyPfaR6Kawog_o0YBcd4D "Learning Git progress")
# Hooks
```
chmod u+x .git/hooks/*
```

```
#!/bin/bash

xdg-open https://www.google.com/
```
#Screencast
[Link to screencast](https://drive.google.com/open?id=1arkhHs5RO2C4pAdV-oKFe-mEn10srLoD)
# Concepts
1. Continuous integration é o processo de integração de uma branch com a base existente, chegando a ser realizada várias vezes por dia. Continuous delivery é a entrega do código para um ambiente, mas diferente do Continuous Deployment - onde a entrega é feita para produção sem intervenção de humanos, essa entrega depende de uma autorização manual.
2. Enquanto DevOps team ainda possuem um time de operações, que estão bem alinhados entre si, times NoOps devem garantir a saúde do código do início ao fim - gerando desafios como a integração entre times autônomos. Isso acaba gerando uma responsabilidade maior por parte do desenvolvedor, com suas obrigações cada vez maiores.
3. Para garantir que uma feature seja interessante para o usuário, elas são tratadas como experimentos - sendo permitido que algo que já está em produção e não seja relevante seja excluída da plataforma. Em prática, isso acaba gerando novas métricas - ou seja mais dados para armazenar e podendo ser difícil de extrair informações relevantes.
4. Apesar de ser rápido para dar deploy, mudanças ficam ocultas dos usuários para verificar sua estabilidade da nova feature e poder testar sem afetar a experiência dos usuários, podendo ativar as novas funcionalidades através de flags nos meses seguintes.
