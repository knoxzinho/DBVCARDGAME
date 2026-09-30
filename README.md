# DESBRAVADORES: RPG CARD GAME

## Release Notes / Histórico Completo do Projeto

**Versão documentada:** V49 Beta\
**Documento:** histórico consolidado desde a V1\
**Status:** Beta / desenvolvimento contínuo

------------------------------------------------------------------------

# 1. Visão geral

**Desbravadores: RPG Card Game** é um card game de sobrevivência,
exploração, construção e gerenciamento de recursos inspirado no universo
dos Desbravadores.

A proposta evoluiu de um protótipo de cartas para um sistema híbrido de:

-   card game;
-   RPG de sobrevivência;
-   exploração;
-   crafting;
-   gerenciamento de inventário;
-   equipamentos;
-   construção de acampamento;
-   objetivos progressivos;
-   eventos ambientais;
-   clima;
-   ciclo de dia e noite;
-   gerenciamento de fome, sede e vida;
-   multiplayer local;
-   progressão de dificuldade;
-   descoberta de objetivos;
-   gerenciamento de peso;
-   cadeia de fabricação.

A referência de experiência de sobrevivência foi inspirada em conceitos
gerais de jogos como **Project Zomboid**, enquanto a apresentação das
cartas buscou referências visuais de card games como **Marvel Snap**,
sem copiar seus elementos proprietários.

O objetivo final da partida é construir um **Acampamento Completo**.

------------------------------------------------------------------------

# 2. Conceito original

A primeira ideia era um card game em que o jogador:

1.  recebe cartas;
2.  administra estrelas;
3.  coloca recursos no campo;
4.  combina cartas;
5.  completa objetivos;
6.  transforma recursos em estruturas;
7.  sobrevive a eventos climáticos;
8.  monta um acampamento.

O projeto posteriormente ganhou sistemas de RPG e sobrevivência, fazendo
com que as cartas passassem a representar não apenas recursos, mas
também:

-   equipamentos;
-   ferramentas;
-   consumíveis;
-   estruturas;
-   objetivos;
-   modificadores;
-   itens de crafting;
-   descobertas.

------------------------------------------------------------------------

# 3. Evolução visual

## V1 e primeiras versões

O protótipo começou com uma apresentação simples de card game, com foco
na funcionalidade.

As primeiras preocupações foram:

-   cartas;
-   custos em estrelas;
-   mão;
-   campo;
-   objetivos;
-   fusão;
-   modificadores.

## Evolução para 16-bit

Foi definida a direção artística:

> **Site moderno + cartas com identidade 16-bit.**

A interface do site não precisava ser completamente pixelada. O estilo
16-bit ficou concentrado principalmente nas cartas, ícones e elementos
de jogo.

## Layout das cartas

O projeto passou por várias experiências visuais.

Posteriormente foi escolhido como referência principal o modelo compacto
usado nas versões iniciais/V17, com:

-   custo no canto;
-   tipo;
-   arte;
-   nome;
-   descrição;
-   informação de uso;
-   controles.

Foram removidos posteriormente:

-   scanlines;
-   grades sobre as cartas;
-   riscos decorativos;
-   excesso de molduras;
-   elementos que causavam sobreposição.

## Verso das cartas

Foi adotado um verso oficial baseado na imagem fornecida durante o
desenvolvimento:

-   vermelho;
-   dourado;
-   escudo;
-   bússola;
-   espada;
-   elementos ornamentais.

Esse verso passou a ser usado em:

-   deck;
-   embaralhamento;
-   sorteio inicial;
-   reposição do deck;
-   animações de cartas.

------------------------------------------------------------------------

# 4. V1 a V10: fundação do jogo

As primeiras versões estabeleceram a estrutura fundamental.

Foram definidos:

-   deck;
-   mão;
-   campo;
-   estrelas;
-   ações;
-   objetivos;
-   materiais;
-   estruturas;
-   modificadores;
-   fusão.

## Regras iniciais

O jogador recebeu:

-   2 ações por rodada;
-   mão com limite inicial;
-   deck de cartas;
-   cartas com custo em estrelas;
-   campo limitado.

A estrutura inicial incluía cartas como:

-   Corda;
-   Lona;
-   Lenha;
-   Fósforos;
-   Balde;
-   Cantil.

E objetivos como:

-   Montar Barraca;
-   Acender Fogueira;
-   Coletar Água;
-   Montar Acampamento.

------------------------------------------------------------------------

# 5. V11 a V17: estabilização das cartas

Essa fase foi marcada por correções de interface e lógica.

Problemas encontrados:

-   cartas que não apareciam imediatamente;
-   animações acessando elementos inexistentes;
-   fusão quebrando a renderização;
-   botões desabilitados incorretamente;
-   cartas com custo insuficiente ainda clicáveis;
-   estado sendo atualizado somente ao terminar a rodada.

## V14

Foi corrigido um problema importante de animação causado por referência
incorreta ao campo.

## V15

Foram adicionados/corrigidos:

-   cartas visualmente desabilitadas quando o jogador não possui
    estrelas;
-   bloqueio de clique quando não há estrelas suficientes;
-   fusão gratuita.

## V16

Foi reorganizada a arquitetura:

> **alterar estado → renderizar → animar**

Isso permitiu que:

-   cartas jogadas aparecessem imediatamente;
-   o campo fosse atualizado sem esperar o final da rodada;
-   animações ocorressem depois da atualização do estado.

## V17

A V17 se tornou uma das principais referências visuais e estruturais.

Foram incorporados:

-   emergência de troca;
-   esforço físico;
-   venda;
-   desmontagem;
-   mochila;
-   luvas;
-   clima;
-   fundo de floresta;
-   eventos;
-   maior variedade de cartas.

------------------------------------------------------------------------

# 6. V18: economia de estrelas

Foi criada uma nova lógica de recompensa.

O sistema passou a considerar o **poder** daquilo que foi construído ou
combinado.

A ideia definida foi:

-   rodada gera estrela;
-   criação de item/objetivo pode gerar estrelas relacionadas ao poder;
-   fusionar também pode gerar recompensa;
-   colocar simplesmente uma carta no campo não deveria representar
    esforço físico.

Também foi reforçado que:

> colocar uma carta no campo não reduz fome/sede.

O esforço físico acontece em ações como:

-   criação;
-   combinação;
-   fusão;
-   conclusão de objetivos.

------------------------------------------------------------------------

# 7. V19 a V23: objetivos, eventos e descoberta

O sistema de objetivos evoluiu.

Foi criada a ideia de que objetivos concluídos deveriam deixar o espaço
do acampamento e aparecer em:

> **AMBIENTE / EVENTOS**

A intenção era liberar espaço para o campo físico.

Também surgiu o conceito de:

-   objetivo oculto;
-   mapa;
-   descoberta;
-   eventos;
-   clima persistente.

## Mapa

Sem Mapa:

-   objetivos completos permanecem ocultos;
-   o jogador pode ser avisado de uma nova descoberta;
-   alguns recursos necessários podem ser identificados.

Com Mapa:

-   objetivos ficam visíveis.

À noite:

