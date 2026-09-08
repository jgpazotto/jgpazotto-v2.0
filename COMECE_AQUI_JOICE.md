# Joice — o que está pronto e o que fazer agora

Um resumo curto, sem termo técnico. O arquivo grande é o `RESUMO_ONDE_PARAMOS.md`,
que é para a Claude ler.

---

## O sistema agora tem UM endereço só

**https://jgpazotto.com/sistema.html**

Guarde este nos favoritos e pode apagar os outros. Os endereços velhos (v3.5, v3.6, v3.7)
agora só levam para cá sozinhos. **Este endereço não muda mais**, mesmo quando eu melhorar
o sistema — chega de confusão de versão.

Entra com o seu **e-mail** e a **senha que você criou**.
Na primeira vez abra apertando **Cmd + Shift + R**.

---

## O que ficou pronto hoje (08/09)

### 📸 As fotos do WhatsApp aparecem ao lado de cada linha

Era o que você pediu. Agora, em **📲 Importar do WhatsApp**, clique em
**📁 Escolher a pasta (com fotos)** e escolha a pasta que o WhatsApp criou quando você
exportou **Com mídia** — aquela do C-MAX AZUL que você conseguiu conectar ontem.

Aí, embaixo de cada linha de dinheiro, aparecem as fotinhas que o Geraldo mandou **naquele
momento da conversa**. No C-MAX AZUL, **190 das 214 linhas têm foto do lado**.

- **1 clique na foto** = ela fica guardada junto com aquele gasto (a borda fica verde)
- **2 cliques** = a foto abre grande, para você olhar direito
- Tem um botão **📎 Guardar a 1ª foto de cada linha marcada**, para não ter que clicar tanto

### 🔎 "Funilaria" e "funileiro" agora se avisam

Aquele caso que você levantou. O sistema não olha mais só palavra igual — ele olha o
**começo da palavra**. Quando duas linhas têm **o mesmo valor** e uma **palavra parecida**
em até 4 meses, aparece um aviso amarelo perguntando se é o mesmo serviço ou dois.

No C-MAX AZUL ele achou 4 casos, e todos merecem seu olho:

- **Funilaria $2.500** (3 ago) × **funileiro $2.500** (24 ago)
- **Bonus Indicacao Mauricio $50** (7 jan) × **Bonus Indic Mauricio $50** (20 jan)
- **Acertando com Luiz $875** (22 fev) × **Acertar Luis MTY $875** (27 fev)
- Lampada freio $5 × lampada pisca trocada $5

**Eu não desmarquei nenhum.** Só avisei — agora você olha a foto e decide.

---

## Consertei o que você achou (parte da tarde)

**A tela não pula mais para o topo.** O defeito era meu: a lista inteira se redesenhava a cada
clique. Agora, quando você marca ou desmarca, só os números lá em cima mudam — você não perde
mais o lugar.

**E a lupa abre a foto certa.** Era o mesmo defeito: eu tinha posto "1 clique marca, 2 cliques
amplia", e entre um clique e outro a lista se redesenhava e o quadradinho já era outro.

**Agora é só 1 clique na foto** — ela abre grande. E é **dentro da foto grande** que você diz
para que ela serve:

- **📎 Comprovante deste lançamento** — fica presa ao gasto, como prova
- **🔧 Foto de vistoria / dano** — vai para a aba Vistoria do carro, **sem marca d'água**
  (é documento, não se marca)
- **📢 Foto para o anúncio** — vai direto para as fotos do carro, **já com a marca d'água**,
  pronta para o site

Use as **setas ‹ ›** (ou ← → no teclado) para passar as fotos daquela linha, e **Esc** para fechar.

## Não vai mais duplicar

Quando você gravar, eu anoto **até que data** já trouxe daquele grupo. Da próxima vez que você
mandar a mesma conversa, tudo que for daquela data para trás já vem **desmarcado**, num quadro
separado chamado "⏮ Já importadas antes" — e um aviso verde em cima diz até quando você já tinha
trazido. Era exatamente o que você pediu.

## Perda total do C-MAX AZUL

Na ficha do carro tem um campo novo: **🚑 Perda total — o que o seguro pagou $**.
Você põe ali o que o seguro indenizou e o Balanço passa a mostrar de verdade:

**Lucro = Recebidos + Seguro − (Compra + Gastos)**

Tem um quadro novo "Seguro (perda total)" ao lado de Compra, Gastos e Recebidos.

---

## Uma coisa ainda falta, e eu preciso de 30 segundos seus

As fotos que você escolher precisam de um **depósito** para morar (elas não cabem junto com
os dados — 342 fotos são 106 MB). O código de guardar já está pronto e no ar, mas eu preciso
criar esse depósito lá no Supabase, e **o seu Chrome estava minimizado** — o painel do
Supabase não abre numa aba escondida, então não consegui.

**É só deixar a janela do Chrome aberta na frente e me falar.** Eu faço em 1 minuto.

**Boa notícia:** isso só atrapalha o **📎 comprovante**. As fotos de **anúncio** e de
**vistoria** já funcionam agora, porque elas ficam guardadas na própria ficha do carro.
Ou seja: você já pode mandar foto do WhatsApp direto para o anúncio hoje.

---

## 🔑 O C-MAX AZUL virou o modelo — e o sistema aprendeu a ler sozinho

Li o grupo inteiro do C-MAX AZUL e descobri uma coisa que vale **para todos os carros**:
o Geraldo **renomeia o grupo com o nome de quem está com o carro** — "CMax 13 Blue 9DHW447
**Daniel**" — e tira o nome quando o carro volta. Ou seja, **a linha do tempo já estava escrita
lá**, em todos os grupos.

Então, em vez de preencher esse carro na mão, ensinei o sistema a ler isso. Na tela
📲 Importar do WhatsApp tem uma aba nova: **🔑 Quem ficou com o carro**. Ela já vem preenchida.

No C-MAX AZUL ele achou **10 períodos**, sozinho:

| quem | de | até |
|---|---|---|
| Plinio | 5 nov. 2022 | 10 fev. 2023 |
| Ivonne | 10 fev. 2023 | 11 abr. 2023 |
| Ivonne | 6 mai. 2023 | 31 jul. 2023 |
| Magda | 8 ago. 2023 | 2 out. 2023 |
| Julio | 22 out. 2023 | 4 mar. 2024 |
| Daniel | 18 mar. 2024 | 13 ago. 2024 |
| Izabella | 9 set. 2024 | 3 out. 2024 |
| Luis | 3 out. 2024 | 20 dez. 2024 *(o início eu não achei — confira)* |
| Wilmar | 16 jan. 2025 | 20 jan. 2025 |
| **Walter** | 22 jan. 2025 | 25 jan. 2025 |

E ele também percebeu a **perda total**: em 25 de janeiro o grupo virou "Total Loss", e quem
estava com o carro era o **Walter**. Aparece uma faixa vermelha com um botão que marca isso na
ficha do carro de uma vez.

**O que isso destrava:** testei aqui — depois de gravar os períodos, um FasTrak de 5 de abril
de 2024 passa a saber **sozinho** que é do Daniel. Era isso que estava faltando desde ontem.

**O que você faz, em cada carro, daqui pra frente:**

1. Exportar o grupo **Com mídia** e escolher a pasta na tela 📲 Importar
2. Aba **🔑 Quem ficou com o carro** → conferir as datas → **💾 Gravar**
3. Se aparecer a faixa vermelha de perda total → clicar em **marcar na ficha**
4. Voltar nas abas de dinheiro, olhar as fotos, marcar o destino de cada uma → **💾 Gravar**
5. Abrir a ficha de cada pessoa em **🔑 Períodos e cobranças** e conferir

**Uma coisa eu não lancei de propósito:** o valor que o seguro pagou pelo C-MAX. Vi o relatório
da Allstate numa foto pequena e não quero escrever número que não li direito. Me diz o valor e
eu ponho — ou você mesma põe no campo **🚑 Perda total** da ficha do carro.

---

## Respondendo a sua pergunta: clicar só MARCA

Quando você clica em "Comprovante", "Vistoria" ou "Anúncio" dentro da foto grande, eu só
**anoto** a sua escolha. **O que grava de verdade é o botão 💾 Gravar no fim da lista.**
Agora está escrito lá dentro, em amarelo, para você não ficar na dúvida.

## 📄 Documento do cliente — o quarto botão

