# Moldura da câmera da kalibxd_ 💚💛

Moldura animada "de cria" pra câmera da [kalibxd_](https://www.twitch.tv/kalibxd_), feita pra fonte **Navegador** do OBS. O fundo é transparente, e é HTML/CSS/JS puro: sem build e sem dependências.

**No ar:** [kalibxd.carlosandemberg.com.br](https://kalibxd.carlosandemberg.com.br). Lá você escolhe a tela e as opções e copia o link pro OBS. A moldura em si fica em `https://kalibxd.carlosandemberg.com.br/moldura-camera.html`.

| Arquivo | O que é | Tamanho no OBS |
|---|---|---|
| `moldura-camera.html` | Borda nas cores da bandeira, plaquinha com o nome em letra de pichação, morrinho com a bandeira, pipas, vira-lata caramelo, caixa de som, adesivos e o grau de moto | **1920 × 1080** (tela do Valorant) ou **583 × 505** (`?solta`, só a câmera) |
| `index.html` | Gerador de link: modelo, nome, posição e tamanho da câmera, quais enfeites entram, quantas pipas e o intervalo do grau. Também mostra a live com a moldura por cima | — |

## A moldura

A borda é a bandeira: verde por fora, um filete amarelo e o miolo azul cheio das estrelinhas brancas do céu da bandeira. Um brilho corre por ela de vez em quando. O nome fica numa plaquinha verde com o losango amarelo e o miolo azul, em maiúscula na [Sedgwick Ave Display](https://fonts.google.com/specimen/Sedgwick+Ave+Display) (letra de pichação), com degradê amarelo e contorno escuro.

Em cima da câmera fica um morrinho com casinhas coloridas, laje com vergalhão, caixa d'água azul, antena e as janelas acendendo e apagando. No alto do morro, a bandeira do Brasil tremula no mastro. As pipas de papel de seda voam com a rabiola balançando, e a linha delas desce pro morrinho. Na quina de cima fica o vira-lata caramelo de bandana verde-amarela: ele abana o rabo, pisca, mexe a orelha, inclina a cabeça e fica com a língua de fora. Do lado de fora, no canto de baixo, a caixa de som tipo JBL bate o grave a 130 BPM, com o LED trocando de cor e soltando notinhas. Na borda da direita tem os adesivos **021** e o coração verde e amarelo.

A cada 30 segundos tem **grau**. Ela, de camisa da seleção, short azul, óculos Juliet e argola, entra pela beirada da tela empinando a moto verde e amarela e soltando fumaça. A moto pula a plaquinha, que pula junto e solta confete verde e amarelo, e dá um mortal por cima do caramelo, que late ("AU AU!"). No fim ela some numa nuvem de fumaça. Enquanto isso as pipas dão laçada em volta do nome, a caixa de som acelera e as janelas piscam.

De vez em quando pipoca um **balãozinho de gíria carioca** no caramelo, na plaquinha ou na caixa de som: COÉ!, MERMÃO, CARACA!, PAPO RETO, SINISTRO!, É O 021, TÁ LIGADO?, DEMORÔ!, QUE ISSO?!, SE LIGA!, PARTIU!, BRABO!

### A tela do Valorant

As medidas saíram da própria live, numa tela 1920 × 1080: câmera em **x 0, y 538, 387 × 217**, encostada na beirada da esquerda e com cantos arredondados.

- A beirada da esquerda fica sem borda (a moldura continua pra fora da tela), e os cantos da moldura acompanham o arredondado da câmera.
- O **minimapa** vai até mais ou menos y 400, então nada sobe além disso. Morrinho, pipas, bandeira e caramelo ficam na faixa entre o minimapa e a câmera.
- **Embaixo da câmera** aparece o "trocar jogador" quando ela morre, então nada fica embaixo. A caixa de som fica do lado de fora, à direita.
- As pipas nunca entram na frente da câmera.

### Colocar no OBS (tela do Valorant)

1. Na cena do jogo: **Fontes → + → Navegador**
2. **URL**: `https://kalibxd.carlosandemberg.com.br/moldura-camera.html?tela=valorant`
3. **Largura 1920, Altura 1080** (o tamanho da tela do OBS). A fonte cobre a tela toda e a moldura cai sozinha em volta da câmera.
4. Na lista de fontes, deixe a moldura **acima** da câmera.

### Só a câmera: pra arrastar junto com a webcam

Com `?solta`, a moldura tem borda **em volta toda**. Em cima ficam o morrinho, a plaquinha e o caramelo. Embaixo ficam a caixa de som no canto esquerdo, a bola fazendo embaixadinha no direito e os adesivos 021, coração e RJ na borda. No grau a moto dá a volta inteira em volta da câmera, grudada na borda, tipo globo da morte, e pula o caramelo.

1. **Fontes → + → Navegador**, URL `https://kalibxd.carlosandemberg.com.br/moldura-camera.html?solta`
2. **Largura 583, Altura 505**, pra uma câmera de 385 × 217. Com outro tamanho (`largura=`/`altura=`), o gerador de link mostra o tamanho da fonte.
3. A câmera fica 99 px da esquerda e 189 px do topo da fonte.
4. Selecione a moldura e a câmera → botão direito → **Agrupar itens selecionados**. Daí é só arrastar e redimensionar o grupo.

### Prévia

Abrindo o link num navegador normal aparece um fundo de exemplo com o HUD do Valorant e o timer e a meta dela de mentirinha, no lugar em que ficam na live. Clique em qualquer lugar pra fazer o grau. Dentro do OBS o fundo fica transparente.

### Opções no link

Junte com `&`, ex.: `moldura-camera.html?tela=valorant&pipas=6&grau=45`.

| Opção | O que faz |
|---|---|
| `tela=valorant` | A tela do jogo (o padrão) |
| `solta` | Modelo só da câmera, com borda em volta toda. Usa só `largura`/`altura` |
| `x=0&y=538` | Canto de cima-esquerdo da câmera, em pixels da tela |
| `largura=387&altura=217` | Tamanho da câmera. Os enfeites crescem ou encolhem junto |
| `resolucao=1280x720` | Tamanho da tela do OBS, se não for 1920 × 1080. Sem `x`/`y`, a posição encolhe junto |
| `nome=Kali` | Texto da plaquinha (`nome=` sem nada esconde a plaquinha) |
| `pipas=6` | Quantas pipas voando (0 a 300; `pipas=0` tira as pipas) |
| `velocidade=0.6` | Velocidade das pipas: `1` é o padrão, `2` é rápido, `0.5` é bem devagar |
| `grau=45` | Segundos entre um grau e outro (`grau=0` desliga) |
| `moto=0` | Grau sem a moto: só a plaquinha pulando, o confete e o latido |
| `morro=0` | Sem o morrinho (e a bandeira) |
| `caramelo=0` | Sem o vira-lata caramelo |
| `som=0` | Sem a caixa de som |
| `adesivos=0` | Sem os adesivos |
| `girias=0` | Sem os balõezinhos de gíria |
| `girias=COÉ,PAPO RETO` | Troca as gírias (separe com vírgula) |
| `zoom` | Só na prévia: mostra a moldura de pertinho |

**Mudou a câmera de lugar?** No OBS, botão direito na câmera → **Transformar → Editar transformação**. Copie a posição e o tamanho pro gerador de link. O tamanho da tela fica em **Configurações → Vídeo → Resolução base**.

### Personalizar

O resto fica no bloco `CONFIG`, no começo de `moldura-camera.html`: cores, fontes, lugar da câmera, lista de gírias, batida da caixa de som, grossura da borda e cantos. Edite, salve e faça o deploy de novo. No OBS, botão direito na fonte → **Atualizar**.

## Publicar

São arquivos estáticos, então qualquer hospedagem estática serve.

**Coolify**

1. **Projects → New Resource → Public Repository** (ou **GitHub App**, pra fazer deploy a cada push) e cole a URL deste repositório.
2. **Build Pack**: `Dockerfile` (serve na porta **80**). Em **Health Checks**, ligue o healthcheck no caminho `/`.
3. Defina o domínio e clique em **Deploy**. A moldura fica em `https://SEU-DOMINIO/moldura-camera.html`.

A seção "Em cima da live" do gerador usa o player da Twitch, que só funciona em HTTPS (ou em `localhost`).
