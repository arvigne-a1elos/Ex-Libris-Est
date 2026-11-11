# ÍNDICE DE PROJETOS — A1ELOS

Painel de todos os projetos com governança ativa.
Atualizar sempre que um projeto novo for criado.

| Projeto | Fase | Pendências ativas | P1 | Última atualização |
|---------|------|-------------------|----|--------------------|
| global-numerology | Final de configuração | 49 | 5 | 09/11/2026 |
| exlibrisest | Em Construção | 10 | 11 | 2026 |

## Projetos registrados

### global-numerology
Site de numerologia, 24 produtos × 14 idiomas.
Repositório de código: arvigne-a1elos/global-numerology
Governança: pasta docs/ dentro do próprio repositório de código.
Status: em fase final de configuração.

### exlibrisest — Ex-Libris Est

**O que é:**
Repositório de periódicos para consulta online e venda de livros e
revistas, com espaço para cursos certificados. Cada cliente tem o seu,
com o seu próprio estilo.

**Por que Ex-Libris Est e não apenas Ex-Libris:**
Já existe uma empresa Ex-Libris na web, e 'Ex-Libris' é termo genérico
de biblioteconomia. O complemento 'Est' cria identidade própria,
evita conflito de endereço e dá margem para registro de marca.

**Os três produtos:**
1. Acervo próprio — vitrine, assinaturas, vendas, impressão sob demanda.
2. Plataforma de cursos — cursos com certificado vinculados ao acervo.
3. Modelo licenciado — o sistema inteiro, personalizado, com o estilo
   de cada cliente.

**Modelo de receita — duas cobranças:**
1. Criação personalizada + licença — MESMA cobrança única e fixa.
   Cobre a adaptação do produto pronto ao cliente (produtos dele,
   especificações dele, identidade dele) mais o direito de uso do
   sistema. Inclui 3 rodadas de ajuste.
2. Manutenção — mensal, valor fixo, muito inferior ao que as
   plataformas cobram por livro vendido. Cobre atualizações,
   correções, suporte técnico e hospedagem.

Princípio registrado: nada é criado antes da cobrança. Criar algo sob
medida e cobrar depois é assumir todo o risco do trabalho. A cobrança
prévia protege o trabalho, filtra o cliente e valida o escopo.

**Tese de negócio — desintermediação editorial:**
O projeto não é uma livraria. É um modelo que elimina os atravessadores
entre o autor e o leitor. Nas plataformas atuais (Amazon, Hotmart,
Mercado Livre e similares), a plataforma retém de 10% a 70% do valor,
é dona da vitrine e é dona do cliente — e o custo cresce com o volume
de vendas. No Ex-Libris Est, o autor é dono da vitrine, do cliente e da
margem, e paga o mesmo independentemente de vender 10 ou 10.000.

**Fluxo de receita do cliente (além do licenciamento):**
- Assinatura mensal contínua para consulta do acervo
- Liberação de acervo em cursos exclusivos
- Assinaturas de revistas (periódicos)
- Impressão sob demanda via editora parceira, com envio de versões
  físicas pelo correio

**Objetivo declarado:**
Reduzir o custo das obras para atingir mais pessoas em diversos idiomas,
tornando cursos mais acessíveis e ampliando o acesso.

**Capacidades técnicas necessárias:**
1. Assinatura recorrente (Stripe mode='subscription', não 'payment')
2. Controle de acesso (quem pode ler o quê, por quanto tempo)
3. Leitor protegido (sem download livre do acervo)
4. Multi-tenant (cada cliente com seu acervo, assinantes e receita,
   isolados entre si) — obrigatório para vender o modelo
5. Progresso do aluno (onde parou, o que completou)
6. Emissão de certificado com código único de validação
7. Validação pública do certificado (URL que qualquer pessoa consulta)
8. Tema personalizável por tenant (logo, cores, tipografia, layout)

**Decisão de 09/11/2026:**
O esqueleto nasce apenas com entrega efêmera. O Ex-Libris adapta a
entrega persistente, a multi-tenancy e os temas personalizados quando
começar.
Recomendação registrada: incluir um campo tenant_id desde já (com um
único tenant por padrão) acompanhado de um config_tema por tenant.
Custa pouco agora e evita refazer depois.

Repositório de código: arvigne-a1elos/exlibrisest (a criar)
Governança: pasta docs/ dentro do próprio repositório de código.
Status: aguardando o encerramento do global-numerology.

## Como adicionar um projeto

1. Copie a pasta _MODELO para uma pasta com o nome do projeto.
2. Preencha os três arquivos .md.
3. Adicione uma linha na tabela acima e uma seção em 'Projetos registrados'.
4. Commit.

## Repositórios de código

O código de cada projeto fica em seu próprio repositório.
Este repositório guarda apenas a governança (estado, decisões, retomada).

## Nomenclatura

Autor: arvigne (a assinatura)
Empresa: a1elos (a casa)
Projeto: o nome do produto (global-numerology, exlibrisest, ...)

Repositórios: arvigne-a1elos/<nome-do-projeto>
