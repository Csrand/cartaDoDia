- # Documentação do Sistema
- ## I. Visão Geral do Sistema
- ### Objetivo:
  Descreva de forma breve o que o sistema faz, seus principais objetivos e funcionalidades. Indique o propósito do sistema e como ele resolve o problema.  
  
  **Exemplo:**  
  "O sistema **Cartas do Destino** oferece aos usuários uma reflexão diária através do sorteio de cartas de tarot aleatórias, com animação e citação relacionada. O objetivo é proporcionar um momento de introspecção e autoconhecimento."  
  
---
- ## II. Requisitos do Sistema
- ### Requisitos Funcionais (RF)
  Descreva as funcionalidades que o sistema precisa ter.  
- **RF01:** O sistema permite que o usuário sorteie uma carta aleatória todos os dias.
- **RF02:** O sistema exibe a carta sorteada com uma animação de virada.
- **RF03:** Após a animação, o sistema mostra uma reflexão relacionada à carta.
- **RF04:** O sistema permite que o usuário salve cartas marcantes em seu perfil.
- **RF05:** O sistema permite que o usuário visualize, edite e exclua cartas salvas.
- **RF06:** O sistema deve ter uma tela para o usuário fazer o login atráves da entrada do seu e-mail junto com sua senha dentro do formulário e será enviado ao back-end para validação através do botão "Login" e deve permitir a solicitação da recuperação de senha através do botão "esqueci a senha". 
- **RF07:** O sistema deve ter uma tela para o usuário fazer o cadastro no sistema colocando seu e-mail que deve ser único por usuário junto com a senha que o usário vai criar e repetir dentro do formulario exibido na tela para a validação do front-end e será enviado ao back-end para validação através do botão "Cadastrar".
- **RF08:** O sistema deve ter uma tela para o usuário solicitar a recuperação de sua senha atráves da entrada do seu e-mail dentro do formulário e é enviado ao back-end para validação através do botão "Confirmar e-mail".
- **RF09:** O sistema deve ter uma tela para o usuário criar uma nova senha informando a nova senha desejada e digitando novamente para a validação do front-end e deve ser enviada para validação através do botão "Confirmar".
- **RF10** O sistema deve ter uma tela onde sera apresentado ao usuário através de texto e imagens informações sobre o site e sobre o seu funcionamento. a pagina deve será a pagina principal e deve ter links através de botões funcionais para a navegação nas demais paginas e para o cadastro e uso do sistema.
- ### Requisitos Não Funcionais (RNF)
  Descreva características como desempenho, segurança, usabilidade, etc.  
- **RNF01:** O sistema deve ser responsivo, adaptando-se bem a dispositivos móveis e desktops.
- **RNF02:** O tempo de resposta para exibir a carta sorteada deve ser inferior a 2 segundos.
- **RNF03:** O sistema deve criptografar as senhas dos usuários para segurança.
-
---
- # Casos de Uso — Sistema de Sorteio de Cartas com Coleção Pessoal
- ## I. Acesso e Navegação Inicial
- ### Caso de Uso 1: Acesso Inicial
- **Ator:** Usuário
- **Descrição:** Apresenta o propósito do sistema e informa as funcionalidades disponíveis.
- #### Fluxo Principal:
	I. O usuário acessa a página inicial do site.
	II. O sistema exibe uma introdução sobre o propósito do site.
	III. O sistema apresenta a funcionalidade principal: sorteio de uma carta diária.
	IV. O sistema informa que usuários cadastrados podem salvar suas cartas favoritas.
	V. O usuário pode optar por seguir para o sorteio ou realizar o cadastro/login.

- #### Pós-condição:
- O usuário entende a funcionalidade do sistema antes de interagir com ele.
  
