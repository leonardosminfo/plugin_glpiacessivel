## 0.2-beta

- consolida a primeira beta publica para GitHub, preservando compatibilidade declarada com GLPI 10 e 11;
- sincroniza metadados, URL de download, catalogos gettext e documentacao da release;
- corrige o namespace dos auxiliares SQL de instalacao e desinstalacao;
- adiciona politica de seguranca, guia de contribuicao, avisos de terceiros e licenca GPL integral;
- endurece a higiene do repositorio e a verificacao automatica do pacote;
- amplia o CI para PHPUnit, PHPStan, PHPCS, Composer Audit e validacao de i18n;
- documenta axe-core 4.10.3, MPL-2.0, fonte correspondente, hash e avisos transitivos;
- adota DCO 1.1 e sign-off para a procedencia de contribuicoes;
- explicita politica de licenciamento, marcas e checklist de propriedade intelectual;
- faz o gate de release validar documentos juridicos e o hash do axe-core.
- publica o pacote principal no perfil enxuto, sem binarios de voz com redistribuicao pendente;
- documenta explicitamente limites de homologacao assistiva, formularios dinamicos e traducao en-GB.
## 0.1.112-beta

- adiciona liberacao gradual por funcionalidade com estados disponivel, oculto e indisponivel;
- mantem ACL, perfil, entidade e permissoes nativas do GLPI como autoridade final;
- bloqueia rotas GET/POST e intents do chatbot para modulos indisponiveis, inclusive conversas ja iniciadas;
- inclui presets administrativos para apresentacao, demonstracao, piloto Self-Service e piloto tecnico;
- ajusta menus, cards, ajuda, atalhos e botao flutuante conforme a configuracao efetiva;
- preserva configuracoes legadas de Formularios e Chatbot durante atualizacao;
- adiciona auditoria, diagnostico, traducoes e regressao automatizada para a politica de modulos.

## 0.1.111-beta

- permite definir o nome publico do chatbot nas configuracoes gerais, mantendo Assistente como padrao;
- propaga o nome para interface, respostas, voz, ARIA e curadoria de roteiros com escape contextual;
- normaliza HTML, controles, marcadores bidirecionais, espacos e comprimento antes de persistir;
- corrige os rotulos ARIA da leitura automatica e internacionaliza as frases com placeholders;
- adiciona migracao idempotente, auditoria sem registrar o nome e testes unitarios de seguranca e fallback.
## 0.1.110-beta

- corrige o fundo preto herdado pelos textos dentro da resposta amarela da Assistente no alto contraste;
- torna transparentes os fundos internos da bolha, preservando texto preto sobre amarelo e o selo independente;
- valida a cascata completa nos modos normal e alto contraste.

## 0.1.109-beta

- corrige o contraste das respostas da Assistente no tema normal e noturno;
- substitui o gradiente por fundo solido `#005a9c` com texto branco, atingindo aproximadamente 7,14:1;
- isola a regra de cor da bolha para impedir sobrescrita pelas regras globais, preservando o selo e o alto contraste.

## 0.1.108-beta

- fecha a equivalencia da Search API no GLPI 11 para mine, busca textual, group_id, grupo unico e multiplos grupos com criterios OR aninhados;
- preserva o fallback seguro quando a Search API nao representa o filtro ou retorna resultado vazio inconclusivo;
- valida entidade ativa concreta e aplica recursividade somente quando o contexto nativo autoriza;
- pagina todo o Service Catalog GLPI 11 e respeita ServiceCatalog::canView() na exibicao do menu;
- correlaciona anexos da criacao, acompanhamento e tarefa com o item recem-criado, nome original e vinculo final Document_Item;
- amplia a auditoria local para resultados que exigem revisao manual e a automacao Pa11y/Axe para WCAG 2.2 A/AA;
- melhora reflow dos botoes flutuantes e respeita prefers-reduced-motion nos controles de voz.
## 0.1.107-beta

- publica o Axe local em uma rota web compativel com GLPI 11 e permite nova tentativa apos falha de carregamento;
- corrige a negacao de acesso a configuracao com HTTP 403 e pagina acessivel, sem excecao bruta;
- usa os rotulos nativos e traduzidos de status do GLPI, incluindo o status de aprovacao do GLPI 11;
- corrige os erros formais bloqueantes do PHPCS e adiciona testes de regressao.
## 0.1.106-beta

- adiciona a opcao geral `Mascarar contatos pessoais`, desativada por padrao;
- preserva a exibicao dos contatos conforme ACL nativa do chamado quando a opcao esta desativada;
- mantem mascaramento, revelacao temporaria, justificativa e auditoria quando a opcao esta ativada;
- registra a configuracao nos diagnosticos e na auditoria administrativa;
- amplia a regressao para validar os estados visivel e mascarado.
## 0.1.105-beta

- reforca isolamento por entidade e ACL nativa em tickets, templates ITIL, auditoria e roteiros;
- elimina a descoberta recursiva de fonte de login por HTTP e usa o seletor nativo do GLPI em memoria;
- valida novamente templates, artigos KB e permissoes imediatamente antes de operacoes sensiveis;
- protege uploads temporarios com ownership, descarte automatico e commit somente apos sucesso nativo;
- mascara dados pessoais por padrao e adiciona revelacao temporaria, justificada e auditada;
- torna aprovacao/rejeicao de roteiros resistente a replay e concorrencia;
- reduz o fallback de listagem para 500 chamados e comunica resultados parciais sem expor diagnosticos tecnicos a usuarios comuns;
- adiciona testes de regressao para fronteiras de entidade, template, login, upload e dados pessoais.

## 0.1.104-beta

