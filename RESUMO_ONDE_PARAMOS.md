# 📌 Onde paramos — JG Pazotto Holding

> ## 🟢 COMECE AQUI (leia só isto para começar a trabalhar)
>
> **Sistema:** https://jgpazotto.com/**sistema.html** ← ENDEREÇO ÚNICO (08/09). Os antigos redirecionam.
> **Entrar:** `jgpazotto@gmail.com` + a senha que ELA criou (eu nunca vi; está salva no Chrome dela)
> · sempre abrir com **Cmd+Shift+R**
> **Site:** https://jgpazotto.com · **Vitrine:** /anuncios.html
> **Pasta:** `/Users/geraldoejoicepazotto/Documents/jgpazotto-v2.0` (conectada)
> **Números:** 56 carros · 11 imóveis · 19 clientes · 9 carnês abertos · $ 47.952,50 a receber
>
> ### ⚠️ 08/09 parte 2 — ELA TESTOU E ACHOU DOIS DEFEITOS MEUS (já corrigidos)
> "qualquer coisa q clica, a tela rola para cima" e "quando clico para ampliar está aparecendo
> outra coisa". **Mesma causa:** `mostrarZap()` redesenhava o HTML inteiro a cada clique, então
> (a) a rolagem voltava ao topo e (b) entre o 1º e o 2º clique do `ondblclick` o quadradinho
> mudava de lugar e a lupa abria a foto errada. **Regra nova: interação de conferência não pode
> redesenhar a lista.** Detalhe na seção do dia.
>
> ### ✅ O que ficou pronto em 08/09 (leia a seção do dia no fim do arquivo)
> 1. **As fotos do WhatsApp aparecem ao lado de cada linha de dinheiro.** A tela agora aceita a
>    **pasta** exportada COM mídia. 190 das 214 linhas do C-MAX AZUL têm foto do lado.
>    1 clique na miniatura = guardar a foto junto · 2 cliques = ampliar.
> 2. **De-duplicação por palavra parecida.** "Funilaria $2.500" e "funileiro $2.500" agora se
>    avisam. Filtro por radical POUCO comum + mesmo valor + até 120 dias → 4 pares no C-MAX,
>    todos de verdade (o funileiro, dois bônus do Mauricio, dois acertos com o Luiz).
> 3. **Endereço único: jgpazotto.com/sistema.html.** v3.5/v3.6/v3.7 viram uma porta que leva
>    para lá. `area.html` e `manifest.json` apontavam para a v3.5 (login velho) — corrigidos.
> 4. ⏳ **FALTA o depósito das fotos no Supabase Storage** — o Chrome dela estava minimizado e
>    o painel do Supabase não renderiza em aba escondida. **É o primeiro passo da próxima vez.**
>
> ### O que mudou em 07/09 (foi muita coisa — leia as seções do dia)
> 1. **Os dados saíram do navegador e foram para o Supabase.** Login de verdade, senha de
>    verdade, funciona em qualquer aparelho. `admin`/`joice123` **não existe mais**.
> 2. **Permissão por funcionário, de verdade** — os dados estão separados por área no banco.
>    Quem não pode ver o Financeiro **não recebe** o Financeiro. Provado por teste.
> 3. **Backup automático** — o sistema baixa uma cópia por dia em `~/Downloads` sozinho.
> 4. **Vitrine de anúncios no ar** com o primeiro carro.
> 5. **Logo certo no site** (era arquivo errado, não decisão de design).
> 6. **A importação do WhatsApp virou outra coisa:** ela explicou o negócio e agora a tela
>    pergunta *"isso é o quê, e de quem?"* em vez de *"isso é gasto?"*. **Leia a seção
>    "A LIÇÃO MAIS IMPORTANTE ATÉ AGORA" — é a regra do negócio dela.**
>
> ### 🔑 COMECE POR AQUI AMANHÃ — as fotos do WhatsApp
> Ela conectou a pasta `~/Documents/jgpazotto-v2.0/Whatsapp/WhatsApp Chat - Total Loss Blue 10`
> (ela achou que não tinha conseguido; **conseguiu sim**). É a exportação **COM MÍDIA** do
> C-MAX AZUL 9DHW447: **342 fotos + 7 vídeos, 106 MB**, mais o `_chat.txt`.
> O texto nomeia cada foto na hora exata: `<anexado: 00000006-PHOTO-2022-07-25-15-39-29.jpg>`.
> **Medido: 47% das linhas de dinheiro têm foto a até 6 mensagens de distância** (136 de 288).
> É isso que ela pediu — ver a foto ao lado da linha para decidir. Plano:
> 1. mostrar a miniatura da foto ao lado de cada linha na tela de importação;
> 2. **Supabase Storage** para guardar as que ela escolher (106 MB não cabem no banco de dados);
> 3. de-duplicação por **palavra parecida** ("Funilaria" vs "funileiro" ainda passam como duas).
>
> ### Depois disso, na ordem
> - Ela cadastrar os **períodos de locação** (aba 🔑 Quem ficou com o carro) — sem isso a
>   cobrança não sabe de quem é. É o gargalo de tudo.
> - Cadastrar o **Geraldo como dono** em 🧑‍💼 Funcionários.
> - **Unificar o endereço**: v3.5, v3.6 e v3.7 estão todos no ar. Ela disse que "ficou tudo
>   bagunçado" — juntar num endereço só.
> - Encher a vitrine (marcar Disponível + foto + preço) · 16 linhas de aluguel/depósito ·
>   8 carnês em aberto.
>
> ### Publicar (funciona, 3 segundos)
> O `.git` da pasta dela está travado por `HEAD.lock`. O jeito que funciona:
> ```
> cd $HOME && git clone --depth 1 "$(cd ~/mnt/jgpazotto-v2.0 && git config --get remote.origin.url)" pub
> cp ~/mnt/jgpazotto-v2.0/<arquivo> $HOME/pub/
> cd $HOME/pub && git add -A && git commit -q -m "..." && git push -q origin HEAD:main
> ```
> Espere ~90 s (GitHub Pages) e confira com `?v=algo` na URL.
> **Confira o diff contra o GitHub antes de sobrescrever** — a cópia do Mac fica velha.
>
> ### Como trabalhar com a Joice
> Português simples e carinhoso · **faça por ela**, nunca mande abrir terminal · **publique
> você mesma** · avise na hora se não conseguir · só este projeto (não misture com o Postou).
> **Ela é ótima parceira de diagnóstico** — foi ela que explicou as oito naturezas do dinheiro
> e por que os gastos duplicavam. Quando ela descreve um sintoma, leve a sério.
> ⚠️ **O tempo de uso dela acaba rápido.** Agrupe o trabalho, publique uma vez só, decida
> sozinha em vez de perguntar a cada passo, prefira ler a tela por código a pedir print.
> **Assunto novo = conversa nova**, anexando este arquivo.
>
> ### Erros meus de 07/09 — não repetir
> - Montei 4 opções de logo quando **o logo certo já estava na pasta** (`imagens/logo-jg.png`).
>   **Procure o arquivo antes de propor design.**
> - Publiquei um `escapaHtml` duplicado: já existia como `const`, e eu só procurei por
>   `function`. **Procure também `const NOME =`.**
> - Pus `vidro` e `gasolina` como "dano" e 21 linhas foram classificadas errado.
>   **Teste a regra contra as conversas reais antes de publicar** (receita no fim do arquivo).

**Sistema:** jgpazotto.com/dashboard-v3.5.html · **Entrar:** `admin` / `joice123`
**Versão dos dados:** `2026-09-02-04` · abrir com **Cmd+Shift+R**

---

## 1. O sistema hoje

**52 carros · 11 imóveis · 25 carnês · 19 clientes**

Menu: Dashboard · **Clientes** · Fornecedores · Carros · **💵 Vendas/Carnê** · Aluguel · Imóveis · 📢 Anúncios · **✅ Dar baixa** · 🔔 Cobrança · **📲 Importar do WhatsApp** · Financeiro · Backup

### As telas que a gente usa pra trabalhar

- **💵 Vendas / Carnê** — quem comprou e está pagando. Hoje: **$ 56.314,50 a receber**, 17 pagando, 14 com atraso, 4 encerrados (Jiner, Joel, Thiago, Artur).
- **✅ Dar baixa** — todas as parcelas em aberto numa tela só, já com valor e data de hoje. Clica e pronto. Tem **↩️ desfazer**. A multa de 10% **não entra sozinha** — aparece em cinza com botão **+10%** (as planilhas vieram com multa zerada; só 40 parcelas tinham multa lançada).
- **🔔 Cobrança** — junta tudo que cada pessoa deve (parcela + multa + FasTrak + licenciamento).
- **👥 Clientes** — 19 fichas dos documentos, com **aniversário** 🎂, os carros de cada um e quanto devem.
- **📲 Importar do WhatsApp** — exporta a conversa do grupo do carro (**sem mídia**), solta o `.txt`, eu acho todos os valores e você marca o que é gasto.

### Fotos e site

- **Marca d'água gravada na foto** que vai pro site (canto inferior direito, 26%, 88%) — o original fica limpo, documento nunca é marcado.
- **📸 Tirar foto agora** em todas as áreas de foto (abre a câmera no celular).
- Foto entra redimensionada, pra não encher a memória do navegador.
- **Tipo do veículo**: Carro / Trailer / Clássico / Moto, com filtros na frota.
- Carro que **muda de placa** (foi pra outro estado) não duplica: eu procuro pelo VIN e pela placa antiga.

---

## 2. MKZ Red — primeiro carro feito pelo WhatsApp ✅

- Placa nova **XZL6150** (era 9HFY639) · VIN 3LN6L2LUXER824814 · 50.350 milhas
- Título **CLEAN** (era salvage) · seguro **Bristol** · no **Texas**, na garagem, **disponível**
- **58 gastos, $ 10.480,09** — 3 anos inteiros, tirados do grupo. (Guardei os 16 antigos da planilha escondidos, em `gastosDaPlanilhaAntiga`.)
- Histórico completo escrito nas Observações do carro: Gustavo → Kaio → José → Romulo → Cassio → Zé
- **Recebidos está $ 0,00** — os aluguéis desses 3 anos não estão lançados em lugar nenhum
- **Falta o preço do anúncio** (em 2023 era $350/semana + $350 depósito na Bay Area)