-   Mapa + Lanterna permitem consultar os objetivos.

------------------------------------------------------------------------

# 8. V24 e V25: identidade visual e acesso

Foram feitas melhorias no tamanho das cartas.

Objetivos:

-   cartas menores;
-   melhor encaixe no campo;
-   botões dentro das cartas;
-   descrição sem sobreposição;
-   interface mais limpa.

A fonte enviada pelo usuário chegou a ser testada como fonte principal,
mas posteriormente foi removida por decisão visual.

Foi adotada uma tipografia mais agradável e limpa.

Também foram adicionados conceitos de:

-   login local demonstrativo;
-   tutorial;
-   manual PDF.

Posteriormente, os botões de Tutorial e Manual PDF foram removidos da
interface principal para deixar o jogo mais limpo.

------------------------------------------------------------------------

# 9. V26 a V30: sobrevivência e crafting

A partir dessa fase, o jogo passou a incorporar uma camada mais profunda
de sobrevivência.

## Recursos por rodada

Foi criado um sistema de coleta.

O jogador pode acumular:

-   madeira;
-   fibras;
-   tecido;
-   metal;
-   água;
-   alimentos;
-   combustível;
-   recursos medicinais.

Esses recursos são usados para fabricar cartas.

Exemplo:

> 2 Fibras → Corda

------------------------------------------------------------------------

# 10. Modo Aventura

O Modo Aventura foi criado para ensinar o jogo.

O fluxo pensado:

1.  escolher modo;
2.  tutorial;
3.  escolher primeiro objetivo;
4.  embaralhar;
5.  receber cartas;
6.  iniciar expedição.

O tutorial apresenta progressivamente:

-   coleta;
-   crafting;
-   construção;
-   sobrevivência;
-   desmontagem;
-   objetivos.

Posteriormente, o texto "MODO AVENTURA" foi removido de determinadas
áreas do HUD para melhorar a organização visual, mas o conceito de modo
continua fazendo parte do jogo.

------------------------------------------------------------------------

# 11. Modo Sobrevivência

Foi criado um segundo modo.

O Modo Sobrevivência utiliza escalonamento de dificuldade baseado na
experiência acumulada.

A ideia:

> quanto mais vezes o jogador repete a expedição, mais o jogo pode
> pressioná-lo.

Possíveis escaladas:

-   clima;
-   duração de eventos;
-   fome;
-   sede;
-   dano estrutural;
-   dificuldade de coleta;
-   economia;
-   margem de recuperação.

O objetivo é evitar que a repetição seja simplesmente uma cópia da mesma
partida.

------------------------------------------------------------------------

# 12. Dia e noite

Foi implementado um ciclo em tempo real.

A partida:

> **sempre começa de dia.**

Depois, o jogo alterna entre:

-   ☀️ Dia;
-   🌙 Noite.

A duração é aleatória.

O sistema não deve depender exclusivamente da rodada para mudar o
período.

## Efeitos

Durante o dia:

-   mesa mais clara;
-   fabricação mais barata;
-   maior visibilidade.

Durante a noite:

-   mesa mais escura;
-   fabricação mais cara;
-   necessidade de iluminação;
-   Mapa exige Lanterna para consulta.

------------------------------------------------------------------------

# 13. Clima e modificadores

Foram definidos eventos ambientais como:

-   Sol;
-   Chuva;
-   Tempestade;
-   Drought/Sol Intenso em versões anteriores.

Cada modificador pode alterar a experiência.

## Visual

Sol:

-   efeito de luz.

Chuva:

-   partículas de chuva.

Tempestade:

-   chuva intensa;
-   relâmpagos;
-   flashes.

## Gameplay

O clima pode:

-   danificar estruturas;
-   aumentar necessidades;
-   alterar custos;
-   alterar duração de eventos.

No multiplayer local, a regra definida foi:

> **o modificador de um jogador pode afetar o adversário.**

------------------------------------------------------------------------

# 14. Vida, fome e sede

Foram definidos três atributos principais:

-   🍖 Fome;
-   💧 Sede;
-   ❤️ Vida.

## Fome e sede

Esforço físico pode reduzir necessidades.

Se o jogador passa períodos sem esforço físico, fome e sede também podem
cair.

O jogo deve oferecer recuperação através de:

-   alimentos;
-   água;
-   refeições;
-   itens médicos;
-   descanso;
-   mecanismos de emergência.

------------------------------------------------------------------------

# 15. Cantil e hidratação

O Cantil evoluiu para um sistema próprio.

Quando equipado:

> **100% de água**

é sua capacidade máxima.

Se a sede diminuir:

-   o Cantil pode consumir automaticamente água;
-   o consumo é proporcional à perda de sede.

Exemplo:

> Sede perde 8%

→ Cantil perde aproximadamente 8%.

Quando o Cantil chega a:

> 0%

a sede volta a diminuir normalmente.

## Abastecimento

Chuva pode abastecer o Cantil com probabilidade aleatória.

Se houver:

> **Reserva de Água construída**

o Cantil pode ser abastecido automaticamente.

------------------------------------------------------------------------

# 16. Água limpa

A água coletada não é automaticamente água limpa.

A sequência passou a ser:

``` text
Coletar água
    ↓
Reserva de Água
    ↓
Fogueira
    ↓
Ferver
    ↓
Água limpa
    ↓
Cantil
```

Isso adiciona uma cadeia de sobrevivência realista ao jogo.

------------------------------------------------------------------------

# 17. Fogueira e cozinha

A Fogueira passou a habilitar a cozinha.

Alimentos que exigem preparo não podem ser consumidos diretamente.

Exemplo:

``` text
Alimento cru
    +
Fogueira
    +
combustível
    ↓
Refeição preparada
```

Foram planejadas receitas como:

-   Carne Assada;
-   Refeição de Trilha;
-   Bebida de Reidratação.

------------------------------------------------------------------------

# 18. Perecíveis

Foi introduzido um sistema de deterioração.

Alimentos não preparados podem estragar com o tempo quando estão:

-   na mesa;
-   no inventário;
-   na mochila.

A mão possui uma exceção definida:

> itens na mão podem ser vendidos ou trocados antes de serem
> armazenados.

A intenção é criar uma decisão:

> armazenar ou utilizar/vender rapidamente?

------------------------------------------------------------------------

# 19. Inventário

Foi criado um inventário separado da mão.

## Mão

A mão representa cartas disponíveis para ações imediatas.

Limite inicial:

> 5 cartas.

## Inventário

O inventário representa itens armazenados.

Limite inicial:

> 5 espaços.

Também existe limite de:

> 10 de peso.

O peso é inspirado em sistemas de inventário de RPG de sobrevivência.

------------------------------------------------------------------------

# 20. Mochila e upgrades

A capacidade pode ser aumentada.

Exemplo definido:

### Sem mochila

-   5 espaços;
-   10 peso.

### Mochila

-   9 espaços;
-   18 peso.

### Mochila Reforçada

-   11 espaços;
-   22 peso.

Luvas podem aumentar a capacidade da mão.

------------------------------------------------------------------------

# 21. Equipamentos

Foi criada uma silhueta de personagem.

