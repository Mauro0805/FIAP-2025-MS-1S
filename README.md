# FIAP-2025-MS-1S

## Linter:  
- É uma ferramenta de **análise de código** estática que verifica automaticamente o código-fonte.  
- Em **busca de erros** de programação, bugs, vulnerabilidades, problemas de estilo e outras construções suspeitas, melhorando a qualidade e a legibilidade do software.  
- Ao analisar a estrutura do código com base em um **conjunto de regras** predefinidas, o linter fornece feedback para os desenvolvedores.  
- Ajudando a resolver problemas no início do processo de desenvolvimento e promovendo um estilo de codificação consistente e fácil de manter.  

## Husky  
- Git hooks  
- Pré Commits  
- Pré Push  
### Requisitos  
- Git instalado  
- Node.js ≥ 18 (Husky é um pacote npm)  
- Wrapper do Maven (mvnw) ou do Gradle (gradlew) no repositório  
### Instalação  
**iniciar package.json (se ainda não existir)**  
`npm init –y`  

**instalar husky**  
`npm i -D husky`  

**habilitar hooks (cria .husky/)**  
`npx husky init`

> Spring Initializr  
> POM XML [josercf/ProductController](https://gist.github.com/josercf/7c32016c026016231317a6233bbc5a28)

## Arquivos de validação do projeto
```
config/
  checkstyle/
    google_checks.xml
  pmd/
    ruleset.xml
```
## Husk
### Edite .husky/pre-commit
```
#!/usr/bin/env sh
. "$(dirname -- "$0")/_/husky.sh"

echo "▶ Pre-commit: formatando e checando código..."
# formata e valida formatação
./mvnw -q spotless:apply spotless:check || exit 1

# análise estática rápida
./mvnw -q -DskipTests checkstyle:check pmd:check || exit 1
```