**Combinado:** WhatsApp é a fonte principal dos gastos, e eu sempre te mostro a lista antes de aplicar.

---

## 3. O que falta

1. **Mandar os outros carros pelo WhatsApp**, um por vez
2. **Telefones dos clientes** — sem eles não consigo ligar o botão de WhatsApp nas fichas
3. **6 pessoas com documento mas sem carro**: Helio Ribeiro · Antonio Garcia Reyes · Jairo Florez Diaz · Mauricio Bautista Escalante · Gustavo Silva Neri Rocha · Andrew Porto Moura
4. **Ines e Rafael** os dois no Sonata 9NTW055 — foi troca de comprador?
5. **Wilson duplicado** no Sonata 9ROZ437
6. **Trailers e clássicos** — cadastrar (o tipo já existe)
7. **Botão "Área de Serviço"** no site — recado pronto pra Claude do Site
8. **Aluguéis recebidos** — não existem no sistema ainda

---

## 4. Como eu trabalho com você

- Falo simples e carinhoso e **faço as coisas por você**
- **Publico eu mesma** pelo GitHub no seu Chrome (o `git push` do seu Mac não funciona — o remoto está com um token de mentira)
- Se eu não conseguir algo sozinha, **eu te aviso na hora**
- **Só este projeto** — não misturo com o Postou
- **WhatsApp eu não acesso** — você exporta a conversa e eu leio
- **Documentos de cliente ficam só no seu computador** (`_docs_privados`, o Git nunca publica)
- ⚠️ A senha está dentro do arquivo, que é público. Quando estiver redondo, quero te propor um login de verdade.
- Eu **não tenho memória entre conversas** — este resumo é a nossa memória

---

*"Não nos apegamos — se não alugar, a gente vende."* 💛

---

## 📅 04/09/2026 — sessão no Claude Projects (memória entre conversas)

**Resolvido de vez: publicar.** O remote do git estava com `SEU_TOKEN` de mentira. A Joice
gerou um Personal Access Token (escopo `repo`) e ele está gravado em `.git/config`
(nunca é publicado). **Publicar agora é `git push`, 3 segundos.** Nunca mais subir
arquivo pela página do GitHub no Chrome.

⚠️ **O `.git` dentro da pasta dela está travado** por `HEAD.lock` e `index.lock` que o
mount não deixa remover. **Contorno que funciona:** clonar em `$HOME/pub` (fora do mnt),
copiar os arquivos pra lá, commitar e dar push. É assim que foi feito hoje.

**Publicado hoje:**
- Os 10 arquivos do site que estavam parados (index, nossa-historia, anuncios, area,
  manifest, css/site.css, brasao-jg.png/.webp, icone-192/512) — commit `d255c31`
- Cadeadinho do rodapé apontando pra `area.html` em vez de entregar o endereço do
  dashboard ao Google — commit `2183eb7`
- `.gitignore` protegendo `_backups/`

**Sincronizado:** o `dashboard-v3.5.html` do Mac dela estava atrasado (`2026-09-01-02`,
3446 linhas). Foi trocado pela versão do GitHub (`2026-09-02-04`, 3802 linhas).
*A cópia do Mac fica velha sempre que se publica pela web — conferir sempre.*

**Backup feito:** `_backups/backup_2026-09-04.json` (1,9 MB) — 52 carros, 25 carnês,
19 clientes, 11 imóveis. É a fonte da migração pro banco de dados.

**Acesso novo:** a pasta `~/Downloads` está conectada. O zip dos anúncios e os backups
podem ser pegos direto de lá, sem ela arrastar nada.

**Decidido por ela hoje:** vitrine de anúncios pelo sistema (ela marca, eu publico) e
**banco de dados de verdade (Supabase)** como solução da senha e do multiusuário.

**Próximo passo:** ela criar a conta no Supabase e mandar a Project URL + a chave
`anon public`. Plano combinado: manter o objeto `database` como está e trocar só
`saveData()`/`loadData()` por chamadas ao Supabase (uma linha por usuário, JSON),
mais `supabase.auth` no lugar do login falso. Mudança cirúrgica, não reescrita.

**Sobre a senha (dito a ela com todas as letras):** `admin`/`joice123` está em texto puro
na linha 1084 de um arquivo público, e a tela de login é só uma div escondida — dá pra
pular pelo console. É cortina, não fechadura. Só o Supabase resolve.

### 04/09 — parte 2: o bug que travava tudo, e a aba nova

**O bug (era isso que travava a Joice).** Em `displayCarros()` a lista era filtrada com
`grupo.testa((c.status||'').toUpperCase())` — mandava o **texto** do status, mas todo
`testa` espera o **carro** (faz `c.status` por dentro). Resultado: a contagem dos filtros
(que usa `g.testa(c)`, certo) mostrava "Comigo hoje 34" e a tabela dizia "Nenhum carro
nesse filtro". Sem linha na tabela, não dava pra abrir carro nenhum — nem pro anúncio,
nem pro WhatsApp. Corrigido para `grupo.testa(c)`. Commit `1caac4f`.
*Lição: contagem e lista usavam caminhos diferentes; sempre conferir os dois juntos.*

**Perda silenciosa de dados (corrigida).** `saveCarro()` e `saveImovel()` montavam o
objeto **do zero**. Qualquer campo que a tela não conhece era apagado ao salvar — inclusive
`gastosDaPlanilhaAntiga` do MKZ. Agora começam com `...anterior` (o registro que já existia).

**Aba nova: 📄 Docs e Notas** (fica entre Anúncio e Fotos). É a *linha do tempo por carro*
que ela pediu duas vezes. Guarda em `c.notas = [{data, texto}]`, mais recente em cima,
data em `<input type="date">`. Funções: `renderNotas()`, `addNota()`, `dataBonita()`,
`escapaHtml()`, variável `cNotas`. O quadro de **documentos está desenhado mas desligado**,
com o motivo escrito na tela — documento vai pro Supabase Storage, não pro localStorage.
Categorias que ela pediu: título/documento, seguro/apólice, contrato, recibos de oficina,
documentos do cliente, e **fotos de dano do veículo na aba Vistoria**.

**CSS:** `.tabs` ganhou `flex-wrap: wrap` — com 10 abas a última estava sendo cortada.

⚠️ **Não mexer no `SEED_VERSAO` para publicar código.** Ele dispara `juntarDadosNovos()`
e o recado verde. Só sobe quando os **dados** da semente mudam. Para código, `Cmd+Shift+R`.

**Como testar sem estragar nada:** abrir o dashboard pelo Claude in Chrome, rodar
`openCarroModal(id)` e as funções direto pelo console. Enquanto não chamar `saveCarro()`,
nada é gravado no localStorage dela.

### 04/09 — parte 3: onde estão os dados de verdade

**WhatsApp Web FUNCIONA, mas só 3 meses.** Ela está logada no Chrome dela; dá pra ler
os grupos direto (Claude in Chrome → web.whatsapp.com), sem exportar nada. Os grupos de
carro seguem o padrão `[Sold/LV/TX] Modelo Ano Cor PLACA Cliente` — ex.: `Sold Cmax 14
Black 9TXJ316 Renan`. **Limite real:** a tela avisa *"Use o WhatsApp no seu celular para
ver mensagens enviadas e recebidas antes de 25/05/2026"*. Histórico antigo só no celular
→ para conversa antiga, ainda precisa exportar o `.txt`.

**A fonte melhor estava na pasta o tempo todo:** `carros_venda.csv/` tem **34 fichas
`*FICHA E PAGAMENTOS*.csv`, com 810 parcelas** — número da parcela, vencimento, valor,
quanto foi pago, **data do pagamento** e desconto do seguro. Muito melhor que o WhatsApp.
Prefixos: `V-` vendido, `P-` parcela, `LV` locação. Ex.: `P C-REN` = Renan,
`V-SONATA -FICHA E PAGAMENTOS INES.csv` = Ines (a ficha diz *"retirado dia 08/01/2025"*,
confirmando que ela abandonou o carro).

**O resumo `CARROS-CARROS - A VENDA.csv` tem coluna FALTA** preenchida por ela. Cruzando
com o sistema: **$ 14.220 de dívida fantasma** (planilha diz $0, sistema ainda cobra) —
Rafael/Ines 9NTW055, Bruno 9EBL950, Walter 9HGT166, Fabio 8YQB922, Poliana 9EPA280, mais
Lara, Martha, Ana e Cintia com parcelas soltas.

**E os 8 que realmente devem batem de perto** entre planilha e sistema (diferença de $50
a $2.500): Daniel, Renan, Romulo, Bruno 8ZMH712, Wilson MKZ, Veronica, Benedita, Andressa.
**Ou seja: o sistema é confiável — só parou em out/2024.**

**Achado:** comparando as fichas com o sistema, há pelo menos **$ 7.984 de pagamentos que
o sistema não conta** (Bruno +5.080, Wilson +2.154, Wilson +750). A comparação foi por
primeiro nome, então cobre pouco — **o trabalho certo é reimportar as 34 fichas casando
por carro**, mostrando o diff antes de aplicar.

⚠️ **Não confundir:** a coluna FALTA do resumo diz $0 para vários carnês cujas fichas
individuais ainda têm parcelas sem pagamento lançado. Ela considerou quitado; o detalhe
nunca foi preenchido. Perguntar antes de decidir por ela.

### 04/09 — parte 4: a reimportação NÃO era necessária (e uma correção minha)

**Erro que eu cometi e corrigi:** cruzei fichas x sistema pelo PRIMEIRO NOME do cliente e
anunciei "$ 7.984 não contabilizados". Era falso — "Bruno" e "Wilson" existem em mais de
um carro, então comparei carnês trocados. **Sempre casar pela PLACA**, usando os arquivos
`carros_venda.csv/<prefixo>-VEICULO.csv`, que trazem a placa de cada prefixo.