Slots:

-   Cabeça;
-   Costas;
-   Tronco;
-   Mãos;
-   Cintura;
-   Acessório;
-   Arma;
-   Pernas;
-   Pés.

A intenção é que o equipamento apareça visualmente sobre o personagem.

Exemplos:

-   Luva → Mãos;
-   Mochila → Costas;
-   Capa → Tronco;
-   Lanterna → Mãos;
-   Cantil → Cintura;
-   Bússola → Acessório;
-   Botas → Pés;
-   Boné → Cabeça.

------------------------------------------------------------------------

# 22. Equipamento afeta gameplay

Equipamentos não são apenas cosméticos.

Eles alteram atributos do jogador.

Exemplos:

**Luvas** - aumentam mão.

**Mochila** - aumenta capacidade de inventário.

**Cantil** - fornece água automática.

A arquitetura foi preparada para futuramente permitir:

-   botas reduzindo custos de deslocamento;
-   capa protegendo contra chuva;
-   ferramentas acelerando construção;
-   equipamentos reduzindo consumo;
-   vestuário aumentando resistência.

------------------------------------------------------------------------

# 23. Crafting

O sistema de Craft passou por várias reformulações.

A versão atual trabalha com uma progressão:

### Tier 1

Básicos.

### Tier 2

Intermediários.

### Tier 3

Avançados/reforçados.

### Tier 4

Especializados.

------------------------------------------------------------------------

# 24. Cadeias de crafting

Exemplos:

``` text
Fibras
 ↓
Corda
 ↓
Corda Reforçada
```

``` text
Tecido
 ↓
Lona
 ↓
Mochila
 ↓
Mochila Reforçada
```

``` text
Papel + Caneta
 ↓
Mapa
```

``` text
Caderno + Papel
 ↓
Livro de Objetivos
```

``` text
Madeira + Metal
 ↓
Ferramentas
 ↓
Construções
```

------------------------------------------------------------------------

# 25. Ferramentas de construção

Foram adicionados ou planejados:

-   🔨 Martelo;
-   🪓 Machadinha;
-   🪚 Serrote;
-   📌 Pregos;
-   🔩 Parafusos;
-   🧵 Arame;
-   🧰 Kit de Construção.

A intenção é fazer ferramentas funcionarem como componentes reais da
progressão.

------------------------------------------------------------------------

# 26. Construções

As principais construções são:

-   Barraca;
-   Fogueira;
-   Reserva de Água;
-   Abrigo Reforçado;
-   Acampamento Completo.

Construções possuem:

-   resistência;
-   durabilidade;
-   efeitos;
-   ações próprias;
-   interação com clima;
-   reparo;
-   desmontagem;
-   evolução.

------------------------------------------------------------------------

# 27. Mudança estrutural V48

Uma das mudanças arquiteturais mais importantes:

## Construções NÃO ficam mais em "SEU ACAMPAMENTO".

Toda construção criada vai para:

> **AMBIENTE / EVENTOS**

Exemplo:

``` text
Mão
 ↓
Construir Barraca
 ↓
AMBIENTE / EVENTOS
```

O mesmo vale para:

-   Fogueira;
-   Reserva de Água;
-   Abrigo;
-   outras estruturas futuras.

Isso separa claramente:

### SEU ACAMPAMENTO

Itens/equipamentos que o jogador administra.

### AMBIENTE / EVENTOS

Estruturas persistentes construídas durante a expedição.

------------------------------------------------------------------------

# 28. Durabilidade das estruturas

Construções possuem resistência.

Exemplo:

> Barraca 4/5

> Fogueira 3/4

> Abrigo Reforçado 8/8

A barra visual acompanha o valor.

## Clima

Chuva/tempestade podem reduzir resistência.

Quando chega a:

> 0

a construção pode ser destruída.

------------------------------------------------------------------------

# 29. Evolução da Barraca

Uma Barraca pode ser transformada em Abrigo Reforçado.

``` text
Barraca
 +
Estacas
 +
ferramentas necessárias
 ↓
Abrigo Reforçado
```

A Barraca original é substituída.

Não ficam duas estruturas ocupando espaço.

------------------------------------------------------------------------

# 30. Objetivo final

O objetivo final é:

> **Montar um Acampamento Completo.**

A estrutura principal exige componentes/estruturas como:

-   Barraca ou Abrigo Reforçado;
-   Fogueira;
-   Reserva de Água.

------------------------------------------------------------------------

# 31. Mapa

O Mapa passou a ser uma carta especial.

Ele pode ser:

-   encontrado;
-   fabricado;
-   comprado em determinadas condições.

Receita definida:

> Papel + Caneta → Mapa.

## Uso

Durante o dia:

> Mapa → revela objetivos.

Durante a noite:

> Mapa + Lanterna equipada → revela objetivos.

O Mapa é consumido/removido depois de utilizado conforme a regra
estabelecida.

------------------------------------------------------------------------

# 32. Livro de Objetivos

O Livro possui função diferente do Mapa.

### Mapa

Permite visualizar.

### Livro

Permite cumprir.

Quando descoberto:

-   fica marcado como descoberto;
-   não volta para as possibilidades de compra;
-   habilita a conclusão dos objetivos conforme as condições.

------------------------------------------------------------------------

# 33. Objetivos ocultos

Sem Mapa:

-   objetivos completos não são exibidos;
-   o jogador recebe notificações de descoberta;
-   alguns recursos necessários podem ser indicados.

Com Mapa:

-   objetivos são revelados.

Isso cria uma camada de exploração e descoberta.

------------------------------------------------------------------------

# 34. Deck e sorteio

O deck principal foi definido como:

> **30 cartas**

O jogador começa com:

> **5 cartas na mão**

Antes do sorteio inicial:

1.  tutorial/fluxo inicial;
2.  escolha da primeira missão;
3.  botão de embaralhar;
4.  animação;
5.  sorteio de 5 cartas.

A animação inicial foi definida com duração de:

> 5 segundos.

------------------------------------------------------------------------

# 35. Reabastecimento do deck

Quando o deck esgota:

-   jogador pode comprar novos lotes;
-   compra em múltiplos de 5;
-   custo definido como ⭐2 por cada 5 cartas;
-   quantidade escolhida em janela;
-   a compra consome os movimentos da rodada;
-   animação especial de 7 segundos;
-   limite total de 100 cartas adicionais por partida.

Texto definido para a animação:

> "Comprando novas cartas para continuar sua expedição"

------------------------------------------------------------------------

# 36. Mapa e Livro no deck

Depois de descobertos:

-   não podem voltar ao deck;
-   não aparecem em novas compras;
-   não podem ser sorteados novamente.

Isso evita cartas únicas duplicadas.

------------------------------------------------------------------------

# 37. Estrelas

As estrelas funcionam como recurso econômico.

Foram definidos usos para:

-   craft;
-   compra de cartas;
-   compra de mapa;
-   ações especiais;
-   reparos;
-   outras ações.

A economia foi sendo ajustada ao longo das versões para evitar acúmulo
excessivo.

A ideia mais recente é:

> recompensa por poder + ganho de rodada + custos reais de
> fabricação/ação.

------------------------------------------------------------------------

# 38. Ações

O jogador possui:

> **2 ações por rodada**

O HUD utiliza um ícone de pés para representar ações.

Ações podem ser usadas para:

-   comprar;
-   craftar;
-   construir;
-   equipar;
-   reparar;
-   desmontar;
-   vender;
-   trocar;
-   cozinhar;
-   ferver;
-   cumprir objetivos.

------------------------------------------------------------------------

# 39. Compra de cartas

A primeira compra pode ser gratuita conforme a economia definida nas
versões anteriores.

Compras adicionais podem:

-   custar estrela;
-   consumir ação;
-   respeitar limite da mão.

O sistema deve impedir compra quando a mão estiver cheia.

------------------------------------------------------------------------

# 40. Fusão

Duas cartas iguais podem ser combinadas.

Regra:

``` text
Nível 1 + Nível 1 = Nível 2
Nível 2 + Nível 2 = Nível 3
```

O poder é somado.

A fusão é gratuita em ações/estrelas conforme a regra estabelecida
anteriormente.

------------------------------------------------------------------------

# 41. Itens reforçados

Itens reforçados não devem aparecer simplesmente como cartas básicas
aleatórias.

Eles devem ser criados pela combinação de itens básicos.

Exemplos:

-   2 Cordas → Corda Reforçada;
-   2 Lonas → Lona Reforçada;
-   2 Lenhas → Lenha Seca;
-   2 Alimentos → Ração Completa;
-   2 Mochilas → Mochila Reforçada.

------------------------------------------------------------------------

# 42. Desmontagem

Construções podem ser desmontadas.

O sistema deve:

-   pedir confirmação;
-   consumir ação;
-   aplicar custo definido;
-   devolver parte dos materiais;
-   enviar materiais para mão/inventário conforme espaço.

Itens reforçados podem devolver componentes básicos.

------------------------------------------------------------------------

# 43. Venda e troca

Itens podem ser:

-   vendidos;
-   trocados;
-   convertidos em recursos de emergência.

Venda pode fornecer:

-   estrelas;
-   item aleatório.

Troca pode fornecer:

-   alimento;
-   água.

------------------------------------------------------------------------

# 44. Modificadores

O deck de modificadores inclui eventos ambientais.

Os modificadores podem afetar:

-   clima;
-   estruturas;
-   custos;
-   necessidades;
-   adversário no multiplayer.

No multiplayer local:

> modificador de um jogador afeta o jogador adversário.

------------------------------------------------------------------------

# 45. Multiplayer local

Foi planejado/implementado o modo multiplayer local.

Ao ativar:

> a tela é dividida.

Cada jogador possui:

-   mão;
-   campo;
-   recursos;
-   estrelas;
-   necessidades;
-   equipamentos;
-   objetivos.

Os modificadores podem afetar o adversário.

------------------------------------------------------------------------

# 46. Responsividade

O site foi progressivamente ajustado para:

-   computador;
-   tablet;
-   celular;
-   zoom do navegador.

Problemas recorrentes tratados:

-   botões sobrepostos;
-   texto cortado;
-   cartas ultrapassando áreas;
-   controles invadindo rodapé;
-   modais desalinhados;
-   cartas apertadas.

A quantidade de cartas por linha foi adaptada de acordo com a largura.

------------------------------------------------------------------------

# 47. Modal de carta

Clicar em uma carta abre uma visualização ampliada.

Mostra:

-   arte;
-   nome;
-   tipo;
-   custo;
-   descrição;
-   peso;
-   "serve para";
-   jogar;
-   recolher;
-   guardar.

**Recolher** retorna a carta para a mão.

**Guardar** envia para o inventário.

------------------------------------------------------------------------

# 48. Mão ≠ Inventário ≠ Equipamento ≠ Ambiente

A arquitetura conceitual atual é:

``` text
DECK
 ↓
MÃO
 ├── JOGAR
 │     ↓
 │   CAMPO / AÇÃO
 │
 ├── GUARDAR
 │     ↓
 │ INVENTÁRIO
 │
 └── EQUIPAR
       ↓
   PERSONAGEM
```

E:

``` text
CONSTRUIR
 ↓
AMBIENTE / EVENTOS
```

Essa separação é fundamental para o projeto atual.

------------------------------------------------------------------------

# 49. Oficina

A janela de Craft foi renomeada visualmente para:

> **OFICINA**

A interface permite:

-   selecionar receita;
-   escolher quantidade;
-   visualizar componentes;
-   visualizar custo;
-   criar diretamente.

O sistema precisa validar:

1.  recursos;
2.  componentes;
3.  ações;
4.  estrelas;
5.  espaço;
6.  peso;
7.  existência da receita;
8.  existência do item de saída.

------------------------------------------------------------------------

# 50. Correções de erros de Craft

Durante o desenvolvimento ocorreram erros como:

> `Cannot read properties of undefined (reading 'i')`

A causa estava relacionada a receitas tratando cartas como recursos ou
referenciando componentes inexistentes.

Foi estabelecida uma separação entre:

### Recursos

Exemplos:

-   madeira;
-   fibras;
-   tecido;
-   metal;
-   água;
-   combustível.

### Itens

Exemplos:

-   papel;
-   caneta;
-   corda;
-   lona;
-   mochila;
-   ferramentas.

Essa distinção deve ser mantida em todas as futuras receitas.

------------------------------------------------------------------------

# 51. Craft transacional

O Craft foi redesenhado para funcionar como uma operação segura.

Fluxo:

``` text
VALIDAR
 ↓
SE TUDO OK
 ↓
CONSUMIR
 ↓
CRIAR
 ↓
ATUALIZAR ESTADO
 ↓
RENDERIZAR
```

Se falhar:

``` text
NADA É CONSUMIDO
```

Isso evita perda de recursos causada por erro interno.

------------------------------------------------------------------------

# 52. Objetivos transacionais

O mesmo princípio foi aplicado aos objetivos.

Antes de consumir componentes:

-   todos os requisitos são verificados;
-   origem dos componentes é identificada;
-   equipamento protegido não é destruído indevidamente;
-   estrutura existente é reconhecida;
-   resultado é preparado.

Somente depois:

> os componentes são consumidos.

------------------------------------------------------------------------

# 53. Equipamentos não devem ser consumidos indevidamente

Um equipamento equipado, como:

-   Lanterna;
-   Bússola;
-   Mochila;
-   Cantil;

pode satisfazer determinados requisitos sem ser automaticamente
destruído.

Itens de construção e componentes físicos continuam sendo consumidos
quando fazem parte de uma construção.

------------------------------------------------------------------------

# 54. Eventos e Ambiente

A área:

> **AMBIENTE / EVENTOS**

agora funciona como uma zona persistente da expedição.

Pode conter:

-   estruturas;
-   eventos;
-   clima;
-   resultados de objetivos;
-   construções;
-   efeitos persistentes.

------------------------------------------------------------------------

# 55. Experiência planejada

O jogo passou de:

> "jogar cartas e completar receitas"

para:

> **planejar → explorar → coletar → fabricar → equipar → construir →
> sobreviver → descobrir → evoluir → completar o acampamento.**

------------------------------------------------------------------------

# 56. Filosofia de design atual

Novas cartas não devem ser adicionadas apenas para aumentar a
quantidade.

Cada nova carta deve cumprir pelo menos uma função:

-   criar uma decisão;
-   abrir uma combinação;
-   resolver um problema;
-   criar uma nova estratégia;
-   melhorar uma cadeia;
-   introduzir risco/recompensa;
-   interagir com clima;
-   interagir com sobrevivência;
-   ampliar exploração.

------------------------------------------------------------------------

# 57. Próximas possibilidades

Famílias de cartas futuras:

## Exploração

-   Binóculo;
-   Apito;
-   GPS/Mapa avançado;
-   Bússola;
-   Bastão de caminhada.

## Abrigo

-   Piso de madeira;
-   Estacas reforçadas;
-   Tarp adicional;
-   Isolante térmico.

## Cozinha

-   Panela;
-   Frigideira;
-   Utensílios;
-   Fogareiro.

## Água

-   Filtro;
-   Pastilhas de purificação;
-   Reservatório;
-   Recipiente extra.

## Saúde

-   Antisséptico;
-   Atadura;
-   Tala;
-   Kit avançado.

## Vestuário

-   Boné;
-   Camisa;
-   Calça;
-   Botas;
-   Capa de chuva;
-   Luvas reforçadas.

## Construção

-   Martelo;
-   Machadinha;
-   Serrote;
-   Pregos;
-   Parafusos;
-   Arame;
-   Kit de construção.

------------------------------------------------------------------------

# 58. Multiplayer futuro

Possibilidades:

-   troca entre jogadores;
-   construção cooperativa;
-   eventos compartilhados;
-   clima global;
-   modificadores direcionados;
-   objetivos competitivos;
-   objetivos cooperativos;
-   recursos disputados.

------------------------------------------------------------------------

# 59. Estado atual: V48 Beta

A V48 consolida uma mudança arquitetural importante:

> **Construções são parte do AMBIENTE / EVENTOS.**

Portanto:

``` text
Barraca
Fogueira
Reserva de Água
Abrigo Reforçado
ou qualquer nova estrutura
```

devem ser encaminhados para:

> **AMBIENTE / EVENTOS**

e possuir:

-   resistência;
-   barra de durabilidade;
-   ações;
-   interação com clima;
-   reparo;
-   desmontagem;
-   evolução.

------------------------------------------------------------------------

# 60. Regras de ouro para futuras versões

1.  Não misturar recurso e carta.
2.  Não misturar mão e inventário.
3.  Não misturar equipamento e estrutura.
4.  Não colocar construções em `SEU ACAMPAMENTO`.
5.  Construções vão para `AMBIENTE / EVENTOS`.
6.  Toda receita precisa referenciar IDs existentes.
7.  Toda ação deve validar pré-requisitos antes de consumir recursos.
8.  Toda operação de consumo deve ser transacional.
9.  Equipamentos equipados não devem ser consumidos automaticamente.
10. O sistema deve funcionar em desktop, tablet e celular.
11. O zoom do navegador não pode destruir o layout.
12. Novas cartas devem ter função estratégica.
13. Clima deve interagir com o ambiente.
14. O ciclo dia/noite deve afetar gameplay.
15. O jogador deve ter recuperação sem que a sobrevivência perca
    importância.
16. O Acampamento Completo permanece como objetivo final.

------------------------------------------------------------------------

# 61. Histórico resumido de versões

  Versão     Principal evolução
  ---------- -------------------------------------------------
  V1         Protótipo inicial do card game
  V2--V10    Fundação de cartas, campo, estrelas e objetivos
  V11--V13   Refinamentos de interface e lógica
  V14        Correção de animação/renderização
  V15        Cartas sem estrelas + fusão
  V16        Estado/render/animação separados
  V17        Referência visual + sobrevivência inicial
  V18        Economia por poder + estrelas
  V19--V23   Objetivos, eventos e descoberta
  V24        Cartas compactas
  V25        Login/tutorial/manual
  V26        Recursos + Aventura + Sobrevivência
  V27        Layout baseado na V17
  V28        Dia/noite + vida + crafting
  V29        Craft modal + eventos visuais
  V30        Inventário/peso + sorteio
  V31        Verso oficial das cartas
  V32        Missão + embaralhamento + compra de deck
  V33        Mão/inventário + UX
  V34        Personagem/equipamentos
  V35        Personagem + necessidades integradas
  V36        Reorganização do HUD
  V37--V39   Ajustes e estabilização
  V40        Correções do fluxo inicial
  V41        Capacidade por equipamentos
  V42        Silhueta dinâmica/equipamentos visuais
  V43        Nome oficial + Craft por tiers
  V44        Mapa/Livro + vestuário + responsividade
  V45        Revisão profunda de Craft e Objetivos
  V46        Correção de receitas/undefined
  V47        Água, cozinha, perecíveis e ferramentas
  V48        Construções movidas para AMBIENTE / EVENTOS

------------------------------------------------------------------------

# 62. Identidade oficial

## Nome

**Desbravadores: RPG Card Game**

## Subtítulo

**EXPEDIÇÃO • CONSTRUÇÃO • SOBREVIVÊNCIA**

## Status

**BETA**

## Objetivo

Construir um acampamento completo e sobreviver à expedição.

------------------------------------------------------------------------

# 63. Documento vivo

Este README deve ser tratado como um documento vivo do projeto.

Toda nova versão deve registrar:

-   versão;
-   data;
-   novas cartas;
-   cartas removidas;
-   mudanças de regras;
-   mudanças de balanceamento;
-   correções;
-   alterações visuais;
-   mudanças de arquitetura;
-   problemas conhecidos;
-   mecânicas experimentais.

A partir da V48, novas mudanças importantes devem ser acrescentadas aqui
para preservar a história e a lógica de evolução do projeto.


# V50 Beta — Durabilidade em tempo real e feedback de equipamentos

## Novidades

- Tooltip interativo ao passar o mouse sobre equipamentos do personagem.
- Tooltip mostra nome, tipo, descrição, função e status atual.
- Equipamentos com durabilidade exibem barra e percentual.
- Cantil mostra a reserva de água atual.
- Construções possuem atualização de durabilidade em tempo real.
- Fogueira possui duração/combustível em segundos e barra dinâmica.
- Papel e Madeira podem abastecer a Fogueira.
- Madeira adiciona mais duração que Papel.
- Chuva acelera o consumo da Fogueira.
- Tempestade acelera ainda mais o consumo.
- Sol intenso reduz o consumo da Fogueira.
- Ao apagar, a Fogueira é removida do Ambiente/Eventos.
- Reparos de estruturas utilizam a durabilidade dinâmica.
- Ferramentas e equipamentos possuem durabilidade inicializada de forma consistente.
- Esforço físico desgasta ferramentas equipadas.
- Alimentos perecíveis possuem frescor em tempo real quando armazenados na mesa, inventário ou mochila.
- Alimentos na mão continuam disponíveis para venda/troca antes do armazenamento.
- Cartas expandidas mostram o status atual de durabilidade/frescor.
- Estruturas mostram atualização de barra sem precisar encerrar a rodada.
- Mantida a separação entre Mão, Inventário, Personagem e Ambiente/Eventos.

