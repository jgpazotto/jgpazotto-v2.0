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