- Corrige ACL de roteamento e mudanca de status por chamado, respeitando Ticket::canAssign() e a matriz nativa de transicoes.
- Bloqueia bypass de roteamento por UPDATE generico e remove aprovacao implicita quando o requisitante nao esta identificado.

## 0.1.102-beta

- implementa os contratos P1 de fallback Search API, com grupo atribuido alinhado ao GLPI e sinalizacao explicita de resultados parciais no limite de 5.000 chamados;
- endurece a confirmacao de anexos com `Document`/`Document_Item` e informa sucesso parcial sem permitir reenvio duplicado;
- melhora a submissao delegada de formularios GLPI 11/Formcreator, tratando redirecionamentos nativos e respostas inesperadas;
- normaliza erros de formulario e torna o resumo de validacao navegavel por teclado e leitor de tela;
- documenta o escopo homologado e os limites beta da paridade de formularios.
## 0.1.101-beta

- normaliza perfil, entidade e grupos pelo contexto nativo antes das telas autenticadas;
- preserva ACL e fallback nativo ao detectar contexto operacional incompleto.
## 0.1.100-beta

- corrige o retorno de foco quando condicoes dinamicas ocultam o campo ativo;
- adiciona reflow assistivo para controles de voz, formularios e iframe nativo;
- adiciona suporte visual a forced-colors para foco e bordas;
- mantem a validacao e a submissao sob o motor nativo homologado.
- detecta iframe nativo sem formulario e oferece foco no link de pagina completa;
- bloqueia temporariamente o envio convertido quando o motor de condicoes falha.
## 0.1.99-beta

- refina o alto contraste dos cards de sugestao do chatbot;
- mantem fundo preto no estado normal, hover e foco;
- usa titulo amarelo, descricao branca e anel de foco branco;
- evita que o foco pareca um estado selecionado permanente.
## 0.1.98-beta

- corrige o contraste dos atalhos do chatbot no alto contraste;
- remove a cascata preto sobre preto dos textos secundarios `small`;
- garante foco visivel com contorno branco e faixa preta de separacao;
- sincroniza o CSS publico durante a geracao do pacote.
## 0.1.97-beta

- adiciona contrato centralizado de capacidades para separar renderizacao acessivel, delegacao nativa e submissao propria;
- adiciona gate de submissao que bloqueia qualquer tentativa propria sem homologacao explicita de ACL, condicoes, destinos, validacoes e anexos;
- expõe diagnostico estruturado de fallback nativo para Service Catalog GLPI 11 e Formcreator GLPI 10;
- corrige a limpeza de `aria-describedby` para remover referencias de erros antigos apos nova validacao;
- amplia a regressao automatizada para 68 testes e 370 assercoes.
## 0.1.96-beta

- Normaliza erros de validacao no servidor e no renderer para `{field, code, message}`, sem depender de busca por substring.
- Atualiza o renderer convertido para consumir mapas nativos de obrigatoriedade e bloqueio, mantendo `required`, `aria-required` e `disabled` sincronizados antes da validacao.
- Endurece a verificacao de anexos de tickets: conta documentos distintos e confirma sua existencia antes de considerar o vinculo `Document_Item` completo.
- Mantem campos nativos de usuario, grupo, dispositivo, ativo, LDAP e tag no fallback ate homologacao real de seletores e ACL por perfil/entidade.
- Formaliza o limite beta de 5.000 chamados e a necessidade de comparacao por IDs reais para `mine`, `group` e `group_id`.
## 0.1.95-beta

- Elimina os 89 achados do PHPStan com stubs de desenvolvimento para a API global do GLPI/Formcreator, sem incluir esses stubs no pacote.
- Corrige o prefixo duplicado do autoloader e documenta a excecao legitima dos doubles globais no PHPCS.
- Remove 821 violacoes mecanicas do PHPCS; permanecem avisos historicos de linhas longas para saneamento incremental.
- Mantem a regressao verde: 62 testes e 360 assercoes.

- Endurece Search API para grupos multiplos e papeis ITIL quando os Search Options reais estao disponiveis.
- Mantem fallback textual quando titulo e conteudo nao podem ser representados nativamente.
- Bloqueia conversao propria diante de condicoes nativas nao normalizadas.
- Confirma um vinculo Document_Item por anexo enviado e formaliza o limite beta de 5.000 chamados.
- Corrige o contrato de excecoes de validacao e a descoberta de APIs do Formcreator.
- Torna explicito o contraste dos placeholders dos campos de pergunta e descricao nos modos claro, noturno e alto contraste.

# Changelog

## 0.1.92-beta

- Corrige os quatro achados de contraste identificados na auditoria Pa11y autenticada.
- Define cores explícitas para campos principais e avatar no tema claro, noturno e alto contraste.
## 0.1.91-beta

- Restringe mensagens tecnicas de fallback e identificacao do backend da listagem de chamados a administradores ou perfis com config/UPDATE.
- Mantem a listagem, os filtros e as validacoes de ACL disponiveis para usuarios comuns sem expor detalhes internos da Search API.
## 0.1.87-beta

- Adiciona auditoria local Axe, restrita a configuradores GLPI, sem telemetria ou persistencia.
- Adiciona ferramentas Pa11y com captura manual de sessao local para homologacao autenticada.
- Inclui assets locais Axe, documentacao e exclusoes de sessao no Git.

## 0.1.86-beta

- Migra os namespaces de runtime para `GlpiPlugin\\Glpiacessivel`.
- Padroniza metadados, XML de catalogo e pacote Marketplace/offline.
- Adiciona pipeline de qualidade, compilacao gettext e checksum de release.
- Mantem Search API e formularios sob gates de equivalencia e homologacao real.

## 0.1.85-beta

- Suporta multiplos targets de ticket delegados ao Formcreator 2.13.11.