# FIAP-2025-MS-1S

## Linter:  
É uma ferramenta de **análise de código** estática que verifica automaticamente o código-fonte.  
Em **busca de erros** de programação, bugs, vulnerabilidades, problemas de estilo e outras construções suspeitas, melhorando a qualidade e a legibilidade do software.  
Ao analisar a estrutura do código com base em um **conjunto de regras** predefinidas, o linter fornece feedback para os desenvolvedores.  
Ajudando a resolver problemas no início do processo de desenvolvimento e promovendo um estilo de codificação consistente e fácil de manter.  

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
npm init –y  

**instalar husky**  
npm i -D husky  

**habilitar hooks (cria .husky/)**  
npx husky init  

