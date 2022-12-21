# Infra Github Actions

Actions reusáveis para projetos Aegro.

## Regras e Padrões
### Nomenclatura

O nome das actions é composto pelos seguintes componentes (entre [ ])

>[linguagem/framework_de_programação?]-[ação_separado_por_underscores]-[ambiente/ferramenta/tecnologia?]

* O símbolo '?' indica que o componente é opcional
* Utilize underscores quando há mais de uma palavra no mesmo componente

#### Exemplos:
* java-deploy-k8s
* java_gradle-unit_tests
* angular-deploy-s3
* kotlin-analyze-sonar
* report_deploy _(esse contém apenas a ação, pois não é específico para tecnologia e atua em diferentes ferramentas)_

### Tag

As tags no git funcionam como marcadores para commits específicos. São constantemente usadas para demarcar versões de software.

É extremamente importante a criação da tag da versão de produção, usamos as tags nesse projeto para garantir uma maior segurança.

Exemplo de como criar a tag:

```console
git checkout production
git pull     
git log -n 1 --pretty=format:"%h" | tail -n 1                 # mostra o ultimo commit
git tag -l                                                    # lista as tags atuais
git tag -a v1.1.0 -m "Aegro workflows - add k8s actions"      # criar a tag com um numero superior (semantic version)
git push origin production --tags                             # Enviar a tag     
```

## Contribuindo
Para contribuir, adicione seu workflow em /.github/workflows e abra uma PR para a branch _dev_, faça os testes nessa branch e quando estiver validado, passe o seu worflow para a branch _production_.
* Antes de incluir um novo workflow, avalie os existentes para se certificar de que não deveria melhorar um deles ao invés de incluir um novo.
* Tenha atenção ao alterar workflows existentes pois eles podem estar em uso por outros projetos.
