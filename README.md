Este relatório detalha a aula prática de Infraestrutura Ágil, que teve como objetivo simular e monitorar um processo de pipeline de entrega contínua (CI/CD) utilizando o sistema de controle de versões GIT e a ferramenta GitLab CI/CD.

A metodologia consistiu na configuração de um projeto de Loja Virtual, no qual um arquivo de orquestração (.gitlab-ci.yml) foi utilizado para definir estágios de build e notificação, fazendo uso do Docker Hub para gerenciamento de imagens.

O monitoramento da execução resultou nas seguintes conclusões essenciais:

Simulação de Falha: Uma falha inicial foi identificada e registrada no estágio pre-build do pipeline, causada por credenciais ou nomes de repositório incorretos (denied: requested access to the resource is denied) durante a tentativa de docker push para o Docker Hub.

Diagnóstico e Correção: O diagnóstico por meio da análise dos logs de execução permitiu a correção imediata, ajustando as variáveis de autenticação e o nome do repositório no comando docker push.

Simulação de Sucesso: Após a correção, o novo pipeline foi executado com sucesso (Status: Passed), demonstrando a capacidade do sistema de realizar a Integração Contínua completa, incluindo o build da imagem, tagging e envio (push) para o repositório externo.

Concluiu-se que o monitoramento em tempo real do pipeline é fundamental para a agilidade, permitindo o diagnóstico rápido de falhas e a manutenção da confiabilidade na entrega automática do software.