## Regras de durabilidade

### Fogueira

- Duração inicial: 180 segundos.
- Capacidade máxima de combustível: 300 segundos.
- Madeira: +45 segundos.
- Papel: +15 segundos.
- Chuva: consumo acelerado.
- Tempestade: consumo fortemente acelerado.
- Sol intenso: consumo reduzido.

### Outras estruturas

A durabilidade é atualizada continuamente e depende do tipo de estrutura e do clima ativo.

### Equipamentos e ferramentas

Equipamentos possuem uma condição de 0–100%. Ferramentas utilizadas em ações de esforço físico sofrem desgaste. O status é apresentado no personagem e nos detalhes da carta.

### Consumíveis perecíveis

Alimentos armazenados perdem frescor em tempo real. Ao chegar a 0%, são considerados estragados e removidos. A mão é tratada como estado de transporte imediato e não inicia a deterioração até o armazenamento.

## V50 — objetivo de UX

O jogador deve conseguir olhar para um equipamento ou construção e entender imediatamente:

- o que é;
- para que serve;
- quanto ainda pode durar;
- qual efeito o clima está causando;
- quando precisa ser reparado ou abastecido.

---

# V51 Beta • UX do personagem e cartas interativas

## Correções e melhorias

### Personagem
- Corrigida a sobreposição dos slots de equipamento na caixa PERSONAGEM.
- Os slots agora possuem posições e alturas reservadas para evitar que MÃOS, CINTURA, ACESSÓRIO e demais equipamentos se sobreponham.
- Ajustes específicos foram adicionados para desktop, tablet e telas estreitas.

### Tooltips do personagem
- Ao passar o mouse sobre a silhueta do personagem, o jogo mostra os equipamentos atualmente equipados.
- Ao passar o mouse diretamente sobre uma camada visual de equipamento, o tooltip identifica o item correspondente.
- O tooltip informa nome, tipo, descrição, função e status atual.
- Durabilidade de ferramentas/equipamentos e percentual de água do Cantil são exibidos quando aplicáveis.
- O conteúdo do tooltip é atualizado enquanto a partida está em execução.

### Cartas em SEU ACAMPAMENTO
- Cartas que já estão na mesa agora são clicáveis.
- Ao clicar em uma carta de SEU ACAMPAMENTO, é aberto um popup detalhado.
- O popup mostra arte, nome, tipo, custo, descrição, peso, finalidade, materiais e durabilidade/frescor quando aplicável.
- O popup mantém acesso ao menu de AÇÕES da carta.

### AMBIENTE / EVENTOS
- Construções também podem ser clicadas para abrir seus detalhes.
- Eventos não estruturais possuem popup informativo próprio.
- O menu de AÇÕES continua separado do clique de detalhes, evitando que os botões acionem o popup por acidente.

### Regras preservadas
- Construções continuam em AMBIENTE / EVENTOS.
- Durabilidade continua sendo atualizada em tempo real.
- Fogueira continua usando combustível e sofrendo influência do clima.
- Cantil continua mostrando sua reserva de água.
- O README completo deve acompanhar todas as versões futuras.

# 63. V52 Beta • hidratação, exploração, upgrades e atalhos

A V52 consolida novas regras de sobrevivência e exploração:

- O Cantil equipado possui barra em tempo real no painel do personagem. A barra acompanha o percentual de água consumido automaticamente pela sede.
- Refeições preparadas na Oficina são enviadas automaticamente para o Inventário, desde que haja espaço e peso disponíveis.
- Toda nova construção inicia com 100% de durabilidade. Upgrades também reiniciam a estrutura para 100%.
- Reparos recuperam 20% da durabilidade máxima por ação, limitado a 100%.
- Upgrades de estruturas incluem Barraca → Abrigo Reforçado, Reserva de Água → Reserva Purificada e Fogueira → Área de Cozinha, com requisitos específicos.
- A evolução de uma estrutura substitui a carta anterior e apresenta uma animação de poeira no local da construção.
- Foram adicionados mapas de exploração: Mata de Coleta, Pomar Silvestre e Depósito de Apoio.
- A Bússola equipada ou guardada na mochila revela os mapas de exploração. Cada área exige ferramentas adequadas para coleta.
- Mapa e Livro de Objetivos são priorizados no sorteio inicial e permanecem garantidos até a 5ª rodada enquanto ainda não tiverem sido descobertos/consumidos.
- TAB abre a tela de mapas da expedição.
- CAPS LOCK localiza e destaca a tela do personagem.
- O tutorial foi atualizado com os novos atalhos, mapas e requisitos de exploração.
- O termo de interface **Equipe** foi padronizado para **Unidade**.

## Novos mapas

| Mapa | Coleta | Requisitos |
|---|---|---|
| Mata de Coleta | Lenha, fibras e frutas | Machadinha ou Facão |
| Pomar Silvestre | Frutas e fibras | Facão ou Lança |
| Depósito de Apoio | Metal, pregos, parafusos, arame e papel | Martelo ou Kit de Construção |

As explorações consomem 1 ação e registram quantas vezes cada mapa foi explorado.


# V53 Beta • Correção de evolução de estruturas e acesso aos objetivos

## Correções
- Barraca não permanece junto do Abrigo Reforçado após a evolução.
- Uma estrutura base é removida quando sua evolução é criada.
- Reserva de Água é substituída por Reserva Purificada quando aplicável.
- Fogueira é substituída por Área de Cozinha quando a evolução é concluída.
- Acampamento Completo remove as estruturas-base que compõem o objetivo final.
- O sistema também normaliza estados antigos que contenham simultaneamente uma estrutura base e sua evolução.

## Mapa e Livro de Objetivos
- Ter o Mapa na mão, inventário ou armazenamento já concede acesso aos objetivos durante o dia.
- Ter o Livro de Objetivos na mão, inventário ou armazenamento já habilita a conclusão.
- As flags `mapDiscovered` e `bookDiscovered` continuam registrando o uso/descoberta permanente.
- À noite, a Lanterna continua necessária para consultar os objetivos.

## Correção de receitas/objetivos
- O objetivo `MONTAR ÁREA DE COZINHA` agora gera a estrutura `ÁREA DE COZINHA`, em vez de gerar uma Refeição.
- As substituições de estruturas são feitas antes da nova estrutura entrar em `AMBIENTE / EVENTOS`.

## Regra arquitetural reforçada
Uma evolução de estrutura ocupa o lugar lógico da estrutura anterior. O jogo não deve apresentar simultaneamente uma versão básica e sua evolução.


## Aparência 16-bit consolidada (sem alteração de versão)

A V53 recebeu uma reformulação visual completa para uma estética 16-bit/pixel art, **sem alteração do número da versão**. A mudança é exclusivamente uma evolução de apresentação e UX visual da mesma release.