**Refeito pela placa: TOTAL A LANÇAR = 0 parcelas.** As 22 fichas que casaram batem
exatamente com o sistema (Renan 24/53, Bruno 22/30, Lara 26/40, Ines 24/27...).
**A importação da outra Claude foi fiel. Não há nada para reimportar.** Os pagamentos que
faltam não estão nas planilhas dela também — nunca foram anotados em lugar nenhum.

**Aplicado no localStorage dela (via Claude in Chrome, `saveData()`): 12 carnês encerrados**
— Fabio, Walter, Poliana, Bruno Couto (9EBL950), Lara, Martha, Cintia, Ana (à vista),
Ines (devolveu 08/01/2025), Rafael, e os DOIS Wilson do 9ROZ437 (o segundo marcado como
"carnê repetido"). Cada um com `motivoEncerrado` escrito.
**Cópia de segurança em `localStorage['jgpazotto_data_ANTES_04set']`** — dá pra voltar atrás.

**A receber caiu de $ 56.314,50 para $ 47.952,50.** Carnês abertos: de 21 para **9**.

**Os 9 que realmente devem:** Romulo 9HRT558 $8.250 · Veronica 9ETZ128 $6.588 ·
Renan 9TXJ316 $6.365 · Wilson 9KVR829 $5.825 · Bruno 8ZMH712 $5.250 ·
Benedita 9NBL362 $5.250 · Daniel 9FSM563 $4.950 · Andressa/Plinio (Tucson, sem placa)
$3.475 · Alexandre Menor (Sonata, sem placa) $2.000.

**6 fichas ficaram sem casar** porque o `-VEICULO.csv` delas não tem placa:
CMAX WILSOM, SONATA (Wilson), MODELO, P-TUCSON (Andressa/Plinio), V - EPA (Poliana),
V- SONATA BRC (Alexandre Menor). Perguntar as placas a ela.

### 04/09 — parte 5: fichas de locação unidas às de venda

**O problema que ela levantou:** vários veículos eram de LOCAÇÃO e depois viraram VENDA.
Ficaram como DUAS fichas — a da locação com o dinheiro do aluguel, a da venda com o carnê.
Resultado: o carro nunca mostrava lucro real.

**3 pares achados pelo VIN e unidos** (ficha de venda sobrevive, a de locação some da lista):

| VIN | locação | venda | trouxe |
|---|---|---|---|
| 1FADP5CU9DL531362 | 8YES705 | **9NBL362** Benedita | **$ 10.535** de aluguéis (Marcos, Joaquim, Fabio, Thiago, Luiza, Leandro) |
| 1FADP5CU3EL521248 | 9ETZ311 | **9TXJ316** Renan | **$ 4.732** de aluguéis (Marco, Luiza, Thiago) |
| 3LN6L2LU7FR621378 | (sem placa) | **9HRT558** Romulo | nada (ficha vazia) |

Carros: 52 → **49**. A ficha antiga inteira ficou guardada em `c.fichaAnteriorLocacao`, e
cada carro ganhou uma **nota datada** contando a união. `placaAntiga` preenchida.
Backup em `_backups/backup_ANTES_DE_JUNTAR_FICHAS.json`.

⚠️ **LIMITE DO localStorage BATEU DE VERDADE.** Guardar uma 2ª cópia dentro do navegador
deu `QuotaExceededError` (~5 MB, ela já usa 1,9 MB). **Nunca guardar snapshot no
localStorage** — baixar arquivo. `makeBackup()` tem `alert()` no fim (congela a automação);
para baixar por código, montar Blob + link.click() sem o alert.

### O QUE AINDA FALTA PARA O LUCRO POR VEÍCULO (pedido central dela)

O balanço hoje é só `Recebidos − Gastos`, onde Recebidos = linhas manuais da aba Balanço.
**Falta:**
1. **Campo VALOR DE COMPRA** — não existe no modelo do carro (só no `carrosAntigo` morto,
   como `valcompra`). Sem ele a planilha de venda entra o carro como zero, que é a
   reclamação dela.
2. **Tela de ALUGUÉIS RECEBIDOS** — hoje só existe a lista manual do Balanço.
3. **Balanço somando tudo:** `Lucro = (aluguéis + recebido no carnê/venda) − (compra + gastos)`.
   O recebido do CARNÊ hoje NÃO entra no balanço do carro — são contas separadas.

**Ela disse que tem os valores de compra nas planilhas e nos grupos do WhatsApp.**

### 06/09 — veículos do Texas cadastrados + campo Valor de compra

**Novo no sistema:** campo **Valor de compra $** na Ficha do carro (`c.valorCompra`) e o Balanço
virou **Lucro = Recebidos − (Compra + Gastos)**, com card "Compra" e aviso de que o recebido
do carnê ainda não entra nessa conta.

**7 veículos criados** (status TX), com valor de compra e uma nota contando a origem:
Motorhome Limpão 9NJN061 ($8.054,84) · F150 XLT Lariat clássico ($1.080) · Trailer Ovo
1PK4858 ($4.745) · Ram Van 2500 ($5.750,44) · Bruto Keystone Premier 2016 ($4.835) ·
Corvette 1982 Cross-Fire ($4.403) · Outlander 2016 Red 9KNP013 ($4.391,64).
**Smurf corrigido:** era `marca "BB SMURF", placa "PAZOTTO"` → agora **placa 9FMS542**,
VIN JTEBU11F370075643, status TX. É o carro de uso do casal e vai ser anunciado.
Carros: 49 → **56**.

⚠️ **GASTOS DOS GRUPOS NÃO FORAM IMPORTADOS — de propósito.** A extração automática não
fecha com os totais que o próprio Geraldo escreve no grupo:

| veículo | minha soma | total no grupo |
|---|---|---|
| Ram Van | $8.068 | $7.899 |
| Bruto Keystone | $7.705 | $8.390 |
| Trailer Ovo | $6.798 | $4.745 |
| Motorhome | $24.605 | $8.993 |
| Outlander 16 | $30.530 | $11.481 |

Causa: os grupos **repetem a lista inteira** como conta corrente, e há endereços/códigos que
parecem dinheiro. Já aplico a regra do sistema (só vale com centavos ou `$`) e ainda não fecha.
**Não escrever esses números na conta dela sem ela ver.** O caminho certo é a tela
📲 Importar do WhatsApp, que mostra a lista para ela desmarcar — ou eu apresento carro a carro.

**Padrão dos nomes de grupo:** `[Sold/LV/TX] Modelo Ano Cor PLACA Cliente`.

### 06/09 — gastos dos 9 grupos do WhatsApp lançados

**As 3 regras que fizeram a extração fechar** (a Joice explicou a causa: o Geraldo posta o
ORÇAMENTO para saber o valor e depois posta de novo quando PAGA):

1. **Só é dinheiro se tiver centavos ou `$`** — senão endereço vira gasto
   (`7201 N General Bruce Dr` → $7.201).
2. **Descrição com `total|saldo|custo|soma|acumulad|resumo|balanço|falta|gastos` é SOMA, não
   despesa.** Era a maior fonte de erro: `14.654,10 custo total` entrava como gasto.
3. **De-duplicar por (valor + descrição), guardando a primeira** — resolve orçamento→pagamento
   e as reconferências. O `bid` de $6.800 do Motorhome aparecia 7 vezes.

**Benchmark:** comparar com o ÚLTIMO total declarado no grupo, **com data** — o total antigo
não cobre os gastos posteriores. Ex.: Outlander 16 fecha $11.686 em dez/23, mas o grupo segue
até 2026 (transmissão $3.800 + $2.400). Depois das regras a soma ficou levemente ABAIXO do
total do Geraldo em quase todos — lado seguro.

**Lançado:** 400+ gastos em 9 veículos. Depois tirei a linha `lote`/`bid` dos gastos de 6
carros porque já estava no **Valor de compra** (senão a compra contava duas vezes).
No Smurf, a linha `COMPRA $10.000` virou `valorCompra`.

**Deixadas de fora de propósito — podem ser dinheiro que ENTROU, não gasto:**
Outlander 16: Aluguel $320 · Deposito Rosalinda $250 · Deposito pago Romulo $250 ·
pago $40 · aluguel $300 · deposito $250 · cash do aluguel $50 · diferenca week e deposito $50.
Outlander 17: Deposito Mauricio $300 · Pago deposito $250 · crédito Luiz MTY $482 ·
pago $300 · Pago $108 · Pago $160 · pago $10 · troca de oleo cliente $80.
**São candidatas a RECEITA DE ALUGUEL — perguntar a ela.**

**Investido hoje nos veículos do Texas** (compra + gastos): Outlander 16 $19.102 ·
Smurf $16.875 · Motorhome $13.689 · Ram Van $8.069 · Bruto Keystone $7.705 ·
Trailer Ovo $6.968 · Corvette $4.876 · F150 $2.805.

Backup: `_backups/backup_DEPOIS_DOS_GRUPOS_TX.json`. localStorage em 1,88 MB de ~5 MB.

### 06/09 — o menu que sumia (era overflow, não o modal)

**Causa real:** a tabela de 11 colunas esticava a página além da janela; o `.main-content`
era `flex:1` **sem `min-width:0`**, então o flex não deixava encolher e empurrava a
`.sidebar` para fora. Ela via "a lateral some", e o Chrome dela não está maximizado.

**Correção (CSS):** `.sidebar` com `flex:0 0 250px; position:sticky; left:0` ·
`.main-content` com `min-width:0; overflow-x:hidden` · `.card,.module` com `overflow-x:auto`
(tabela rola dentro do quadro) · `html,body { overflow-x:hidden }` ·
`.modal-content` com `max-width:min(700px, calc(100vw - 32px))` ·
e `@media (min-width:900px){ .modal { left:250px; width:calc(100% - 250px) } }` —
**o cartão do carro abre AO LADO do menu**, então o menu nunca mais some.