---
- ## II. Interação com Cartas
- ### Caso de Uso 2: Sorteio de Carta
- **Ator:** Usuário
- **Descrição:** Permite o sorteio e visualização de uma carta por dia.
- #### Pré-condição:
- Estar na página principal e ainda não ter sorteado a carta do dia.
- #### Fluxo Principal:
	I. O sistema mostra um baralho embaralhado.
	II. O usuário clica no baralho.
	III. O sistema mostra uma carta saindo do baralho.
	IV. O usuário clica na carta para virá-la.
	V. O sistema exibe a carta virada, seu significado e uma citação relacionada.
	VI. O sistema registra a data da interação.
	VII. O sistema pergunta se o usuário deseja salvar a carta.

- #### Pós-condição:
- O sistema bloqueia novos sorteios até o dia seguinte.
  
---
- ## III. Coleção Pessoal
- ### Caso de Uso 3: Registro de Carta
- **Ator:** Usuário
- **Descrição:** Permite ao usuário salvar a carta sorteada em seu perfil.
- #### Pré-condição:
- O usuário já sorteou sua carta do dia.
- #### Fluxo Principal:
	I. O sistema pergunta se o usuário deseja salvar a carta sorteada.
	II. O usuário clica na opção "Sim".
	III. O sistema verifica se o usuário está autenticado.
	IV. Caso não esteja, o sistema redireciona para login.
	V. O usuário informa e-mail e senha.
	VI. O sistema valida os dados.
	VII. Se corretos, salva a carta no perfil.
	VIII. Exibe: "Carta registrada com sucesso".

- #### Fluxo Alternativo:
- Se o usuário já estiver logado, a carta é salva diretamente.
- #### Pós-condição:
- Carta salva na coleção do usuário.
  
---
- ### Caso de Uso 4: Visualizar Cartas Salvas
- **Ator:** Usuário autenticado
- **Descrição:** Permite ao usuário ver suas cartas salvas.
- #### Fluxo Principal:
	I. O usuário acessa a área de perfil.
	II. O sistema exibe a lista de cartas salvas com data e significado.
---

- ### Caso de Uso 5: Remover Carta da Coleção
- **Ator:** Usuário autenticado
- **Descrição:** Permite ao usuário excluir uma carta salva.
- #### Fluxo Principal:
	I. O usuário acessa sua coleção.
	II. Seleciona a carta a ser excluída.
	III. O sistema exibe uma confirmação.
	IV. O usuário confirma.
	V. O sistema remove a carta da coleção.
---

- ## IV. Gerenciamento de Conta
- ### Caso de Uso 6: Cadastro de Usuário
- **Ator:** Novo usuário
- **Descrição:** Criação de conta com e-mail e senha únicos.
- #### Fluxo Principal:
	I. O usuário acessa a página de cadastro.
	II. Informa e-mail e senha.
	III. O sistema verifica se o e-mail já existe.
	IV. Se não existir, cria o usuário.
	V. Exibe mensagem: "Cadastro realizado com sucesso".

- #### Validações:
- E-mail deve ser único.
- Senha com no mínimo 8 caracteres, contendo letras e números.
  
---
- ### Caso de Uso 7: Login
- **Ator:** Usuário
- **Descrição:** Permite acesso à área de usuário.
- #### Fluxo Principal:
	I. O usuário acessa a tela de login.
	II. Informa e-mail e senha.
	III. O sistema valida as credenciais.
	IV. Se corretas, redireciona o usuário.
	V. Caso contrário, exibe erro.
---

- ### Caso de Uso 8: Logout
- **Ator:** Usuário autenticado
- **Descrição:** Permite ao usuário sair da conta.
- #### Fluxo Principal:
	I. O usuário clica em "Sair".
	II. O sistema encerra a sessão e redireciona para a página inicial.
---

- ## V. Recuperação e Alteração de Conta
- ### Caso de Uso 9: Esqueci Minha Senha
- **Ator:** Usuário
- **Descrição:** Recuperar senha via e-mail.
- #### Fluxo Principal:
	I. O usuário acessa "Esqueci minha senha".
  	II. Informa seu e-mail.
  	III. O sistema envia um link de redefinição.
  	IV. O usuário acessa o link e define nova senha.

- #### Pós-condição:
- O usuário redefine a senha com sucesso.
  
