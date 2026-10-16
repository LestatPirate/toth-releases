<p align="center"><img src="images/toth-logo.png" alt="Toth" width="140"></p>

# Toth

**Captura e anota o ecrã no Mac. Tudo local: sem conta, sem nuvem, sem telemetria. Gratuita.**
*Capture and annotate your Mac screen. Fully local: no account, no cloud, no telemetry. Free.*

[Português](#português) · [English](#english)

<p align="center"><img src="images/toth-editor-pt.png" alt="Editor do Toth" width="900"></p>

> **Versão 1.4.3 (pré-visualização).** Descarregue em [**Releases**](../../releases/latest). A app ainda não está notarizada pela Apple (ver *Instalar*) e os documentos legais são rascunhos. Este repositório só tem a página de descarregamento; o código-fonte é privado.

---

## Português

### O que faz

**Captura**
- **Região com o ecrã congelado** ao carregar no atalho: a captura é a do momento do atalho, mesmo que o ecrã mude depois. Arraste para escolher a área, **mova-a e redimensione-a** pelas alças, e só ao **confirmar** (botão *Capturar* ou **Enter**) segue para o editor. **Esc** cancela. Funciona com vários monitores.
- **Ecrã inteiro** pelo menu da barra de menus.
- **Imagem nova**, para além das capturas: **em branco** (tamanho, cor de fundo ou transparente) ou **a partir da área de transferência** (botão *Novo*, menu *Ficheiro*; ⌘N e ⇧⌘N).
- **Atalho global configurável** (por omissão **⌃⇧4**) em *Preferências*; avisa se a combinação é do sistema ou já está em uso.

**Editor (não destrutivo: a imagem original nunca é alterada)**
- **Ferramentas:** Mover, Seta, Linha, Texto, Balão, Retângulo, Elipse, Etapa, Marcador, Pixelização, Blur e Tela.
- **Texto no próprio objeto** (texto, balão, retângulo, elipse): fonte, tamanho, negrito/itálico/sublinhado, cor, alinhamento horizontal e vertical, listas de marcadores ou numeradas.
- **Cores da linha e do preenchimento** à escolha, espessura, opacidade e sombra.
- **Etapas numeradas** (1, 2, 3 · I, II, III · i, ii, iii · A, B, C · a, b, c), com cor do círculo e do número, fonte e **reinício da sequência**. **Redimensionam-se pelos cantos mantendo a proporção** (ou pelo controlo *Tamanho*), e o número ou a letra acompanha a escala e fica sempre centrado; o último tamanho usado é lembrado.
- **Blur e Pixelização** com intensidade ajustável, para ocultar informação sensível. Atuam sobre **tudo o que está por baixo**: a imagem e também os objetos inseridos em camadas inferiores (um objeto por cima do efeito continua nítido).
- **Área de trabalho (Tela):** aumente ou diminua a imagem, com cor de fundo ou transparente; **expande-se sozinha** quando um elemento sai da área.
- **Camadas:** ordem, ocultar, remover. Qualquer elemento pode ser removido ou editado **mais tarde**, mesmo depois de fechar e reabrir.
- **Copiar, colar, duplicar**; cola **imagens e texto de outras apps**. Desfazer/refazer, zoom e deslocamento.
- **Seleção rápida:** com uma ferramenta de desenho ativa, **clicar** num objeto existente seleciona-o e mostra as opções desse objeto; **arrastar** continua a desenhar um novo (por exemplo, uma seta a partir de uma caixa). **⌥ + clique** força a criação por cima de um objeto (útil para as etapas).
- **Exportar PNG** ou **copiar tudo** para a área de transferência.

**Biblioteca**
- **Abrir Biblioteca** (botão no canto inferior direito): grelha com a **pré-visualização atual** de cada captura, para escolher clicando; faixa de miniaturas no editor, que se pode **ocultar/mostrar** (botão «Biblioteca» no rodapé, ou *Ver → Mostrar/ocultar Biblioteca*, ⌥⌘L).
- **Abrir** (barra superior): abre **qualquer imagem do computador** (PNG, JPEG, HEIC, TIFF, GIF, BMP…) no editor. Fica como captura nova (o ficheiro original não é tocado) e as alterações guardam-se; com **Salvar como** exporta em **PNG, JPEG, HEIC ou TIFF**.
- Cada captura é **um só ficheiro `.capture`** (um ZIP normal) em `~/Pictures/Capture`, com nome **sem espaços**: `Toth_AAAA-MM-DD_HH.MM.SS.capture`. Os ficheiros `.capture` **abrem com o Toth** (duplo clique, *Abrir com*, ou arrastar para o ícone do Dock).

**Comodidades**
- **Janela ajustável:** pode ficar estreita (as ferramentas deslizam na barra; as setas «‹ ›» deslizam as ferramentas **de forma contínua**: um clique avança um pouco, mantendo premido continua a deslizar, e a roda/trackpad também; apagam-se quando não há mais para esse lado), e o painel de **Propriedades** está sempre à direita, com uma divisória que se **arrasta** para o redimensionar, até desaparecer para o lado; com o painel escondido aparece uma **faixa larga** com uma pega bem visível: um clique, ou arrastar para a esquerda, volta a abri-lo (também por *Ver → Mostrar/ocultar Propriedades*, ⌥⌘P; duplo clique na divisória esconde-o).
- O Toth também aparece em *Abrir com* para imagens.
- Cada ferramenta **lembra a última personalização**, mesmo depois de fechar a app.
- **Português e inglês**, com mudança imediata em *Preferências*.
- **Privacidade:** a app não usa a internet nem recolhe dados.

### Requisitos
macOS 15 ou superior (Apple Silicon e Intel; testado em Apple Silicon).

### Instalar
1. Em [**Releases**](../../releases/latest), descarregue `Toth-1.4.3.zip` e descomprima.
2. Arraste `Toth.app` para a pasta **Aplicações**.
3. **Primeira abertura (só é preciso uma vez):** como a app ainda não está notarizada pela Apple, o macOS mostra *“Toth” não aberto*, com os botões *Mover para o Lixo* e *OK*. **Não mova para o Lixo.** Clique em **OK**, abra **Definições do Sistema → Privacidade e Segurança**, desça até **Segurança**, clique em **Abrir mesmo assim** junto a “Toth”, confirme com a palavra-passe ou Touch ID e clique em **Abrir**. (No macOS 14 ou anterior basta botão direito → **Abrir**. Alternativa no Terminal: `xattr -dr com.apple.quarantine /Applications/Toth.app`.)
4. Conceda a permissão de **Gravação de Ecrã** (*Definições do Sistema → Privacidade e Segurança → Gravação de Ecrã e Áudio do Sistema*) e volte a abrir a app. O Toth aparece no **Dock** e na **barra de menus**; clicar no ícone do Dock abre o editor.

### Usar
Carregue em **⌃⇧4** (ou use o ícone na barra de menus ou o menu *Ficheiro*) → escolha a área → **Enter** → anote → **Salvar como** / **Copiar tudo**. As **Preferências** (engrenagem no rodapé, ou ⌘,) têm o atalho e o idioma.

### Ainda não tem
Captura de janela e de scroll, temporizador, cursor na captura, vídeo/áudio/GIF, apagar uma área da imagem, versão para Windows. Fora do âmbito por decisão: contas, partilha online, IA na nuvem e telemetria.

### Licença, privacidade e contacto
Gratuita, de código fechado. Dúvidas e problemas: abra uma *issue* neste repositório. © 2026 **Matéria Primordial, Unipessoal Lda** (NIF 515982890). [Licença](LICENSE.md) ([EN](LICENSE.en.md)) · [Privacidade](PRIVACY.md) · [Segurança](SECURITY.md) · [Avisos de terceiros](THIRD_PARTY_NOTICES.md).

---

## English

<p align="center"><img src="images/toth-editor-en.png" alt="Toth editor" width="900"></p>

### What it does

**Capture**
- **Region capture with a frozen screen:** the screen freezes the moment you press the shortcut, so the capture is that exact moment even if the screen changes afterwards. Drag to choose the area, **move and resize** it with the handles, and only when you **confirm** (*Capture* button or **Enter**) does it go to the editor. **Esc** cancels. Multi-monitor aware.
- **Full-screen capture** from the menu bar.
- **New images** besides captures: **blank** (size, background color or transparent) or **from the clipboard** (*New* button, *File* menu; ⌘N and ⇧⌘N).
- **Configurable global shortcut** (default **⌃⇧4**) in *Preferences*; it warns if a combination is taken by the system or already in use.

**Editor (non-destructive: the original image is never changed)**
- **Tools:** Move, Arrow, Line, Text, Callout, Rectangle, Ellipse, Step, Highlighter, Pixelate, Blur and Canvas.
- **Text directly in the object** (text, callout, rectangle, ellipse): font, size, bold/italic/underline, color, horizontal and vertical alignment, bulleted or numbered lists.
- Your choice of **line and fill colors**, thickness, opacity and shadow.
- **Numbered steps** (1, 2, 3 · I, II, III · i, ii, iii · A, B, C · a, b, c), with circle and number colors, font, and **sequence restart**. They **resize by their corners keeping the proportions** (or with the *Size* control), and the number or letter scales along and stays centered; the last size used is remembered.
- **Blur and Pixelate** with adjustable strength, to hide sensitive information. They act on **everything beneath them**: the image and also objects on lower layers (an object above the effect stays sharp).
- **Work area (Canvas):** enlarge or shrink the image, with a background color or transparent; it **expands automatically** when an element goes outside the area.
- **Layers:** order, hide, remove. Any element can be removed or edited **later**, even after closing and reopening.
- **Copy, paste, duplicate**; pastes **images and text from other apps**. Undo/redo, zoom and pan.
- **Quick selection:** with a drawing tool active, **clicking** an existing object selects it and shows its options; **dragging** keeps drawing a new one (for example an arrow from a box). **⌥ + click** forces creation on top of an object (handy for steps).
- **Export PNG** or **copy all** to the clipboard.

**Library**
- **Open Library** (button at the bottom right): a grid with the **current preview** of each capture to pick by clicking; a thumbnail strip in the editor.
- **Open** (top bar): opens **any image on your computer** (PNG, JPEG, HEIC, TIFF, GIF, BMP…) in the editor. It becomes a new capture (the original file is never touched) and your changes are saved; **Save as** exports **PNG, JPEG, HEIC or TIFF**.
- Each capture is **a single `.capture` file** (a standard ZIP) in `~/Pictures/Capture`, with a name **without spaces**: `Toth_YYYY-MM-DD_HH.MM.SS.capture`. `.capture` files **open with Toth** (double-click, *Open With*, or drag onto the Dock icon).

**Conveniences**
- **Adjustable window:** it can be narrow (tools slide along the bar; the «‹ ›» arrows scroll the tools **continuously**: a click nudges them, holding keeps them moving, and the wheel/trackpad works too; they dim when there is no more on that side), and the **Properties** panel is always on the right, with a divider you **drag** to resize it until it slides out of sight; when it is hidden a **wide strip** with an obvious grip appears: one click, or dragging left, brings it back (also via *View → Show/Hide Properties*, ⌥⌘P; double-clicking the divider hides it).
- Toth also appears under *Open With* for images.
- Each tool **remembers its last customization**, even after you quit the app.
- **Portuguese and English**, switchable instantly in *Preferences*.
- **Privacy:** the app never uses the internet and collects no data.

### Requirements
macOS 15 or later (Apple Silicon and Intel; tested on Apple Silicon).

### Install
1. Under [**Releases**](../../releases/latest), download `Toth-1.4.3.zip` and unzip it.
2. Drag `Toth.app` to **Applications**.
3. **First launch (only needed once):** because the app is not yet notarized by Apple, macOS shows *“Toth” Not Opened*, with *Move to Trash* and *Done* buttons. **Don't move it to the Trash.** Click **Done**, open **System Settings → Privacy & Security**, scroll to **Security**, click **Open Anyway** next to “Toth”, confirm with your password or Touch ID, then click **Open**. (On macOS 14 or earlier, right-click → **Open** is enough. Terminal alternative: `xattr -dr com.apple.quarantine /Applications/Toth.app`.)
4. Grant the **Screen Recording** permission (*System Settings → Privacy & Security → Screen & System Audio Recording*) and reopen the app. Toth shows in the **Dock** and the **menu bar**; clicking the Dock icon opens the editor.

### Use
Press **⌃⇧4** (or use the menu bar icon or the *File* menu) → choose the area → **Enter** → annotate → **Save as** / **Copy all**. **Preferences** (gear icon in the footer, or ⌘,) hold the shortcut and the language.

### Not yet available
Window and scrolling capture, timer, cursor in captures, video/audio/GIF, erasing an area of the image, a Windows version. Out of scope by design: accounts, online sharing, cloud AI and telemetry.

### License, privacy and contact
Free, closed source. Questions and problems: open an issue in this repository. © 2026 **Matéria Primordial, Unipessoal Lda** (NIF 515982890). [License](LICENSE.en.md) · [Privacy](PRIVACY.md) · [Security](SECURITY.md) · [Third-party notices](THIRD_PARTY_NOTICES.md).