Conferido por código: página não estica, menu na tela e não coberto com o carro aberto.

### ECONOMIA DE USO — a Joice está gastando rápido demais

O que mais custa, em ordem:
1. **Conversa longa.** Cada mensagem reprocessa o histórico inteiro. Esta sessão ficou enorme.
   **Assunto novo = conversa nova**, anexando este RESUMO. É de longe a maior economia.
2. **Print/foto.** Uma imagem custa muito mais que texto. Pedir a ela o texto do erro quando der.
3. **Ida e volta.** Perguntar tudo de uma vez em vez de confirmar a cada passo.

Do meu lado: menos perguntas de confirmação, agrupar as mudanças e publicar uma vez só,
`get_page_text`/JS em vez de screenshot, e não reler arquivo que já li.

### 07/09 — rede de segurança dos dados + vitrine no ar

**1. Backup automático (publicado, commit `577997d`).** O sistema agora baixa **sozinho uma
cópia por dia** na pasta `Downloads`, na primeira vez que ela salva algo no dia (é um clique
dela, então o Chrome não bloqueia o download). Funções novas: `baixarBackupArquivo(prefixo)`,
`backupAutomatico()`, `mostrarUltimoBackup()`, chave `jgpazotto_ultimo_backup`.
Aviso verde flutuante `#avisoBackup` e a data da última cópia (`#ultimoBackup`) na aba Backup,
em vermelho se passou de 3 dias.
- `makeBackup()` trocou `data:` URI por **Blob** — o data URI engasgava com ~2 MB.
- O caminho automático **não tem `alert()`** (só o botão manual tem), então não congela a automação.

**2. Vitrine de anúncios NO AR — jgpazotto.com/anuncios.html** (commit `39bb21e`).
Era só isto que faltava: **nada tinha sido exportado ainda**. O pipeline inteiro rodou pela
primeira vez e funciona. Publicado: `anuncios.json`, `dados/anuncios.json` e
`imagens/anuncios/v-001-*.jpg`.
- Primeiro veículo: **Lincoln MKZ Hybrid 2014 XZL6150**, 6 fotos, marca d'água conferida
  (brasão dourado + jgpazotto.com no canto). Sem preço → o site mostra **"Sob consulta"**,
  escolha dela.
- **Correção no gerador:** `preco: num(a.preco) || undefined` — preço 0 ia para o site e
  virava "$ 0,00". Agora some do JSON e o site cai no "Sob consulta" que já existia.
- **Como gerar sem travar:** NÃO chamar `gerarArquivoAnuncios()` (tem `alert()` no fim).
  Repetir o miolo por JS: `montarAnuncios()` → `texto2bytes` → `encolherFoto` →
  `base642bytes` → `fazerZip` → link.click(). O zip cai em `~/Downloads`.
- **`~/Downloads` está conectada** nesta sessão — dá para pegar o zip e os backups direto.

**Estado da vitrine hoje:** dos 56 carros, só **1 está marcado "Disponível"**, só 1 tem foto
e **nenhum tem preço de anúncio**. Candidatos naturais: 6 em GARAGEM + 8 no TX (esses já têm
`valorCompra`). O trabalho dela é: marcar Disponível, tirar foto, pôr preço. O texto do
anúncio eu escrevo.

**3. Supabase — em andamento.** Ela escolheu ser guiada passo a passo. A página
`supabase.com/dashboard/sign-up` foi aberta no Chrome dela; o caminho é **"Continue with
GitHub"** (ela já tem a conta `jgpazotto`). ⚠️ **Criar conta e digitar senha é ela** — eu não
faço. Depois de entrar: criar o projeto → pegar Project URL + chave `anon public` → aí a
migração é toda minha (trocar `saveData()`/`loadData()`, `supabase.auth` no lugar do login falso).

⚠️ **Dois Chrome ligados na conta dela.** `tabs_context_mcp` recusa até escolher. `switch_browser`
respondeu "no other browsers available" e o segundo caiu sozinho — se acontecer de novo,
perguntar a ela e usar `select_browser`.

### 07/09 — SUPABASE FUNCIONANDO: login de verdade e dados no banco ✅

**O projeto já existia** (`JG Pazotto`, ref `dobppztwphbppffoknkx`, org `fifaoptnueehlcujnmex`),
só estava **pausado** pelo plano grátis. Reativado — "Restoration complete".
⚠️ Na mesma org existem `Organizador` (o projeto Postou) e `karpalm`: **não mexer neles**.

**Dados do projeto**
- URL: `https://dobppztwphbppffoknkx.supabase.co`
- Chave publishable: `sb_publishable_RMYz2IvXYBMC_XXzetTXNA_2C7kwQks`
  ⚠️ A tela de API Keys **mostra a chave cortada** no texto da página. Ler pelo DOM
  (`input.value`), senão dá "Invalid API key". Foi o erro que eu cometi.
- Usuário: `jgpazotto@gmail.com` — **a senha é dela, eu nunca vi**. Criada por ela no
  dashboard (Authentication → Add user → Create new user, com "Auto confirm" ligado).

**Banco**
```sql
create table public.dados (id text primary key, conteudo jsonb, atualizado_em timestamptz, atualizado_por text);
-- RLS ligado; policies p_ler/p_criar/p_mudar, todas "to authenticated using (true)"
revoke all on table public.dados from anon;
grant select, insert, update on table public.dados to authenticated;
```
Uma linha só, `id = 'jgpazotto'` — a empresa inteira. **Conferido por código:** sem login,
ler/escrever/alterar devolvem *permission denied for table dados*.

**No dashboard (v3.6)**
- `<script src=".../supabase-js@2.45.4/dist/umd/supabase.min.js">` + `SB_URL`/`SB_KEY`/`SB_LINHA`.
- `handleLogin()` usa `sb.auth.signInWithPassword`. **`admin`/`joice123` não existe mais.**
- `entrarNoSistema()` → `loadData()` (mostra o local na hora) → `sincronizarNaEntrada()`.
- `sincronizarNaEntrada()`: **nunca apaga dado bom com dado vazio.** Compara `pesoDosDados()`
  (nº de carros+imóveis+clientes+financeiro); banco vazio → sobe o local; local vazio → baixa;
  empate → o mais recente. `gravarNoBanco(false)` junta alterações por 4 s; grava também no
  `visibilitychange`; `beforeunload` avisa se ainda falta gravar.
- Indicador `#statusBanco` no canto ("Salvando... / ✓ Salvo no banco / ⚠️ só neste computador").
- O init agora depende da **sessão do Supabase**, não do sinalzinho no localStorage.

**Publicado em `dashboard-v3.6.html` DE PROPÓSITO** — o `dashboard-v3.5.html` continua no ar
com o login antigo, como rede de segurança. Só trocar o endereço oficial depois que ela
confirmar (ela confirmou que entrou: *"entrou sim, agora com senha, ficou lindo"*).
Backup de antes: `_backups/backup_ANTES_DO_SUPABASE_2026-09-07.json` (sha256 conferido,
idêntico ao localStorage: `e6ae8b1a...`).

**Truques do dashboard do Supabase (para não perder tempo de novo)**
- O editor SQL é Monaco: escrever com `monaco.editor.getModels()[0].setValue(sql)` em vez de
  digitar (o auto-fecha-parêntese estraga o texto). Clicar na linha 1 uma vez antes, para o
  editor existir. `Run` fica em cima à direita; `drop policy` dispara um aviso "destructive".
- `/api/pg-meta/<ref>/query` **não** existe (404). Usar o editor mesmo.
- Navegar para fora do editor com alteração não salva é bloqueado ("Leave site?") — abrir
  aba nova em vez de forçar.

### ⚠️ 07/09 — O PROBLEMA QUE A ÁREA DE FUNCIONÁRIOS DESTAPA

A Joice pediu área de funcionários **com permissão diferente para cada um** (só ela e o
Geraldo com acesso total). Decisão dela + minha recomendação: **ela cadastra e autoriza**;
o funcionário só cria a própria senha ("Primeiro acesso"). Cadastro aberto, não.

**Mas hoje TODO o sistema é UMA linha jsonb.** Quem consegue ler a linha lê tudo — inclusive
Financeiro. Então esconder menu é enfeite, não segurança. Para permissão de verdade é preciso
**quebrar a linha única em uma linha por módulo** (`carros`, `clientes`, `financeiro`, ...) e
pôr a permissão na RLS. Bônus grande: salvar deixa de mandar 2 MB a cada alteração.

### 07/09 — PERMISSÃO DE VERDADE: dados separados por área ✅ (v3.7)

**A decisão dela:** *ela* cadastra e autoriza; ninguém pede o próprio cadastro (o endereço é
público). O funcionário só **cria a própria senha** — ela nunca sabe a senha de ninguém.
Cargos que ela pediu: Vendedor, Aluguel/imóveis, Cobrança e **família (filhos): vê tudo,
não edita valores**.

**A descoberta que mudou o desenho:** medindo os dados, **1650 KB dos 1925 KB são as 6 fotos
de UM carro**. A ficha dos 56 carros inteira dá ~21 KB; o dinheiro, ~194 KB. E o dinheiro
(carnê, valorVenda, balanço, gastos) mora **dentro** do objeto do carro — então separar só
por chave de topo NÃO esconderia nada do mecânico.

**Áreas na tabela `public.areas`** (uma linha por área, `conteudo jsonb`):
`carros` (ficha) 21 KB · `carros_dinheiro` 194 KB · `fotos` (fotos+vistoria) 1669 KB ·
`clientes` · `fornecedores` · `imoveis` · `aluguel` · `financeiro`.
Campos que vão para `carros_dinheiro`: gastosLista, pagamentos, balanco, totalGastos,
totalRecebidos, saldo, carnes, debitos, valorVenda, entrada, valorCompra, anuncio,
fichaAnteriorLocacao, gastosDaPlanilhaAntiga. Para `fotos`: fotos, vistoria.

