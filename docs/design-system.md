# 🎨 Design System - Gamebox
Neste projeto, utilizamos um framework UI e aplicamos customizações pontuais para refletir a identidade visual.

### 1. Framework Base

- **Framework escolhido:** MaterializeCSS
- **Motivação:** Oferece componentes baseados no Material Design, permitindo uma prototipagem rápida e um visual corporativo, limpo e confiável.

### 2. Paleta de Cores (Customização)

As variáveis de cor do framework foram escolhidas para induzir o usuário ao erro ou alertá-lo (tarde demais) sobre as taxas:

### Cores de Fundo e Superfície

- **Deep Obsidian (Fundo Principal):** #0c0f10 (Usado para o background geral de todas as telas).

- **Surface Container (Cartões e Modais):** #1a1d1e (Usado para blocos bento, cards de jogos e superfícies de destaque).

- **Surface High (Hover e Destaque sutil):** #232e31 (Usado para estados de interação e separação de conteúdo).

### Cores de Texto e Acento

- **Primary Ice (Acento):** #aecbda (Usado para botões primários, ícones ativos, barras de progresso e links de navegação selecionados).

- **High Emphasis (Texto Primário)**: #f8f9fa (Off-white) (Usado para títulos e corpo de texto principal).

- **Medium Emphasis (Texto Secundário)**: #dee7eb com 60% de opacidade. (Usado para legendas, metadados e informações de apoio).

### Cores de Feedback

- **Positive (Prós):** #1B4D3E (Verde escuro)

- **Negative (Contras):** #7A1B1B (Carmesim profundo)

### 3. Tipografia

Importada via Google Fonts para substituir a fonte padrão do navegador e dar um ar mais moderno:

**Fonte Principal:** Inter (Sans-serif Geométrica)
- **Display (Títulos Hero):** 48px / Bold / Espaçamento -0.025em
- **Headline (Títulos de Seção):** 30px / Bold / Espaçamento -0.015em
- **Body Regular (Corpo de Texto):** 16px / Regular / Altura da linha 1.625
- **Metadata/Label (Legendas):** 12px / Medium / Espaçamento 0.2em (Caps)

### 4. Diretrizes de Uso de Componentes

Regras para a aplicação dos componentes do MaterializeCSS dentro da lógica predatória do Roubank:

- **Botões de Ação (`.btn`):** Ações que resultam em cobrança de taxas devem usar o modificador `.btn-large` e a cor primária (vermelho), para chamar atenção e induzir o clique. Ações de cancelamento ou fuga usam botões sem preenchimento (`.btn-flat`) para passarem despercebidos.
- **Cards (`.card`):** Usados obrigatoriamente para exibir o Saldo em destaque e encapsular as listagens do Extrato. Devem usar a sombra padrão (`z-depth-1`).
- **Formulários (`.input-field`):** Os inputs devem ser largos e burocráticos.