Você tem razão: tem foto que é do carro e tem foto que é da pessoa (a CNH que você viu).
Agora, dentro da foto grande, tem um quarto botão: **📄 Documento do cliente**.

Ao clicar, aparece um campo **"Documento de quem?"** — e ele **já vem preenchido** com quem
estava com o carro naquela data (se você tiver cadastrado o período). A foto vai direto para a
**ficha da pessoa**, na aba 📷 Fotos/Docs, guardando de qual carro e de que dia ela veio.
Se a pessoa ainda não tiver ficha, eu crio e te aviso.

## 💥 Quem responde pela batida

Na ficha do carro, ao lado da perda total, tem agora **Data da batida** e **Quem era o
responsável**. Quando você põe a data, eu procuro quem estava com o carro naquele dia e
**preencho sozinha** — é para isso que servem os períodos de locação.

## 🔑 A conta de cada pessoa

Na ficha do cliente tem uma aba nova: **🔑 Períodos e cobranças**. Ali, num lugar só, aparece:

- um aviso vermelho se aquela pessoa é a **responsável por um sinistro**, com a data e quanto o seguro pagou
- **todos os períodos** em que ela ficou com carro — qual carro, de quando até quando, e **quantos dias**
- **as multas, pedágios e danos dela**, com o total em aberto
- os carnês e o que falta pagar

É exatamente o que você descreveu: a CNH na ficha dela, com as datas em que ficou com o carro
e as multas pelas quais ela responde.

---

## 📱 O celular ficou simples

**Cada carro virou um cartão.** Em vez daquela tabela larga que saía da tela, agora cada carro
é um quadro com a placa em cima e, embaixo, cada informação com o nome do lado:
Carro, Ano, Cor, Cliente, Gastos, Recebidos, Saldo, Status. O que estiver em branco nem aparece,
para não poluir.

**E os botões ficaram grandes, com nome:** **👁️ Ver** e **✏️ Abrir**. Agora dá para entrar na
ficha do veículo com o dedo, sem arrastar a tela de lado. A lixeira ficou estreita de propósito,
para você não apagar sem querer.

**Os filtros viraram uma fileira só.** Aqueles 12 botõezinhos (Comigo hoje, Alugados, No carnê,
Garagem…) ocupavam sete fileiras antes de a lista começar. Agora é uma fileira que você
**arrasta para o lado** com o dedo. As abas de dentro do carro (Ficha, Gastos, Fotos, Vistoria…)
funcionam do mesmo jeito.

Isso valeu para **todas as listas** do sistema — clientes, imóveis, carnês — não só a de carros.

## 📱 O menu

O menu tinha largura fixa e sobrava quase nada de tela. Agora, no celular, ele fica **escondido**
e você abre no botão **☰** no canto de cima. Ele fecha sozinho quando você escolhe uma tela,
e também dá para fechar no **✕** ou tocando fora.

Testei numa tela de tamanho de iPhone aqui: o conteúdo agora usa a largura toda e não precisa
mais arrastar a página de lado.

**Uma diferença que existe mesmo entre computador e celular:** escolher a **pasta** do WhatsApp
(aquela com as fotos) o iPhone não deixa — isso é limitação dele, não do sistema. Então:
**a importação com fotos você faz no computador**; no celular você usa o sistema normalmente,
inclusive o 📸 para tirar foto na hora.

## ⚠️ Abra com Cmd + Shift + R

O sistema mudou hoje duas vezes. Se a tela ainda estiver com o defeito antigo, é o navegador
mostrando a versão velha — **Cmd + Shift + R** resolve.

## Depois disso, na ordem

1. **Preencher quem ficou com cada carro e quando** (aba 🔑 Quem ficou com o carro).
   É isso que faz a cobrança saber de quem é cada multa. Continua sendo o que destrava o resto.
2. **Cadastrar o Geraldo** como dono, na tela de 🧑‍💼 Funcionários.
3. Encher a vitrine: marcar **Disponível**, pôr **foto** e **preço** nos carros.

---

## Se algo der errado

Suas cópias de segurança estão na pasta `_backups`. E as versões antigas do sistema não foram
apagadas — estão guardadas na pasta `antigos/`, caso um dia precise.

Para começar a conversa da próxima vez, é só anexar o `RESUMO_ONDE_PARAMOS.md` — está tudo lá.