**Tabela `public.pessoas`**: email (PK), nome, papel, permissoes jsonb, ativo.
Funções `public.perm(area)` e `public.sou_dono()` — ambas SECURITY DEFINER (por isso a policy
de `pessoas` pode consultar `pessoas` sem recursão). Policies de `areas` leem `perm(area)`:
select se `ver|editar`, insert/update só se `editar`. `anon` sem nenhum grant.

**MIGRAÇÃO CONFERIDA ITEM POR ITEM.** Remontei os carros a partir das áreas e comparei com o
original: **56 de 56 idênticos**, clientes/imóveis/aluguel/financeiro idênticos, fotos intactas.
⚠️ Comparar com normalização profunda — **o jsonb do Postgres reordena as chaves**, então
`JSON.stringify` direto acusa diferença falsa.
A linha antiga `dados` (bloco único) **continua lá de propósito**, como rede.

**PROVA DE QUE A PERMISSÃO É REAL** (rodado no editor SQL):
```sql
begin;
select set_config('request.jwt.claims','{"email":"...","role":"authenticated"}', true);
set local role authenticated;
select area from public.areas;   -- devolve SÓ o que a pessoa pode
rollback;
```
Um "Teste Oficina" com `{"carros":"editar","fotos":"editar"}` pediu tudo e recebeu **2 linhas:
carros e fotos**. Financeiro, carros_dinheiro, clientes e imóveis simplesmente não vieram.
O update no `carros_dinheiro` alcançou **0 linhas**. Teste apagado depois; dados conferidos
intactos (56 carros, 23 carnês, 19 clientes, 11 imóveis).

**No sistema (v3.7)**
- `carregarPermissoes()` lê a linha da pessoa; `EU`, `MINHAS`, `souDono()`, `podeVer/podeEditar`.
- Quem **não está em `pessoas`** entra no Auth mas é deslogado na hora com recado — conta
  criada por conta própria não vê nada.
- `separarEmAreas()` / `juntarAreas()`; `gravarNoBanco()` manda **só a área que mudou e que a
  pessoa pode editar** (não são mais 2 MB por gravação).
- `aplicarPermissoesNaTela()` esconde menu por área; classe `body.so-olhar` some com os botões
  que gravam (para os filhos).
- Tela **🧑‍💼 Funcionários** (só dono) com grade nada/só olha/pode mexer por área e modelos
  de cargo prontos (`PAPEIS`). Link **"Criar minha senha"** no login → `sb.auth.signUp`.

⚠️ **Erro meu, para não repetir:** publiquei uma versão com `escapaHtml` duplicado. Ele já
existia no arquivo como `const escapaHtml = s => ...` — meu `grep "function escapaHtml"` não
achou. **Procurar também por `const NOME =` antes de criar função.** Corrigido em `4a791fb`.
Outro: os modais deste sistema abrem com `classList.add('active')`, não `style.display`.

**Endereços hoje:** v3.5 (login antigo) · v3.6 (Supabase, bloco único) · **v3.7 (o bom)**.
Falta combinar com ela juntar tudo num endereço só.

### O QUE FALTA AGORA
1. **Geraldo como dono** — ela cadastra em Funcionários e ele cria a senha.
2. Ela testar a tela de Funcionários de verdade (cadastrar alguém e ver a pessoa entrar).
3. **Fotos para o Supabase Storage** — hoje ainda são base64 dentro do jsonb (1,6 MB).
   Resolve de vez o peso e libera fotos à vontade.
4. Unificar o endereço (v3.7 virar o oficial; v3.5/v3.6 redirecionarem).
5. Encher a vitrine (marcar Disponível + foto + preço) · 16 linhas de aluguel/depósito ·
   8 carnês em aberto.

### 07/09 — o que a gente sabia na mão virou código (tela do WhatsApp)

**O diagnóstico:** as regras de de-duplicação estavam escritas no RESUMO e eu as aplicava
**manualmente** ao processar os grupos. A tela `📲 Importar do WhatsApp` nunca aprendeu —
por isso a Joice viu "muita coisa dobrada". Agora está no software.

**Regras dentro da tela** (constantes ao lado das que já existiam):
- `ZAP_SOMA` = `total|totais|saldo|custo|soma|somando|acumulad*|resumo|balanço|falta|gastos`
  → é **soma**, não despesa. Vem desmarcada, em aba própria.
- `ZAP_COMPRA` = `lote|bid|arremate|leilão|compra do carro` → é o **Valor de compra** da
  ficha; se entrar como gasto, a compra conta duas vezes.
- `ZAP_RECEITA` = `pago|paguei|pagou|depósito|crédito|aluguel|rent|cliente|recebi|recebido`
  → pode ser dinheiro que ENTROU. Nunca lanço como gasto sozinha.
- `agruparZap()` de-duplica por **(valor + descrição normalizada — minúscula, sem acento,
  só letras e números)**, guarda a **primeira** e conta as demais. Selo `🔁 N×` clicável
  mostra as datas.

**Tela nova:** abas *Gastos diferentes · Repetidas · Compra do carro · Somas e totais ·
Pode ser recebimento · Tudo*, com explicação em português em cada uma, contador do que está
marcado e botão "↩️ Voltar ao que eu sugeri".
**Conferidor automático:** pega o MAIOR valor entre as linhas de soma (o total que o próprio
Geraldo escreveu) e compara com o que está marcado — **fica vermelho se passar de 15% acima**.

**Medido em conversas reais** (teste em node reaproveitando o código do arquivo — ver abaixo):

| conversa | antes | depois | total escrito no grupo |
|---|---|---|---|
| F150 clássico | $23.486 (181 linhas) | **$3.249** (50 gastos) | $611 · "bid e taxas $880" repetia **12×** |
| Bruto Keystone | $30.113 | **$6.665** | $8.390 (RESUMO 06/09) — ficou abaixo, lado seguro |
| Outlander 16 | $37.161 | **$18.179** | $9.944 → a tela avisa em vermelho, ainda tem repetição |

**Como testar a extração sem abrir o navegador** (vale muito a pena, é rápido):
extrair de `dashboard-v3.7.html` o trecho de `const ZAP_CAB =` até `let zapFiltro =`,
colar num arquivo com stubs de `fmt()` e `mostrarZap()`, e rodar
`node zt.js "<conversa>.txt"`. Os `.txt` e os `.zip` das conversas estão em `~/Downloads`.

### 07/09 — o logo: "JG" aparece duas vezes
O brasão (`imagens/brasao-jg.png`) tem **JG** gravado no escudo, e o `<span class="marca-nome">`
ao lado escreve **JG Pazotto** — lê-se "JG · JG Pazotto". Fica no `<header>` do `index.html`
(linha ~489), repetido em `anuncios.html` e `nossa-historia.html`.
Mandei a ela 4 opções renderizadas com a arte real (brasão + Pazotto · com linha de apoio ·
só o brasão · só o nome). **Esperando ela escolher** — é decisão de criação, é a área dela.
⚠️ Chrome dela **não abre `file://`** pela automação; para mostrar comparação visual, montar
HTML com a imagem em data-URI e mandar por `SendUserFile`.

### 07/09 — pedido dela: fotos dos carros direto do WhatsApp
As fotos dos carros já estão nos grupos. Ela quer que a importação traga as fotos junto.
**Ordem certa:** primeiro **Supabase Storage** (hoje 6 fotos de um carro = 1,6 MB de base64
dentro do jsonb), depois ler o `.zip` exportado **com mídia**. O `.zip` dá para abrir no
navegador com `DecompressionStream('deflate-raw')` — o código já tem um *escritor* de zip
(`fazerZip`), falta o leitor. Os zips com mídia dela já estão em `~/Downloads`.

### 07/09 — logo resolvido: o certo já estava na pasta

**Não era decisão de criação, era arquivo errado.** O site montava o logo na mão —
`imagens/brasao-jg.png` (só o escudo, que já tem **JG** dentro) + `<span class="marca-nome">JG
Pazotto</span>`. Lia-se *JG · JG Pazotto*.
**O logo oficial é `imagens/logo-jg.png`** (900×267, fundo transparente): brasão + **PAZOTTO**.
Estava na pasta e não estava sendo usado. Ela mandou as artes confirmando.

Trocado em `index.html`, `anuncios.html`, `nossa-historia.html` (o `<picture>` inteiro virou
uma imagem só). Gerei `imagens/logo-jg.webp` com Pillow (57 KB no lugar de 115 KB).
Altura no CSS: **58px** no computador, 40px no celular (o logo é deitado, 3,37:1 — a régua do
CSS é a altura, então o valor do escudo quadrado não servia).
O `favicon` continua com `brasao-jg.png` de propósito: escudo sozinho é o certo para ícone.
Commits `b0ac655` e `d28f8e1`.

⚠️ **Lição:** antes de propor alternativas de design, **procurar o arquivo na pasta**
(`find . -iname "*logo*"`). Eu montei 4 opções de lockup quando bastava usar a arte que ela
já tinha. Há mais artes em `Imagens /` (com espaço no nome): logo-header, jg-pazotto-logo,
Logo topo, logo_JG_300.

**Sobre as fotos (recado dela):** ela vai subir as fotos **do próprio WhatsApp**, porque o
WhatsApp já reduz o tamanho. Ou seja, não precisa do leitor de zip agora — precisa do
**Supabase Storage**, senão 56 carros × 6 fotos não cabem no jsonb nem no localStorage.

### 07/09 — A LIÇÃO MAIS IMPORTANTE ATÉ AGORA: nem tudo no grupo é gasto do carro

A Joice explicou o negócio dela e isso mudou o desenho da importação. No grupo do WhatsApp
convivem **oito naturezas** de dinheiro, e a tela tratava tudo como "gasto do carro" —
por isso a multa do inquilino virava prejuízo do carro.