A reformulação abrange: cabeçalho, HUD, botões, painéis, mesa, zonas, cartas, deck, modais, tooltips, personagem, equipamentos, barras de status, inventário, oficina, mapas, eventos, multiplayer, clima e animações. Foram adotadas bordas em degraus, sombras duras, tipografia pixel, transições em passos e padrões de fundo pixelados.

# V53 Beta • Progressão pós-acampamento, pausa, Autogame e biomas reais

> **A versão permanece V53.** Estas mudanças foram incorporadas à mesma release, conforme decisão do projeto de não alterar o número da versão nesta etapa.

## Pausa
- `ESC` pausa a partida.
- Dia/noite, degradação de estruturas, deterioração de perecíveis e Autogame são congelados durante a pausa.
- O menu de pausa oferece continuar, tutorial e regras rápidas.

## Autogame
- O botão `🤖` ativa/desativa o Autogame.
- Quando ativo, o jogo toma decisões automaticamente em pequenos intervalos para que o jogador possa apenas observar a expedição.
- A lógica prioriza objetivos disponíveis, crafting possível, cartas jogáveis, compra de cartas e encerramento da rodada.
- O Autogame pode ser interrompido pelo mesmo botão.

## Acampamento Completo não encerra a partida
- Concluir o Acampamento Completo agora é um marco de progressão, não uma condição de Game Over.
- O jogador continua na mesma expedição.
- O evento libera o sistema de Duelo.
- O evento libera novos mapas de biomas reais brasileiros.

## Duelo
- O botão `⚔️` permanece oculto até o Acampamento Completo.
- O Duelo é uma disputa opcional em 3 rodadas contra um oponente simulado.
- O poder do jogador considera estruturas, equipamentos e estrelas.
- Vitória concede uma pequena recompensa de estrelas.
- Derrota reduz Vida, sem encerrar a expedição.

## Biomas reais
Após o Acampamento Completo, com Bússola equipada ou guardada na mochila, ficam disponíveis:
- Mata Atlântica
- Cerrado
- Caatinga
- Amazônia
- Pantanal

Cada bioma exige ferramentas adequadas e possui uma tabela de recursos própria.

## Novos recursos
Foram adicionados recursos coletáveis para ampliar a exploração:
- Frutas Silvestres
- Sementes
- Argila
- Bambu

Eles passam a fazer parte do estado de recursos da partida e podem ser expandidos em receitas futuras.

## Controles atualizados
- `ESC` = Pausar/retomar
- `TAB` = Abrir mapas da expedição
- `CAPS LOCK` = Destacar/ir para o painel do personagem
- `🤖` = Ativar/desativar Autogame
- `⚔️` = Abrir Duelo, quando desbloqueado
- `➡️` = Avançar para a próxima rodada

## Princípio de progressão
A sequência principal passa a ser:

```text
RECURSOS
  ↓
CRAFT
  ↓
ESTRUTURAS
  ↓
ACAMPAMENTO COMPLETO
  ↓
NOVOS BIOMAS
  ↓
EXPLORAÇÃO AVANÇADA
  ↓
DUELOS E NOVOS DESAFIOS
```

O Acampamento Completo é, portanto, a preparação para a segunda camada da expedição, e não o encerramento da partida.

## Ajuste visual de tipografia - V53

A interface continua integralmente com identidade visual 16-bit, porém a tipografia pixelada foi removida dos textos corridos e controles por prejudicar a leitura.

A nova hierarquia tipográfica usa:
- **Rajdhani** para títulos, HUD, botões, nomes de cartas e elementos de destaque;
- **Inter** para descrições, textos corridos, tooltips, regras e informações detalhadas.

O objetivo é manter a aparência de RPG/card game com estética retrô, sem sacrificar legibilidade em desktop, tablet, celular ou zoom do navegador.

**Importante:** essa alteração é exclusivamente visual e **não altera o número da versão**. O projeto continua em **V53 Beta**.


## V53 Beta • Tipografia, rodapé, layout e embaralhamento

Esta atualização mantém a versão **V53 Beta** e aplica apenas refinamentos de apresentação e UX:

- toda a interface usa a mesma família tipográfica da caixa **COMPRAR CARTA**, baseada em Rajdhani;
- rodapé padronizado como `DESBRAVADORES: RPG CARD GAME • PRE-ALPHA • BUILD 0.53 • DESENVOLVIDO POR KNOXZINHO`, com o crédito em itálico;
- revisão responsiva para reduzir sobreposição, corte e desalinhamento em desktop, tablet, celular e zoom;
- animação de embaralhamento refinada e reduzida para aproximadamente 3 segundos;
- arte do verso fornecida para as cartas/deck também é usada como textura sutil no fundo das cartas frontais;
- a versão permanece **V53**, sem criação de V55.

## V53 Beta • Fluxo do sorteio inicial

A etapa de sorteio inicial foi refinada sem alteração do número da versão.

Antes do embaralhamento, a janela apresenta somente as informações da missão e a instrução para iniciar o sorteio:
- `MISSÃO DEFINIDA: [Nome da missão]`;
- `O sorteio inicial acontece quando você clicar em EMBARALHAR`;
- botão `🔀 EMBARALHAR`.

As cartas exibidas nessa etapa permanecem estáticas. A animação de embaralhamento somente é ativada depois que o jogador clica em **EMBARALHAR**.

Durante a animação, a mensagem apresentada é:
> `Prepando a Deck para sua aventura`

A animação continua com duração aproximada de 3 segundos. Ao término, as cartas iniciais são distribuídas para a mão.

**Importante:** esta alteração mantém o projeto em **V53 Beta**.


## Atualização V53 · UX da expedição

Esta atualização mantém deliberadamente a identificação **V53 Beta / Build 0.53** e acrescenta os seguintes refinamentos de experiência:

- A seleção da primeira missão apresenta **MISSÃO DEFINIDA: [nome]** antes do sorteio.
- O sorteio inicial só começa após o clique em **EMBARALHAR**.
- A animação inicial dura **3 segundos**, usa deslocamento em uma única direção e exibe a mensagem **Preparando as cartas para sua aventura** com barra percentual de progresso.
- Toda a interface utiliza **Rajdhani** como família tipográfica principal, mantendo a leitura mais limpa dentro da estética 16-bit.
- O **📜 DIÁRIO** pode ser ocultado ou fixado como uma janela durante a partida.
- O tutorial inicial explica ESC para pausa e o controle de visibilidade/fixação do Diário.
- **COMPRAR CARTA** e **DECK DE MODIFICADORES** foram compactados para ocupar a mesma linha quando houver largura suficiente.
- Objetivos que já possuem todos os requisitos passam a gerar uma notificação visual com um **pássaro voando**, informando qual objetivo está pronto para ser cumprido.
- O layout recebeu ajustes responsivos para reduzir cortes e sobreposições.

### Regra de versionamento

As alterações acima são parte da **V53**. O projeto não avança o número da versão para estes refinamentos visuais e de UX.


## Atualização V55 · Modificadores ocultos, objetivos em popup e embaralhamento corrigido

