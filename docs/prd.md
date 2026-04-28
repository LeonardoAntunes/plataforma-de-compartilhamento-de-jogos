# 📄 Product Requirements Document (PRD) - Gamebox

## 1. Visão Geral e Objetivo

O **Gamebox** é uma aplicação web didática que visa criar um espaço onde você pode compartilhar a sua experiencia de suas jogatinas e deseja ao decorrer dos jogos mostrar as suas conquistas e fazer reviwes sobre os jogos qual completou.

## 2. Atores do Sistema

- **Visitante:** Usuário não autenticado que acessa a página inicial e deseja abrir uma conta.
- **Jogador:** Usuário autenticado que consegue realizar postagens, sendo as mesmas reviews, comentarios em outras postagens, compartilhar conquistas e os status atual de sua jogatina(se está jogando atualmente, deu uma pausa ou completou).
- **O Administrador(Sistema):** Ator invisível que monitora os comportamentos da comunidade, agindo quano necessario para ajudar sobre duvidas ou realizar punimentos aos que ferem as diretrizes da comunidade.

## 3. Histórias de Usuário e Escopo

Abaixo estão as funcionalidades principais do MVP (Minimum Viable Product), escritas sob a perspectiva do usuário final.

### 👤 Épico 1: Criação de conta e login

- **US01 - Abertura de Conta:** Como um Visitante, para criar a conta será necessario a criação de um nome de usuario, um email valido e a criação de uma senha.
  - _Critérios de Aceitação:_ O nome de usuario deve ser unico; todos os campos são obrigatórios; o email deve ser válido.
- **US02 - Acesso ao Sistema (Login):** Como um Jogador, para acessar é necessário usar o email ou o nome de usario e utilazar a sua senha.
- **US03 - Personalização de Perfil:** Após realizar o login e ao entrar na aplicação, ha a possibilidade de entrar no seu perfil e personalizalo da maneira que deseja, podendo mudar a foto de perfil e colocar detalhes sobre vocẽ, como suas redes socias.**(ideia pode ser alterada/removida no futuro)**

### 🎮 Épico 2: Opções dentro da aplicação

- **US04 - Registro de jogos:** Como usuário, quero registrar os jogos que estou jogando para acompanhar meu progresso.
Como usuário, quero marcar um jogo como “finalizado” para indicar que completei a experiência.
Criação de reviews
- **US05 - Criação de reviews:** Como usuário, quero escrever uma review ao terminar um jogo para compartilhar minha opinião.
Como usuário, quero avaliar os pontos positivos e negativos de um jogo para ajudar outros jogadores.
Como usuário, quero dar uma nota ao jogo para resumir minha avaliação.

### 📋 Épico 3: Admnistração

- **US06 - Gerenciamento e exclusão de qualquer postagen:** Como administrador, quero moderar reviews 
Como administrador, quero remover conteúdos inadequados para garantir boas práticas na comunidade.