| natureza | o que é (palavras dela) | onde cai ao gravar |
|---|---|---|
| 🔧 gasto | peça, funilaria, óleo | `c.gastosLista` |
| 🏢 jg | manutenção que a JG assume, nunca vai ao cliente | `gastosLista` + `assumidoPelaJG` |
| 🎫 cobrar | **FasTrak, ticket, multa, licenciamento, dívida** — "temos que cobrar do cliente" | `c.debitos` → 🔔 Cobrança |
| 💥 dano | parabrisa quebrado, batida | `c.debitos` → 🔔 Cobrança |
| 🎁 desconto | **bônus de indicação $50** — "é só marcação, o cliente vai ter $50 de desconto na próxima semana" | `c.debitos` com valor **negativo** |
| 💵 recebido | depósito, aluguel, "Luiz pagou e está debitando do carro" | `c.pagamentos` |
| 🤝 fornecedor | acerto com o **Luiz, que é o mecânico deles** (parte em dinheiro, parte descontada em serviço) | `gastosLista` + `fornecedor` |
| 🚫 nada | soma, total, repetida, preço de compra | não grava |

**"De quem cobrar" — decisão dela:** cadastrar **os períodos de locação**. Aba nova na ficha
do carro **🔑 Quem ficou com o carro**: `c.locacoes = [{cliente, tel, de, ate, obs}]` (datas
ISO). `clienteNaData(carro, iso)` acha quem estava com o carro naquele dia; se não achar,
`donoDaLinha()` procura o **primeiro nome** de algum cliente escrito na mensagem.
Cada linha achada agora carrega `iso` (AAAA-MM-DD) — foi preciso guardar isso em `acharGastosZap`.

**Correção na Cobrança:** `c.debitos` ganhou `cliente`, `tel`, `iso` e `natureza`, e
`displayCobranca` usa `d.cliente || clienteNaData(...) || dono do carnê`. Antes jogava **todo
débito no dono do carnê** — a multa de um inquilino caía no colo de outra pessoa.

**Duas regras minhas estavam gulosas (achado testando, não no navegador):**
`vidro` pegava "calhas vidro" (peça) e `gasolina|tanque` pegavam abastecimento normal —
21 linhas viraram "dano" no Outlander. Agora `ZAP_DANO` é só
`parabrisa|para-brisa|batida|amassad|quebrad|dano|arranh`. Gasolina, limpeza, lavagem,
aspirar, Lyft/Uber ficam como **gasto** com um aviso amarelo na linha
(`ZAP_TALVEZ_CLIENTE`) — "costuma ser do inquilino, confira". **Não decido por ela.**

**Medido no C-MAX AZUL 9DHW447** (o carro que ela estava olhando), depois das 8 naturezas:
cobrar **$1.750** (14 linhas de FasTrak/ticket) · dano **$100** (parabrisa) ·
desconto **$300** (5 bônus) · recebido **$7.510** (12 linhas) · gasto $19.643.
Ou seja, **~$9.660 que iriam para "gasto do carro" não eram gasto do carro.**
Publicado em `173e010`.

⚠️ **As fotos:** todos os zips que ela tem foram exportados **SEM mídia** — o `_chat.txt` do
Outlander tem **337 "imagem ocultada"**, mas nenhum arquivo de imagem no zip. Para as fotos
entrarem (ela quer, e são a prova da multa/dano), ela precisa exportar **Com mídia**.
Ela disse que vai subir as fotos do próprio WhatsApp porque ele já reduz o tamanho.

### O QUE FALTA (atualizado 07/09, fim do dia)
1. Ela cadastrar os **períodos de locação** dos carros alugados — sem isso a cobrança não
   sabe de quem é. É o gargalo do resto.
2. **Supabase Storage** para as fotos.
3. Mostrar, ao lado de cada linha do WhatsApp, **quantas fotos** vieram junto naquele momento
   (dá para ler do `_chat.txt` mesmo sem mídia: contar "imagem ocultada" perto da mensagem).
   Ela pediu isso — é o que deixa ela decidir se "Funilaria 2500" e "funileiro 2500" (3 semanas
   depois) são o mesmo serviço ou dois.
4. De-duplicação **por palavra parecida**, não só igual: "Funilaria" ≠ "funileiro" hoje.
5. Geraldo como dono · testar Funcionários · unificar o endereço · encher a vitrine.

---

## 📸 07/09 (fim do dia) — A EXPORTAÇÃO COM MÍDIA FUNCIONA. Comece por aqui.

Ela conseguiu conectar a pasta (achou que não tinha conseguido, mas conseguiu):
`~/Documents/jgpazotto-v2.0/Whatsapp/WhatsApp Chat - Total Loss Blue 10`

**O que tem lá:** 357 arquivos — **342 fotos, 7 vídeos, 106 MB** — e o `_chat.txt`.
É o grupo do **C-MAX AZUL 9DHW447**, o mesmo carro que ela estava revisando.

**Como o texto liga a foto à mensagem** (é simples, e é a chave de tudo):
```
[7/25/22, 3:39:29 PM] Geraldo Pazotto EUA: <anexado: 00000006-PHOTO-2022-07-25-15-39-29.jpg>
```
O nome do arquivo está escrito na própria linha, com a hora exata. Basta ler o `_chat.txt`,
guardar a posição de cada `<anexado: ...>` e casar com a posição das linhas de dinheiro.

**Medido de verdade** (script em `/tmp/zt3.js`, receita abaixo):
- 356 fotos anexadas citadas no texto
- 288 linhas com dinheiro
- **136 delas (47%) têm foto a até 6 mensagens de distância**

**Por que isso importa:** ela disse *"seria importante olhar as imagens para ver se são outras
pq geralmente colocamos fotos"*. Com a miniatura ao lado da linha, ela resolve de bater o olho
o caso "Funilaria $2.500 (3 ago)" × "funileiro $2.500 (24 ago)" — mesmo serviço ou dois?

**Plano para amanhã, na ordem:**
1. Aceitar uma **pasta ou um zip com mídia** na tela 📲 Importar do WhatsApp (hoje só aceita
   `.txt`). No navegador dá para ler pasta com `<input type="file" webkitdirectory>` — mais
   simples que descompactar zip, e ela já sabe conectar pasta.
2. Mostrar a **miniatura** das fotos próximas de cada linha, com lupa para ampliar.
3. Só as fotos que ela escolher vão para o **Supabase Storage** (106 MB não cabem no jsonb
   nem no localStorage — isso já foi medido e é limite duro).
4. De-duplicação por **palavra parecida**: normalizar radical (funilaria/funileiro),
   ou distância de edição, ou "mesmo valor + até 30 dias" como sinal amarelo.

**Receita do teste sem navegador** (usei muito hoje, vale a pena):
```bash
# extrai o miolo da importação do HTML e roda contra uma conversa de verdade
python3 - <<'PY'
import io
s = io.open('dashboard-v3.7.html', encoding='utf-8').read()
ini = s.index('const ZAP_CAB ='); fim = s.index('    function carroDoZap()')
io.open('/tmp/zt.js','w',encoding='utf-8').write('''
const fs=require('fs'); let zapAchados=[]; const database={clientes:[],carros:[]};
function fmt(v){return '$ '+Number(v).toFixed(2);} function mostrarZap(){}
function clienteNaData(){return null;} function carroDoZap(){return null;}
''' + s[ini:fim] + '''
acharGastosZap(fs.readFileSync(process.argv[2],'utf8')); agruparZap();
const t={}; zapAchados.filter(a=>!a.repetida).forEach(a=>t[a.tipo]=(t[a.tipo]||0)+1);
console.log(JSON.stringify(t));
''')
PY
node /tmp/zt.js "$HOME/mnt/Downloads/F150 - calssico.txt"
```
Conversas para testar: `~/Downloads/*.txt` e os `WhatsApp Chat - *.zip` (esses **sem** mídia).

## 🧾 Estado dos arquivos publicados em 07/09
| arquivo | o que é |
|---|---|
| `dashboard-v3.7.html` | **o bom** — Supabase, permissões por área, 8 naturezas, locações |
| `dashboard-v3.6.html` | Supabase com bloco único de dados (rede de segurança) |
| `dashboard-v3.5.html` | login antigo `admin`/`joice123` (rede de segurança) |
| `index/anuncios/nossa-historia.html` | site com o logo certo |
| `anuncios.json`, `dados/anuncios.json`, `imagens/anuncios/` | a vitrine |
| `imagens/logo-jg.png` e `.webp` | o logo oficial |

Commits do dia: `577997d` backup automático · `39bb21e` vitrine · `4865f7b`/`ba8e4da` v3.6
Supabase · `4a791fb` v3.7 permissões · `55252f5` WhatsApp agrupado · `b0ac655`/`d28f8e1` logo ·
`173e010` as 8 naturezas.

**Backups em `_backups/`:** `backup_ANTES_DO_SUPABASE_2026-09-07.json` (sha256 conferido,
idêntico ao localStorage dela antes da migração) · `backup_DEPOIS_DOS_GRUPOS_TX.json` ·
`backup_ANTES_DE_JUNTAR_FICHAS.json` · `backup_2026-09-04.json`.


---

## 📸 08/09/2026 — AS FOTOS ESTÃO NA TELA (commit `ed0442a`)

### 1. A tela de importação aceita a PASTA com mídia
`<input type="file" webkitdirectory directory multiple>` + `lerZapPasta(ev)`. Ela escolhe a pasta
que o WhatsApp criou ao exportar **Com mídia**; eu acho o `_chat.txt` sozinho e guardo todo o
resto em `zapArquivos = {nome: File}`. O botão do `.txt` continua lá (exportação sem mídia).

**Como a foto acha a linha:** em `acharGastosZap()`, depois de juntar as mensagens, cada
mensagem ganha `x.anexos` lendo `<anexado: NOME>` (iOS) e `NOME (arquivo anexado)` (Android).
`fotosPerto(k)` pega os anexos das mensagens de `k-2` a `k+6` (constantes `ZAP_ANTES`/`ZAP_DEPOIS`),
no máximo 8, e cada linha de dinheiro nasce com `fotos: [...]` e `fotosOk: []`.