---
- ### Caso de Uso 10: Alterar Senha
- **Ator:** Usuário autenticado
- **Descrição:** Permite troca da senha atual.
- #### Fluxo Principal:
	I. O usuário acessa a área de "Alterar senha".
	II. Informa a senha atual.
	III. Informa nova senha e confirmação.
	IV. O sistema valida e atualiza.

- #### Validações:
- Senha nova deve ser segura e diferente da anterior.
  
---
- ### Caso de Uso 11: Alterar E-mail
- **Ator:** Usuário autenticado
- **Descrição:** Permite alterar o e-mail de login.
- #### Fluxo Principal:
	I. O usuário acessa as configurações de conta.
	II. Informa novo e-mail e senha atual.
	III. O sistema valida os dados.
  	IV. O sistema atualiza o e-mail.
	V. O sistema notifica o usuário.

- #### Validações:
- O novo e-mail não pode estar em uso.
  
---
-
- ## VI. Arquitetura do Sistema
- ### Componentes Principais:
- **Frontend:** Interface com o usuário, utilizando HTML, CSS e JavaScript.
- **Backend:** Responsável pela lógica de negócios e interação com o banco de dados, utilizando Node.js ou outro framework.
- **Banco de Dados:** Onde os dados são armazenados, como SQLite ou MySQL.
- **Autenticação:** Utilização de JWT (JSON Web Tokens) para autenticação de usuários.
- ### Fluxo de Dados:
	I. O usuário faz login no sistema.
	II. O frontend envia uma requisição para o backend, que valida as credenciais.
	III. O backend consulta o banco de dados para obter as cartas salvas do usuário, se houver.
	IV. O backend sorteia uma carta aleatória e a envia ao frontend.
	V. O frontend exibe a carta e animação.
---

- ## VII. Estrutura do Banco de Dados
- ### Tabelas e Entidades Principais:
- **Usuários**
	- id (PK)
	- email (único)
	- senha_hash
- **CartasSalvas**
	- id (PK)
	- id_usuario (FK)
	- nome_carta
	- data_sorteio
	    
	  **Relacionamento:**  
	  Um usuário pode ter várias cartas salvas, então existe um relacionamento 1:N entre a tabela `Usuários` e `CartasSalvas`.  
	    
---
- ## VIII. Fluxo de Navegação (Wireframes)
  
  
---![image](https://github.com/user-attachments/assets/5da80ed9-7a7c-472c-a057-b64381e78ef9)


- ## IX. Regras de Negócio
  
  Defina as regras essenciais para o sistema funcionar corretamente.  
- **RN01:** Um usuário pode salvar apenas uma carta por vez. Caso queira salvar uma nova, deve excluir a carta anterior.
- **RN02:** O sistema garante que o email do usuário seja único.
- **RN03:** O sistema só permite o sorteio de uma carta nova uma vez a cada 24 horas.
  
---
- ## X. Tecnologias Utilizadas
  
  Liste as tecnologias escolhidas para o desenvolvimento do sistema.  
- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Node.js, Express
- **Banco de Dados:** SQLite
- **Autenticação:** JWT (JSON Web Tokens)
  
---
- ## XI. Testes
  
  Descreva os tipos de testes que serão feitos para garantir o funcionamento do sistema.  
- **Testes Unitários:** Testar funções do backend isoladamente.
- **Testes de Integração:** Testar se o frontend, backend e banco de dados estão funcionando corretamente juntos.
- **Testes Funcionais:** Testar se o sistema atende aos requisitos funcionais definidos.
  
---
- ## XII. Plano de Lançamento
  
  Descreva as etapas para colocar o sistema em produção.  
  
	1. **Verificação de Testes:** Certifique-se de que todos os testes passaram.
	2. **Configuração do Ambiente de Produção:** Ajuste as configurações para produção.
	3. **Lançamento Beta:** Lançamento para um grupo pequeno de usuários para testes.
	4. **Ajustes Finais:** Corrigir bugs com base no feedback dos usuários beta.
	5. **Lançamento Oficial:** Colocar o sistema disponível para o público em geral.
---
