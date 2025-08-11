# 📖 Explicação sobre o TsConfig

| Opção                                | O que faz                                                                            | Uso comum / Quando usar                                     |             |
| ------------------------------------ | ------------------------------------------------------------------------------------ | ----------------------------------------------------------- | ----------- |
| **allowJs**                          | Permite compilar arquivos `.js` junto com `.ts`                                      | Migração gradual de JS para TS                              |             |
| **allowSyntheticDefaultImports**     | Permite importar módulos CommonJS com sintaxe default                                | Integração com módulos que não exportam default             |             |
| **allowUmdGlobalAccess**             | Permite acessar variáveis globais em módulos UMD                                     | Raramente usado                                             |             |
| **baseUrl**                          | Base para resolver módulos não relativos                                             | Configurar aliases de importação                            |             |
| **composite**                        | Permite projetos compostos (monorepos)                                               | Projetos multi-pacote com dependência entre eles            |             |
| **declaration**                      | Gera arquivos `.d.ts` de declaração                                                  | Bibliotecas e pacotes que exportam tipos                    |             |
| **declarationMap**                   | Gera arquivos `.d.ts.map` para mapear declaração e fonte                             | Debug de bibliotecas                                        |             |
| **emitDeclarationOnly**              | Emite só arquivos `.d.ts`, sem JS                                                    | Apenas exportar tipos                                       |             |
| **downlevelIteration**               | Suporta iteração em targets antigos                                                  | Compatibilidade com ES5 para `for..of` e iteradores         |             |
| **esModuleInterop**                  | Garante interoperabilidade entre CommonJS e ES Modules                               | Importações mais naturais                                   |             |
| **exactOptionalPropertyTypes**       | Faz checagem rígida em propriedades opcionais                                        | Garantir que `foo?: string` seja diferente de \`foo: string | undefined\` |
| **experimentalDecorators**           | Habilita decorators (anotações, ex: Angular, NestJS)                                 | Usado em frameworks que usam decorators                     |             |
| **forceConsistentCasingInFileNames** | Evita erros com nomes de arquivos com diferença de maiúsculas/minúsculas             | Evitar bugs cross-OS                                        |             |
| **importHelpers**                    | Usa helpers externos para evitar duplicação                                          | Reduz tamanho do bundle                                     |             |
| **importsNotUsedAsValues**           | Controla remoção de imports que são só tipos                                         | Controle sobre imports que aparecem só em tipagem           |             |
| **inlineSourceMap**                  | Inclui sourcemaps dentro do JS gerado                                                | Debug mais fácil, mas arquivo maior                         |             |
| **inlineSources**                    | Inclui código fonte dentro do sourcemap                                              | Facilita debug                                              |             |
| **isolatedModules**                  | Verifica compatibilidade para transpilers que compilam arquivo a arquivo (ex: Babel) | Projetos com Babel                                          |             |
| **jsx**                              | Configura suporte JSX (`react`, `react-jsx`, etc)                                    | Projetos React ou similares                                 |             |
| **jsxFactory**                       | Define função JSX factory (`React.createElement` padrão)                             | Custom JSX (ex: Preact)                                     |             |
| **jsxFragmentFactory**               | Define componente fragmento JSX padrão                                               | Custom JSX                                                  |             |
| **lib**                              | Define libs padrão (ex: `["ES2020", "DOM"]`)                                         | Define APIs disponíveis no código                           |             |
| **locale**                           | Define idioma para mensagens de erro                                                 | Usar mensagens em PT, EN, etc                               |             |
| **mapRoot**                          | Diretório para sourcemaps                                                            | Controle avançado                                           |             |
| **maxNodeModuleJsDepth**             | Profundidade máxima para checar arquivos JS dentro de node_modules                   | Evita slowdowns                                             |             |
| **module**                           | Define sistema de módulos (CommonJS, ESNext, etc)                                    | Conforme ambiente de execução                               |             |
| **moduleDetection**                  | Controla detecção de módulo em arquivos JS                                           | Raramente alterado                                          |             |
| **moduleResolution**                 | Como o compilador resolve módulos (node, classic, node16)                            | Normalmente `node` ou `node16`/`nodeNext`                   |             |
| **newLine**                          | Define o caractere de quebra de linha (`crlf` ou `lf`)                               | Compatibilidade com sistemas diferentes                     |             |
| **noEmit**                           | Não gera arquivos JS, só checa                                                       | Usado quando compilação é feita por outra ferramenta        |             |
| **noEmitHelpers**                    | Não gera funções helper no JS                                                        | Usar com `importHelpers`                                    |             |
| **noEmitOnError**                    | Não gera JS se houver erro de compilação                                             | Evitar distribuir código com erro                           |             |
| **noErrorTruncation**                | Mostra mensagens de erro completas                                                   | Debug mais detalhado                                        |             |
| **noFallthroughCasesInSwitch**       | Erro em casos faltando no switch                                                     | Ajuda evitar bugs com switch                                |             |
| **noImplicitAny**                    | Erro quando uma variável recebe tipo `any` implícito                                 | Código mais seguro, recomendado sempre                      |             |
| **noImplicitReturns**                | Erro quando função não retorna valor em todos caminhos                               | Evita bugs silenciosos                                      |             |
| **noImplicitThis**                   | Erro quando `this` é do tipo `any`                                                   | Segurança na tipagem de `this`                              |             |
| **noStrictGenericChecks**            | Desativa checagem estrita em generics                                                | Raramente recomendado                                       |             |
| **noUnusedLocals**                   | Erro para variáveis locais não usadas                                                | Código mais limpo                                           |             |
| **noUnusedParameters**               | Erro para parâmetros não usados                                                      | Código mais limpo                                           |             |
| **outDir**                           | Diretório onde o JS compilado será salvo                                             | Geralmente `dist` ou `build`                                |             |
| **outFile**                          | Junta tudo em um único arquivo JS                                                    | Usado em projetos AMD/UMD antigos                           |             |
| **paths**                            | Define aliases para imports                                                          | Facilita imports e evita caminhos relativos longos          |             |
| **preserveConstEnums**               | Não remove enums constantes                                                          | Debug e interoperabilidade                                  |             |
| **preserveSymlinks**                 | Preserva links simbólicos na resolução de módulos                                    | Para projetos com links simbólicos                          |             |
| **preserveValueImports**             | Preserva imports só para tipos, mesmo que não usados                                 | Controle avançado                                           |             |
| **pretty**                           | Exibe erros coloridos e formatados                                                   | Facilita leitura no terminal                                |             |
| **reactNamespace**                   | Define namespace JSX                                                                 | Raramente usado                                             |             |
| **removeComments**                   | Remove comentários no JS gerado                                                      | Para produção                                               |             |
| **resolveJsonModule**                | Permite importar arquivos JSON                                                       | Muito usado para configs e dados estáticos                  |             |
| **rootDir**                          | Diretório raiz do código-fonte                                                       | Organização do projeto                                      |             |
| **rootDirs**                         | Vários diretórios raiz combinados                                                    | Monorepos e projetos complexos                              |             |
| **skipDefaultLibCheck**              | Ignora checagem da lib padrão do TS                                                  | Acelera compilação                                          |             |
| **skipLibCheck**                     | Ignora checagem de arquivos `.d.ts` externos                                         | Acelera build e evita erros em libs externas                |             |
| **sourceMap**                        | Gera arquivos `.map` para debug                                                      | Desenvolvimento                                             |             |
| **sourceRoot**                       | Define raiz para fontes nos sourcemaps                                               | Controle avançado                                           |             |
| **strict**                           | Ativa várias opções rígidas (mais abaixo)                                            | Recomendado sempre                                          |             |
| **strictBindCallApply**              | Checa corretamente tipos em funções bind/call/apply                                  | Segurança extra                                             |             |
| **strictFunctionTypes**              | Checagem mais rígida para tipos de funções                                           | Evita bugs sutis                                            |             |
| **strictNullChecks**                 | Tratamento rigoroso para `null` e `undefined`                                        | Muito recomendado para segurança                            |             |
| **strictPropertyInitialization**     | Checa inicialização de propriedades na classe                                        | Evita propriedades não inicializadas                        |             |
| **stripInternal**                    | Remove código marcado com `/** @internal */`                                         | Bibliotecas que querem esconder APIs internas               |             |
| **target**                           | Versão JS alvo (ES5, ES2015, ES2022, etc)                                            | Compatibilidade com ambiente de execução                    |             |
| **traceResolution**                  | Mostra detalhes da resolução de módulos                                              | Debug                                                       |             |
| **tsBuildInfoFile**                  | Arquivo para armazenar informações de build incremental                              | Builds incrementais                                         |             |
| **useDefineForClassFields**          | Usa semântica padrão de ECMAScript para campos de classe                             | Para compatibilidade com JS moderno                         |             |
| **watch**                            | Modo watch para recompilar automaticamente                                           | Desenvolvimento                                             |             |