**Medido na conversa real do C-MAX AZUL (`Whatsapp/WhatsApp Chat - Total Loss Blue 10`):**
214 linhas com dinheiro · **190 com foto do lado** · **0 nomes citados que não existem na pasta**.
A extração continua idêntica à de 07/09 na exportação sem mídia (`cm azul.txt`):
gasto $19.643 · recebido $7.511 · cobrar $1.750 · desconto $300 · dano $100. **Não regrediu nada.**

**Na tela:** `zapTirinha(a,i)` desenha as miniaturas embaixo da descrição.
**1 clique = guarda a foto junto com o lançamento** (borda verde) · **2 cliques = amplia**
(`zapVerFoto`, overlay `#zap-lupa`, fecha em qualquer clique; trata vídeo e PDF também).
Botão **📎 Guardar a 1ª foto de cada linha marcada** para não ter que clicar 100 vezes.
⚠️ `zapUrlDe(nome)` cria o `URL.createObjectURL` **uma vez por arquivo** e guarda em `zapUrls` —
`mostrarZap()` refaz o HTML inteiro a cada clique; criar URL dentro do render vaza memória.

### 2. De-duplicação por palavra parecida
`zapRadicais(obs)` = palavras com 5+ letras, sem acento, cortadas nos 5 primeiros caracteres
(funilaria → `funil`, funileiro → `funil`). `zapParecidas()` marca `a.parecida` quando:
**mesmo valor** + **radical em comum** + **até 120 dias** + **o radical aparece em no máximo 3
linhas** (esse último filtro é o que importa: sem ele, "troca" casava troca de óleo com
"trocar transmissão" e "trocar insulfilme" — 19 avisos, quase todos lixo; com ele, 8 linhas
= 4 pares, todos legítimos). **Eu só aviso em amarelo — não desmarco nada.** Quem decide é ela,
olhando a foto. Os 4 pares achados no C-MAX: Funilaria×funileiro $2.500 · Lampada freio×lampada
pisca $5 · Bonus Indicacao Mauricio 7jan × Bonus Indic Mauricio 20jan $50 · Acertando com Luiz
22fev × Acertar Luis MTY 27fev $875.

### 3. Endereço único
**`sistema.html` é o endereço oficial agora.** `dashboard-v3.5/3.6/3.7.html` viraram uma
página bonita com `location.replace('sistema.html')`. Os arquivos originais da v3.5 e v3.6 estão
em **`antigos/`** (sem underscore de propósito: o GitHub Pages ignora pasta `_alguma-coisa`
porque não existe `.nojekyll`). `area.html` (a portinha do cadeado no site) e `manifest.json`
apontavam para **dashboard-v3.5.html**, a versão do login `admin`/`joice123` — corrigidos.
Daqui pra frente **edite `sistema.html`**, não os dashboards.

### 4. ⏳ O que ficou faltando: o depósito das fotos (Supabase Storage)
O código de subir já está escrito e publicado (`SB_FOTOS = 'comprovantes'`, `subirFotoZap()`,
`verFotoGuardada()`, clipe 📎 nas abas Gastos e Débitos abrindo por *signed URL* de 1 h).
**Só falta criar o bucket.** Enquanto não existir, gravar funciona normalmente e as fotos
falham com um aviso amarelo — os lançamentos NÃO se perdem.

**SQL para rodar no editor do Supabase** (conferir antes `select public.perm('fotos');`):
```sql
insert into storage.buckets (id, name, public, file_size_limit)
values ('comprovantes','comprovantes', false, 26214400) on conflict (id) do nothing;

create policy comprovantes_ler on storage.objects for select to authenticated
  using (bucket_id = 'comprovantes' and public.perm('fotos') in ('ver','editar'));
create policy comprovantes_subir on storage.objects for insert to authenticated
  with check (bucket_id = 'comprovantes' and public.perm('fotos') = 'editar');
create policy comprovantes_mudar on storage.objects for update to authenticated
  using (bucket_id = 'comprovantes' and public.perm('fotos') = 'editar');
```

⚠️ **POR QUE NÃO DEU HOJE — anotar para não perder tempo de novo:** o Chrome dela estava
minimizado/em segundo plano. `document.visibilityState` ficou **`hidden`** e o painel do
Supabase (React) **não monta em aba escondida** — `monaco.editor.getModels()` volta vazio e
`document.body.innerText` volta `''`, mesmo com `readyState: complete` e 35 KB de HTML.
Abrir aba nova não resolve. **Peça a ela para trazer o Chrome para a frente antes de tentar.**

### Onde publicar / testar
- Publicar: continua o clone em `$HOME/pub` (o `.git` da pasta dela está travado por `HEAD.lock`).
  ⚠️ **É preciso `git config user.email/user.name` no clone** — o clone novo não herda identidade
  e o `git commit` falha com *"Author identity unknown"*.
- Testar a extração sem navegador: `~/w/zt.js` (mesma receita de 07/09, agora com stubs de
  `ZAP_ANTES`/`ZAP_DEPOIS`/`zapArquivos`). Rodar:
  `node ~/w/zt.js "<pasta>/_chat.txt" "<pasta>"` — o 2º argumento faz ele conferir se os nomes
  de foto citados no texto existem mesmo na pasta.
- Conferir sintaxe do arquivo inteiro: extrair o maior `<script>` com python e `node --check`.
  **Vale sempre**, o arquivo tem 535 KB e um erro de vírgula derruba o sistema todo.

### O QUE FALTA (atualizado 08/09)
1. **Criar o bucket `comprovantes`** (SQL acima) — com o Chrome na frente.
2. Ela cadastrar os **períodos de locação** (🔑 Quem ficou com o carro) — segue sendo o gargalo:
   é o que faz a cobrança saber de quem é cada multa.
3. **Geraldo como dono** em 🧑‍💼 Funcionários, e ela testar a tela cadastrando alguém.
4. Encher a vitrine (marcar Disponível + foto + preço) · 16 linhas de aluguel/depósito ·
   8 carnês em aberto.
5. Levar as fotos que ela escolher para dentro da ficha do carro (aba 📷 Fotos), não só no gasto.


---

## 🔧 08/09 parte 2 — os defeitos que ela achou, e o que ela pediu junto (commit `7b8cfd6`)

### O que estava errado (erro meu de desenho, não de digitação)
`mostrarZap()` reconstrói `#zap-resultado` inteiro. Eu chamava ele **em todo clique** —
inclusive no checkbox e na miniatura. Consequências que ela sentiu:
1. **A tela voltava ao topo** a cada marcação: ela perdia o lugar em 214 linhas.
2. **A lupa abria a foto errada:** eu tinha posto `onclick` (marcar) + `ondblclick` (ampliar) na
   mesma miniatura. O 1º clique redesenhava a lista, o elemento sob o cursor deixava de ser o
   mesmo, e o `ondblclick` caía noutra foto.

**Regra para não repetir: o que é conferência (marcar, escolher foto) atualiza só o pedaço;
só muda de natureza/valor/filtro é que redesenha a lista.**

### Como ficou
- `zapUsar(i, ok)` altera o dado e chama `zapAtualizarResumo()`, que reescreve **só**
  `#zap-abas` e `#zap-resumo` (fatorados em `zapHtmlAbas()` e `zapHtmlResumo()`).
- `zapAtualizarLinha(i)` troca por `outerHTML` **só** a tirinha `#zap-fotos-<i>`.
- `mostrarZap()`, quando precisa mesmo rodar, guarda `#zap-rolagem`.scrollTop e `window.scrollY`
  e devolve depois.
- **1 clique na foto = lupa** (`zapAbrirFoto`), sem `ondblclick` em lugar nenhum.
  Na lupa: setas `‹ ›` (e ← →), `Esc`/✕ para fechar, fecha clicando no fundo preto.

### Os 3 destinos da foto (pedido dela: "as fotos de anúncio também estão no WhatsApp")
Dentro da lupa ela escolhe para que serve a foto — `a.destino = {nomeArquivo: 'comp'|'vist'|'anun'}`:

| destino | onde cai | marca d'água |
|---|---|---|
| 📎 comprovante | Supabase Storage; só o caminho vai no lançamento (`fotos:[{nome,path}]`) | — |
| 🔧 vistoria/dano | `c.fotosVistoria = [{nome, dia, foto}]`, base64 encolhido a 1200px | **não** (é documento) |
| 📢 anúncio | `c.fotos` (base64 via `encolherFoto`), que é o que a vitrine exporta | **sim** |

⚠️ **`c.fotos` TEM que ser base64** — `gerarArquivoAnuncios` faz `dados: f` e mete no zip.
Caminho do Storage ali quebraria a vitrine. Por isso só o *comprovante* usa Storage.
`c.zapFotosUsadas = [nomes]` impede a mesma foto do grupo de entrar duas vezes.
`encolherSimples(dataUrl, max)` é o encolher **sem** marca (novo, ao lado de `encolherFoto`).

### "de tal data adiante" — não duplicar nas próximas importações
`c.zapUltimaData` guarda a data ISO mais nova gravada naquele grupo. Em `agruparZap()`,
`a.jaImportado = a.iso <= corte` → nasce **desmarcada**, some das abas por natureza, e ganha
aba própria **⏮ Já importadas antes** + aviso verde no topo com a data por extenso.
**Medido:** corte em 2024-01-01 no C-MAX marca 62 linhas e deixa **0 marcadas por engano**.

### Perda total (o C-MAX AZUL foi perda total, o seguro finalizou)
Campo **🚑 Perda total — o que o seguro pagou $** (`carro-indeniz` → `c.indenizacaoSeguro`),
card **Seguro (perda total)** no Balanço, e a conta virou
**Lucro = Recebidos + Seguro − (Compra + Gastos)**.
⚠️ **NÃO usar o id `carro-seguro`** — já existe e é a seguradora (`c.seg`). Quase caí nessa.
Novos campos registrados: `CAMPOS_DINHEIRO += indenizacaoSeguro, zapUltimaData` ·
`CAMPOS_PESADOS += fotosVistoria, zapFotosUsadas`.

