# Infra Github Actions

Actions reusáveis para projetos Aegro.

## Regras e Padrões
### Nomenclatura

O nome das actions é composto pelos seguintes componentes (entre [ ])

>[linguagem/framework?]\_[ação]_[ambiente/ferramenta/tecnologia?]

* O símbolo '?' indica que o componente é opcional
* Utilize hífens quando há mais de uma palavra no mesmo componente

#### Exemplos:
* java_deploy_k8s
* java_unit-tests
* angular_deploy_s3
* kotlin_analyze_sonar
* notify-deploy _(esse contém apenas a ação, pois não é específico para tecnologia e atua em em diferentes ferramentas)_

## Contribuindo
Para contribuir, adicione seu workflow em /.github/workflows e abra uma PR para a branch _dev_, faça os testes nessa branch e quando estiver validado, passe o seu worflow para a branch _production_.
* Antes de incluir um novo workflow, avalie os existentes para se certificar de que não deveria melhorar um deles ao invés de incluir um novo.
* Tenha atenção ao alterar workflows existentes pois eles podem estar em uso por outros projetos.
