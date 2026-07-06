# Product

## Register

brand

## Users

Simracers e entusiastas de automobilismo virtual (eSport SimRacing) buscando hardware de simulação — volantes, câmbios, aros e bases (ex: kit F4R). Chegam ao site para conhecer a marca ITS3, ver o portfólio de projetos/produtos e entrar em contato ou comprar. Também é o cartão de visitas da marca para parceiros e patrocinados (ex: pilotos de Porsche Cup / Stock Car que usam a libré ITS3).

## Product Purpose

Site institucional/portfólio da ITS3 ("Inovação Tecnológica em Simulação"), uma empresa brasileira especializada em hardware de simulação para games (volantes, aros, bases, cockpits). O site existe para apresentar a marca, mostrar os projetos/produtos desenvolvidos, e converter visitantes em contato/cliente. Sucesso = visitante entende rápido o que a ITS3 faz, sente a identidade motorsport/eSport da marca, e consegue navegar até o portfólio ou o contato sem fricção.

## Brand Personality

eSport SimRacing: técnico, agressivo, motorsport. Preto como base, vermelho como acento primário (extraído do badge do "3" no logo real do Instagram @its3.br), laranja/coral como acento raro secundário (confete do logo). Tipografia técnica (Titillium Web para corpo, Raleway bold para headings) em vez de fontes SaaS genéricas. Tom sério de hardware de precisão, não "startup fofa" — hashtag real da marca `#JuntosSomosMaisFortes` usada como elemento de identidade.

## Anti-references

Não deve parecer um template SaaS genérico claro: nada de fundo branco, botões pill laranja suave, cara de "landing page de agência" Bootstrap. A versão anterior do site (fundo branco + laranja `#c35302` + Open Sans + cards com sombra azulada suave) é exatamente o que estamos evitando — não fiel à marca real.

## Design Principles

1. **Fidelidade à marca real**: cores, tom e vocabulário visual vêm do Instagram real da ITS3 (@its3.br), não de convenções genéricas de template.
2. **Motorsport, não corporativo**: ângulos, contraste alto, tipografia técnica e acentos vermelhos — a estética de HUD/liga de corrida, não de dashboard SaaS.
3. **Acessibilidade não é opcional**: contraste AA, hierarquia de headings correta, mesmo dentro de um tema escuro de alto contraste.
4. **Um acento de cada vez**: vermelho carrega a maior parte do destaque; laranja é usado com moderação, como o confete do logo — nunca os dois competindo no mesmo elemento.
5. **Site estático, sem complexidade desnecessária**: continua HTML/CSS/JS vanilla (Bootstrap + jQuery legado); melhorias de design não devem introduzir build step ou dependências novas.

## Accessibility & Inclusion

WCAG AA: contraste de texto ≥4.5:1 (≥3:1 para texto grande), hierarquia de headings sem saltos, foco visível em elementos interativos, sem depender só de cor para transmitir estado. Já auditado e corrigido nesta sessão com o Impeccable CLI (contraste, `line-height`, padding, `overflow` cortando conteúdo, comprimento de linha).
