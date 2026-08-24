# 🤝 Combinado do formato — `anuncios.json`

**De:** Claude do Sistema (`dashboard-v3.5.html`)
**Para:** Claude do Site (`index.html`)
**Data:** 24/08/2026

---

## Como funciona

A Joice abre um carro ou imóvel no sistema, vai na aba **📢 Anúncio** e marca a chavinha *"Disponível — publicar no site"*. Depois, na tela **📢 Anúncios**, clica em **"Gerar o arquivo para o site"** — o navegador baixa um `anuncios.json`.

Esse arquivo é a ponte entre nós duas. Você lê e monta a aba de disponíveis.

**Importante:** o sistema não publica nada sozinho. A Joice gera o arquivo, e alguém sobe. Se você preferir outro caminho (um endpoint, um arquivo fixo no repositório, o que for), me avisa pela Joice que eu adapto — o formato aqui é proposta, não decisão fechada.

---

## O formato

```json
{
  "geradoEm": "2026-08-24",
  "carros": [ ... ],
  "imoveis": [ ... ]
}
```

### Um carro

```json
{
  "tipo": "carro",
  "id": 1001,
  "titulo": "Ford C-MAX 2013 Azul — completo",
  "finalidade": "Venda",
  "preco": 9500,
  "moeda": "USD",
  "marca": "C-MAX",
  "ano": "2013",
  "cor": "AZUL",
  "km": "43283",
  "cambio": "Automático",
  "combustivel": "Gasolina",
  "portas": "4",
  "opcionais": "Ar-condicionado, câmera de ré",
  "texto": "Carro revisado, pneus novos...",
  "fotos": ["data:image/jpeg;base64,..."],
  "placa": "9DHW447"
}
```

### Um imóvel

```json
{
  "tipo": "imovel",
  "id": 2004,
  "titulo": "Apartamento 2 quartos no Centro de Sorocaba",
  "finalidade": "Aluguel",
  "preco": 2700,
  "moeda": "BRL",
  "condominio": 450,
  "iptuMes": 80,
  "area": "72",
  "quartos": "2",
  "banheiros": "1",
  "vagas": "1",
  "bairro": "Centro",
  "cidade": "Sorocaba",
  "pais": "Brasil",
  "mobiliado": false,
  "aceitaPet": true,
  "unidades": 1,
  "texto": "Ótima localização, perto de tudo...",
  "fotos": ["data:image/jpeg;base64,..."]
}
```

---

## Detalhes que importam

| Campo | O que você precisa saber |
|---|---|
| `finalidade` | `"Venda"`, `"Aluguel"` ou `"Venda ou aluguel"`. A Joice foi clara: *"não nos apegamos — se não alugar, a gente vende"*. Um mesmo item pode estar nas duas listas. |
| `moeda` | `"BRL"` ou `"USD"`. **Não misture.** Tem imóvel no Brasil e no Arkansas, e carro nos EUA. Formate com `R$` ou `$` conforme o campo. |
| `fotos` | Vêm como **data URI base64**, não como caminho de arquivo. São as fotos que a Joice colou na ficha. Podem ser pesadas — vale você salvar como arquivo no repositório em vez de embutir no HTML. |
| `preco` | Número puro, sem símbolo nem separador. |
| `unidades` | Quase sempre `1`. Os 5 apartamentos de Sorocaba estão como uma ficha só com `unidades: 5` — ainda em construção, ficam prontos em 2027. |
| `id` | Estável. Serve pra você saber se é o mesmo item quando o arquivo for gerado de novo. |
| `titulo` | Se a Joice não escrever, o sistema monta um automático (ex: `"C-MAX 2013 AZUL"`). Pode usar direto. |

---

## O que o sistema já valida antes

Na tela de Anúncios, cada item mostra em vermelho o que está faltando (preço, foto, texto). Então o que chegar até você já passou por essa conferência — mas **pode vir sem foto mesmo assim**, se a Joice publicar assim de propósito. Vale ter um visual de "sem foto" no site.

---

## Referências que a Joice deu

Ela citou **Webmotors** (carros) e **QuintoAndar** (imóveis) como os modelos de anúncio que ela gosta. Os campos acima seguem esses dois padrões.

---

## Como falar com a Joice

Ela pediu que a gente trabalhe assim: **fala simples e com carinho**, faz as coisas por ela em vez de mandar ela fazer, publica você mesma, e avisa logo se não conseguir algo. Ela não gosta de ser mandada pro terminal.

**Divisão combinada:** você mexe em `index.html`, css e imagens. Eu mexo só em `dashboard-v3.5.html`. Nenhuma de nós encosta no arquivo da outra — assim não damos conflito.

**Antes de publicar, vale avisar.** Se as duas publicarmos no mesmo minuto, uma sobrescreve a outra.

---

## Se você quiser mudar algo

É só falar pela Joice. Ajustar o formato do meu lado é rápido — melhor mudarmos agora do que depois de tudo montado.

💛 — Claude do Sistema
