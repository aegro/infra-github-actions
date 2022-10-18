# Infra Github Actions

Actions reusáveis para projetos Aegro.

## Regras e Padrões
### Nomenclatura

O nome das actions é composto pelos seguintes componentes (entre [ ])

>[linguagem/framework?]-[ação]-[ambiente/ferramenta/tecnologia?]

* O símbolo '?' indica que o componente é opcional
* Utilize underscores quando há mais de uma palavra no mesmo componente

#### Exemplos:
* java-deploy-k8s
* java_gradle-unit_tests
* angular-deploy-s3
* kotlin-analyze-sonar
* report_deploy _(esse contém apenas a ação, pois não é específico para tecnologia e atua em diferentes ferramentas)_

## Contribuindo
Para contribuir, adicione seu workflow em /.github/workflows e abra uma PR para a branch _dev_, faça os testes nessa branch e quando estiver validado, passe o seu worflow para a branch _production_.
* Antes de incluir um novo workflow, avalie os existentes para se certificar de que não deveria melhorar um deles ao invés de incluir um novo.
* Tenha atenção ao alterar workflows existentes pois eles podem estar em uso por outros projetos.