- Build atual: **0.54**.
- Modificadores agora entram diretamente em uma mão exclusiva de 1 carta e não ocupam os 5 espaços da mão principal.
- O conteúdo do modificador permanece oculto enquanto estiver na mão. O jogador usa **ATIVAR** para revelar e aplicar o efeito.
- **MUDAR MODIFICADOR** permite trocar a carta. A troca é gratuita após 2 rodadas; antes disso, é possível trocar imediatamente pagando o custo do novo modificador, se houver estrelas suficientes.
- O painel lateral não exibe mais nome, descrição ou arte detalhada do modificador que está oculto.
- **OBJETIVOS** saíram da lista fixa do painel lateral e passam a ser exibidos em uma janela popup por meio de **ABRIR OBJETIVOS**.
- Quando um objetivo fica pronto para conclusão, a notificação visual do pássaro é disparada uma vez por objetivo enquanto ele permanecer pendente.
- A animação do embaralhamento inicial foi corrigida: a animação é desativada no estado de espera e só recebe `animation` quando a sequência de 3 segundos começa.
- O fluxo inicial continua: aviso de desenvolvimento → seleção de modo → tutorial → escolha de objetivo → tela estática de embaralhamento → clique em **EMBARALHAR** → animação → mão inicial.
- Arte de verso das cartas mantida em `assets/card-back.png`.


## Atualização V55 · Interface responsiva
- Barra superior reduzida aos ícones de Inventário, Mapa e Craft e ao indicador PLANEJAMENTO • DIA/NOITE.
- Título do deck de modificadores simplificado para MODIFICADORES.
- Diário com botão OCULTAR/MOSTRAR funcional, incluindo restauração do estado salvo.
- Objetivos apresentados em popup responsivo, com grade adaptativa e rolagem interna.

## Atualização V57 · Finalização de jogada e embaralhamento

- O botão de encerramento da rodada foi transformado em uma ação primária explícita: **✓ FINALIZAR JOGADA**.
- O botão possui área maior, texto descritivo, contraste reforçado e adaptação para telas pequenas.
- O título/aria-label explica que a ação encerra a jogada e inicia a próxima rodada.
- Corrigida a cascata CSS que anulava a animação das cartas no modal de embaralhamento. A regra final de V57 tem especificidade superior à regra que colocava `animation:none`.
- A animação do embaralhamento usa movimento contínuo, escalas e rotações leves, com atraso entre as cartas, durante a sequência de 3 segundos.
- O verso `assets/card-back.png` continua sendo usado nas cartas.
- Build: **0.57**.


## Atualização V57 · Embaralhamento e cartas

A animação de embaralhamento inicial foi retirada da dependência de CSS e passou a ser controlada diretamente por JavaScript com `requestAnimationFrame`, evitando regras antigas da cascata que poderiam cancelar a animação. As cartas da mão também receberam proteção de visibilidade e o sorteio inicial ganhou uma rotina de entrega robusta para garantir cartas válidas na mão.


## Atualização V58 · Compras e animações
- Texto da compra de cartas resumido para uma leitura mais rápida.
- Animação de compra reforçada, com carta voando do deck até a área da mão em trajetória curva.
- Embaralhamento inicial refeito como simulação de baralho real: cada carta recebe movimentos, rotações, escalas e alvos aleatórios renovados durante os 3 segundos da preparação.
- Build atual: 0.58.

## Atualização V59 · Inspeção de decks e novo embaralhamento

- O indicador `👣 AÇÕES` foi renomeado para `👣 MOVIMENTOS`.
- Clicar no deck principal ou no deck de modificadores abre uma janela de inspeção responsiva com todas as cartas daquele deck em destaque.
- As cartas podem ser pressionadas e arrastadas visualmente, mas retornam à posição original e não podem alterar a ordem do deck.
- Duplo clique em uma carta executa uma animação de giro vertical por 2 segundos, funcionando como interação visual/AFK sem modificar o estado da partida.
- Foi adicionado o comando `EMBARALHAR NOVAMENTE` à inspeção dos decks.
- O novo embaralhamento respeita intervalo mínimo de 5 rodadas entre usos.
- O custo começa em ⭐1 e aumenta em ⭐2 a cada uso: ⭐1, ⭐3, ⭐5, ⭐7, etc.
- O embaralhamento manual apresenta a animação de cartas sendo misturadas antes de devolver o deck ao estado embaralhado.
- O embaralhamento manual não consome movimentos, apenas estrelas.
- A contagem e a rodada do último embaralhamento são mantidas no estado da partida.

## Atualização V60 · Inspeção dos decks

- Grade do inspetor de decks reorganizada para manter as cartas alinhadas dentro da área da janela, com rolagem interna quando necessário.
- A arte do verso usa dimensionamento completo para evitar cortes da imagem.
- Duplo clique no verso não revela mais a frente da carta.
- Duplo clique executa uma rotação vertical contínua durante 2 segundos, funcionando como animação de ociosidade da carta.
- A ordem lógica do deck continua inalterada durante a interação visual.

## Atualização V61 · Deck responsivo

- Janela de inspeção dos decks agora respeita a largura real do modal.
- Grade responsiva reduz o número de colunas em telas menores.
- Cartas mantêm proporção quadrada e a arte completa do verso, sem corte.
- Conteúdo excedente usa rolagem interna, sem ultrapassar a caixa do deck.
- Build atualizada para 0.61.


## Atualização V62 · Proporção fixa da mão

A área de mão passou a manter sempre a mesma largura relativa de cada carta usada no layout de cinco cartas. Com 1, 2, 3, 4 ou 5 cartas, as cartas não se expandem para preencher o espaço disponível.


## Atualização V63 · Rotação, contas, progresso e custos de cartas

- A rotação vertical das cartas no inspetor foi acelerada para uma animação de 2 segundos com maior número de voltas, sem revelar a frente.
- O tutorial recebeu novas etapas explicando o custo individual das cartas, a inspeção/embaralhamento dos decks e o sistema de sessão e progresso por usuário.
- Foi adicionada uma tela de conta local com criação de usuário e autenticação por senha armazenada como hash SHA-256 no navegador.
- Cada usuário possui uma chave de save própria e uma sessão local independente.
- O progresso da expedição é salvo automaticamente a cada 2 segundos e também antes de fechar a página.
- Uma expedição salva pode ser retomada sem reiniciar a mão, o deck, os modificadores, a rodada ou os recursos.
- Foi adicionada a opção de sair da conta pelo menu de pausa.
- O sistema de custos das cartas foi reforçado: cartas jogáveis exigem o número de estrelas definido em `C[id].cost`, e o custo é retirado do total ao jogar a carta.
- Equipamentos, Mapa e Livro também passam a descontar o custo de estrelas ao serem jogados/consultados.
- Exemplo: CORDA custa ⭐2; o jogador precisa possuir pelo menos 2 estrelas e, ao jogar a carta, perde 2 estrelas e 1 movimento.
- A construção de estruturas continua utilizando seu custo próprio e mantendo a validação de estrelas e movimentos.
- Build atualizada para 0.63.

> Observação: o sistema de contas desta versão é local, adequado ao protótipo. Ele não substitui autenticação de servidor para um produto publicado em produção.