### Como testei sem o Chrome dela (vale MUITO, repetir sempre)
`npm i jsdom` no container da nuvem, extrair de `sistema.html` o trecho de
`let zapAchados = [];` até `function lerComoDataUrl(f) {`, colar entre um `pre.js` (stubs de
`document` via JSDOM, `fmt`, `escapaHtml`, `database`, `clienteNaData`, `saveData`, `sb`) e um
`pos.js` com as asserções, concatenar num arquivo só e `node teste.js`.
⚠️ `eval()` não vale — `let` fica preso no escopo do eval. **Concatenar os arquivos.**
Resultado (tudo verdadeiro): 214 achados · lista e ids renderizam · desmarcar **não** troca o
elemento da lista · a lupa abre exatamente a foto pedida e com a legenda certa · setas andam ·
destino grava · ao fechar, só a tirinha da linha muda · corte marca 62 e erra 0.

### O QUE FALTA (atualizado 08/09, parte 2)
1. **Bucket `comprovantes` no Supabase** — SQL na seção anterior. **Pedir a ela para trazer o
   Chrome para a frente antes** (aba escondida não monta o painel). Sem ele, só o destino
   *comprovante* falha; **vistoria e anúncio já funcionam**, porque são base64 na própria ficha.
2. Períodos de locação (🔑 Quem ficou com o carro) — segue sendo o gargalo da cobrança.
3. Geraldo como dono em 🧑‍💼 Funcionários.
4. Encher a vitrine — agora ela pode mandar foto do WhatsApp direto para o anúncio.
5. Ela conferir se o balanço do C-MAX AZUL fecha depois de lançar a indenização do seguro.


## 📱 08/09 parte 3 — o celular (commit `b8678ad`)

Ela tentou entrar pelo iPhone: **o menu ocupava dois terços da tela e não dava para mexer.**

**A causa (armadilha de CSS):** já existia `@media (max-width:768px){ .sidebar{ width:150px } }`,
mas **não fazia efeito nenhum** — a regra de cima é `.sidebar{ width:250px; flex:0 0 250px }`,
e **dentro de um flex container o `flex-basis` manda mais que o `width`**. Numa tela de 390px
sobravam 140px para o conteúdo. **Lição: ao “corrigir” largura de item flex, mexer no `flex`,
não só no `width`.**

**Como ficou:** em `<=820px` o menu virou **gaveta** — `.sidebar` `position:fixed` com
`transform: translateX(-102%)`, abre com `body.menu-aberto`, fundo escuro `#fundo-menu`
(z-index 1100, gaveta 1200 — acima do `.modal`, que é 1000). Botão **☰** (`#btn-menu`) dentro
do `.header`, ✕ (`#btn-fecha-menu`) no topo da gaveta, e `switchModule()` chama `fecharMenu()`.

**Conferido com Playwright em 390×844** (chromium do container, `file://` do sistema, escondendo
o `#loginContainer` e mostrando o `#appContainer` por JS): conteúdo com 390px, **sem rolagem
lateral**, botão visível, gaveta abre com 290px e fundo escuro, e clicar num item fecha e troca
de módulo. Receita boa, repetir para qualquer mexida de layout — não depende do celular dela.
⚠️ `switchModule` usa o `event` global: chamar por `p.evaluate(()=>switchModule('carros'))` dá
`Cannot read properties of undefined (reading 'target')`. **Clicar no link de verdade** (`p.click`).

⚠️ **`<input webkitdirectory>` não funciona no Safari do iPhone** — escolher a *pasta* do
WhatsApp só dá no computador. No celular ela usa o `.txt` ou o 📸 da câmera. Dito a ela.


## 📱 08/09 parte 4 — o celular de verdade: a lista virou cartão (commit `a2ac5d0`)

A gaveta resolveu o menu, mas ela voltou: *"a tela pelo celular não está fácil de mexer, o
espaço é curto para muita informação, não dá para entrar na aba do veículo"*. Estava certa —
a tabela de **11 colunas** saía da tela e os botões de abrir o carro ficavam do lado de fora,
e os **12 filtros** ocupavam **7 fileiras** antes de a lista começar.

### A lista vira cartão (CSS, sem mexer em nenhuma tela)
Em `<=820px`, `.section > table` vira bloco: `thead` some, cada `tr` é um cartão com borda
dourada à esquerda, e cada `td` mostra **o nome da coluna à esquerda e o valor à direita**,
via `content: attr(data-rot)`. A 1ª célula (placa) é o título do cartão; a última (os botões)
ganha borda em cima, botões grandes e **texto** — `::after { content: ' Ver' }` e `' Abrir'` —
com a lixeira estreita (58px) para não clicar sem querer.

**Quem põe o `data-rot`:** `rotularTabelas()` lê o `<thead>` de cada tabela e escreve em cada
célula. Para não ter de chamar isso dentro de `displayCarros`, `displayClientes`, `displayImoveis`…
um **MutationObserver** em `#appContainer` (`childList: true, subtree: true`, debounce 60 ms)
reaplica a cada redesenho. ⚠️ **Observar só `childList`** — se observasse `attributes`, o próprio
`setAttribute` chamaria o observer de novo, em laço. Também marca `.cel-vazia` quando o valor é
vazio, `-` ou `—`, e o CSS esconde essas no cartão (menos ruído).

Isso serve para **todas** as listas do sistema de uma vez, e não muda nada no computador.

### Filtros e abas: uma fileira que rola
`.filtro-bar` e `.tabs` com `flex-wrap: nowrap; overflow-x: auto` (+ `flex: 0 0 auto` nos
botões e `::-webkit-scrollbar{display:none}`). 7 fileiras viraram 1 de 42px; as 11 abas da
ficha viraram 1 de 35px.

### Conferido em 390×844 (Playwright)
cartão 302px de largura e 389 de altura, **cabe na tela** · **sem rolagem lateral na página** ·
filtro 42px e rola de lado · ficha do carro abre com 351px e as abas rolam · botão "Abrir"
com 83×42px (alvo de toque bom).
⚠️ **Para testar uma lista é preciso ATIVAR o módulo antes** — `.module` sem `.active` fica
`display:none`, e tudo mede 0. Abrir a gaveta, clicar no link do menu e só então chamar
`displayCarros()` (a função de exibir não precisa de `event`; `switchModule` precisa).


## 👤 08/09 parte 5 — documento do cliente, quem responde pela batida, a conta da pessoa (`9c0694b`)

Ela reparou, olhando as fotos do grupo, que **tem foto que é documento do CARRO e tem foto que é
documento do CLIENTE** (viu uma CNH), e perguntou: *"clicando aqui já vai automático ou tenho que
salvar algo?"*

**Resposta que foi dada e agora está escrita na tela:** clicar na lupa só **marca**; quem grava é
o botão **💾 Gravar** no fim da lista. A lupa agora mostra em amarelo:
*"Isto só marca. Para valer, feche e clique em 💾 Gravar no fim da lista."*

### 4º destino: 📄 Documento do cliente
`ZAP_DEST.docli` (roxo `#6b3fa0`). Quando escolhido, a lupa abre um campo **"Documento de quem?"**
(`#zap-dono-doc`, datalist `lista-de-clientes`) já preenchido por `zapDonoDoc(a)` =
`a.docDe` → `a.cliente` → `clienteNaData(carro, a.iso)`. Ao gravar, vai para
`cliente.documentos = [{titulo, dia, iso, carro, placa, foto, origem}]` (base64 1400px, **sem**
marca d'água). Se a pessoa não existe, **crio a ficha** e aviso no relatório.
`mesmoNome()`/`nomeChave()` comparam nome sem acento/caixa, aceitando nome completo x primeiro nome.

### Regra nova: foto de ficha não precisa da linha
Antes, `gravarZap` só olhava fotos das linhas marcadas, e marcar uma foto marcava a linha —
o que criaria gasto que ela não quer. Agora: **anúncio, vistoria e documento valem sozinhos**;
só o **comprovante** exige a linha marcada (e só ele marca a linha sozinho).
A de-dup virou `zapFotosUsadas: 'destino|arquivo'`, para a mesma foto poder ser documento
**e** anúncio.

### Quem responde pela batida
Na Ficha do carro, ao lado da perda total: **💥 Data da batida** (`carro-databatida` →
`c.dataBatida`) e **💥 Quem era o responsável** (`carro-responsavel` → `c.responsavelBatida`).
`sugerirResponsavel()` olha `clienteNaData({...c, locacoes: cLocacoes}, data)` e preenche
sozinho, escrevendo embaixo quem estava com o carro naquele dia — ou avisando que faltam os
períodos de locação.

### A conta da pessoa (aba nova na ficha do cliente)
**🔑 Períodos e cobranças** (`#cli-conta`, montada por `resumoDoCliente(nome)`), varrendo
**todos** os carros:
- faixa vermelha se a pessoa é `responsavelBatida` de algum carro, com a data e o que o seguro pagou;
- 🔑 todos os períodos em que ela ficou com carro (carro, de, até, **contagem de dias**, obs);
- 🎫 só as multas/danos/descontos dela, com **total em aberto**;
- 💵 carnês e o que falta (reaproveita `carrosDoCliente`).
A aba **📷 Fotos/Docs** ganhou a lista dos documentos vindos do WhatsApp (miniatura, título,
data, de qual carro, lupa em `verDocGrande`).

### ⚠️ BUG SÉRIO CORRIGIDO NO CAMINHO
`saveCliente()` montava o objeto **do zero** — exatamente o mesmo erro que `saveCarro` tinha em
04/09. Qualquer campo que a tela não conhecesse era apagado ao salvar (os `documentos` sumiriam
no primeiro "Salvar Cliente"). Agora começa com `...anterior`.
**Procurar esse padrão nos outros save\*()**: imóvel, fornecedor, funcionário.

### Conferido com Playwright (dados de mentira, sem tocar nos dela)
sinistro aparece com o valor do seguro · período de 1 nov 24 → 22 jan 25 conta **82 dias** ·
só os débitos dela aparecem (o "Outro Fulano" não) · total em aberto $ 35,50 correto ·
documentos na ficha · 4 botões na lupa, com o campo "de quem?" e o aviso de gravar.
