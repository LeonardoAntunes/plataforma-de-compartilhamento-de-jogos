# 📄 Product Requirements Document (PRD) - Gamebox

## 1. Visão Geral e Objetivo

O **Gamebox** é uma aplicação web didática que visa criar um espaço onde você pode compartilhar a sua experiencia de suas jogatinas e deseja ao decorrer dos jogos mostrar as suas conquistas e fazer reviwes sobre os jogos qual completou.

**O grande diferencial ():**

## 2. Atores do Sistema

- **Visitante:** Usuário não autenticado que acessa a página inicial e deseja abrir uma conta.
- **Reviwer:** Usuário autenticado que consegue realizar postagens, sendo as mesmas reviews, comentarios em outras postagens, compartilhar conquistas e os status atual de sua jogatina(se está jogando atualmente, deu uma pausa ou completou).
- **O Administrador(Sistema):** Ator invisível que monitora os comportamentos da comunidade, agindo quano necessario para ajudar sobre duvidas ou realizar punimentos aos que ferem as diretrizes da comunidade.

## 3. Histórias de Usuário e Escopo

Abaixo estão as funcionalidades principais do MVP (Minimum Viable Product), escritas sob a perspectiva do usuário final.

### 👤 Épico 1: Criação de conta e login

- **US01 - Abertura de Conta:** Como um Visitante, para criar a conta será necessario a criação de um nome de usuario, um email valido e a criação de uma senha.
  - _Critérios de Aceitação:_ O nome de usuario deve ser unico; todos os campos são obrigatórios; o email deve ser válido.
- **US02 - Acesso ao Sistema (Login):** Como um Reviwer, para acessar é necessário usar o email ou o nome de usario e utilazar a sua senha.
- **US03 - Personalização de Perfil:** Após realizar o login e ao entrar na aplicação, ha a possibilidade de entrar no seu perfil e personalizalo da maneira que deseja, podendo mudar a foto de perfil e colocar detalhes sobre vocẽ, como suas redes socias.**(ideia pode ser alterada/removida no futuro)**

### 🎮 Épico 2: Opções dentro da aplicação

- **US04 - Compartilhar os jogos que estão jogando e seu status:** Como um Reviwer logado, ele pode deixar registrado os jogos que está jogando e os status no mesmo, podendo definir se está jogando, deu uma pausa ou já o completou.
- **US04 - Realizar e publicar Review:** Como um Reviewer, você pode produzir reviews dos jogos que jogou e comentar seus pontos fortes e fracos, o que julgou como um diferencia e se recomenda ele ou não.
- **US05 - Comentar em postagens:** Como um Reviewer, vocẽ tem a opção de realizar comentarios em postagens, podendo discutir sobre o tema que achou debativel em alguma postagem.
  - _Critérios de Aceitação:_ Para realizar essas acções é necessario que o usuario esteja logado; 

### 📊 Épico 3: Histórico e Transparência

- **US06 - Visualizar Extrato:** Como um Cliente, quero visualizar uma lista (tabela ou cards) com o histórico de todas as minhas transações (depósitos e saques).
  - _Critérios de Aceitação:_ A lista deve mostrar a data, o tipo de transação, o valor bruto e **o valor da taxa cobrada** pelo Roubank, deixando claro o quanto o cliente perdeu na operação.
