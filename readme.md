- # Documentação do Sistema
- ## 1. Visão Geral do Sistema
- ### Objetivo:
  Descreva de forma breve o que o sistema faz, seus principais objetivos e funcionalidades. Indique o propósito do sistema e como ele resolve o problema.  
  
  **Exemplo:**  
  "O sistema **Cartas do Destino** oferece aos usuários uma reflexão diária através do sorteio de cartas de tarot aleatórias, com animação e citação relacionada. O objetivo é proporcionar um momento de introspecção e autoconhecimento."  
  
---
- ## 2. Requisitos do Sistema
- ### Requisitos Funcionais (RF)
  Descreva as funcionalidades que o sistema precisa ter.  
- **RF01:** O sistema permite que o usuário sorteie uma carta aleatória todos os dias.
- **RF02:** O sistema exibe a carta sorteada com uma animação de virada.
- **RF03:** Após a animação, o sistema mostra uma reflexão relacionada à carta.
- **RF04:** O sistema permite que o usuário salve cartas marcantes em seu perfil.
- **RF05:** O sistema permite que o usuário visualize, edite e exclua cartas salvas.
- ### Requisitos Não Funcionais (RNF)
  Descreva características como desempenho, segurança, usabilidade, etc.  
- **RNF01:** O sistema deve ser responsivo, adaptando-se bem a dispositivos móveis e desktops.
- **RNF02:** O tempo de resposta para exibir a carta sorteada deve ser inferior a 2 segundos.
- **RNF03:** O sistema deve criptografar as senhas dos usuários para segurança.
-
---
- # Casos de Uso — Sistema de Sorteio de Cartas com Coleção Pessoal
- ## 1. Acesso e Navegação Inicial
- ### Caso de Uso 1: Acesso Inicial
- **Ator:** Usuário
- **Descrição:** Apresenta o propósito do sistema e informa as funcionalidades disponíveis.
- #### Fluxo Principal:
	1. O usuário acessa a página inicial do site.
	2. O sistema exibe uma introdução sobre o propósito do site.
	3. O sistema apresenta a funcionalidade principal: sorteio de uma carta diária.
	4. O sistema informa que usuários cadastrados podem salvar suas cartas favoritas.
	5. O usuário pode optar por seguir para o sorteio ou realizar o cadastro/login.

- #### Pós-condição:
- O usuário entende a funcionalidade do sistema antes de interagir com ele.
  
---
- ## 2. Interação com Cartas
- ### Caso de Uso 2: Sorteio de Carta
- **Ator:** Usuário
- **Descrição:** Permite o sorteio e visualização de uma carta por dia.
- #### Pré-condição:
- Estar na página principal e ainda não ter sorteado a carta do dia.
- #### Fluxo Principal:
	1. O sistema mostra um baralho embaralhado.
	2. O usuário clica no baralho.
	3. O sistema mostra uma carta saindo do baralho.
	4. O usuário clica na carta para virá-la.
	5. O sistema exibe a carta virada, seu significado e uma citação relacionada.
	6. O sistema registra a data da interação.
	7. O sistema pergunta se o usuário deseja salvar a carta.

- #### Pós-condição:
- O sistema bloqueia novos sorteios até o dia seguinte.
  
---
- ## 3. Coleção Pessoal
- ### Caso de Uso 3: Registro de Carta
- **Ator:** Usuário
- **Descrição:** Permite ao usuário salvar a carta sorteada em seu perfil.
- #### Pré-condição:
- O usuário já sorteou sua carta do dia.
- #### Fluxo Principal:
	1. O sistema pergunta se o usuário deseja salvar a carta sorteada.
	2. O usuário clica na opção "Sim".
	3. O sistema verifica se o usuário está autenticado.
	4. Caso não esteja, o sistema redireciona para login.
	5. O usuário informa e-mail e senha.
	6. O sistema valida os dados.
	7. Se corretos, salva a carta no perfil.
	8. Exibe: "Carta registrada com sucesso".

- #### Fluxo Alternativo:
- Se o usuário já estiver logado, a carta é salva diretamente.
- #### Pós-condição:
- Carta salva na coleção do usuário.
  
---
- ### Caso de Uso 4: Visualizar Cartas Salvas
- **Ator:** Usuário autenticado
- **Descrição:** Permite ao usuário ver suas cartas salvas.
- #### Fluxo Principal:
	1. O usuário acessa a área de perfil.
	2. O sistema exibe a lista de cartas salvas com data e significado.
---

- ### Caso de Uso 5: Remover Carta da Coleção
- **Ator:** Usuário autenticado
- **Descrição:** Permite ao usuário excluir uma carta salva.
- #### Fluxo Principal:
	1. O usuário acessa sua coleção.
	2. Seleciona a carta a ser excluída.
	3. O sistema exibe uma confirmação.
	4. O usuário confirma.
	5. O sistema remove a carta da coleção.
---

- ## 4. Gerenciamento de Conta
- ### Caso de Uso 6: Cadastro de Usuário
- **Ator:** Novo usuário
- **Descrição:** Criação de conta com e-mail e senha únicos.
- #### Fluxo Principal:
	1. O usuário acessa a página de cadastro.
	2. Informa e-mail e senha.
	3. O sistema verifica se o e-mail já existe.
	4. Se não existir, cria o usuário.
	5. Exibe mensagem: "Cadastro realizado com sucesso".

- #### Validações:
- E-mail deve ser único.
- Senha com no mínimo 8 caracteres, contendo letras e números.
  
---
- ### Caso de Uso 7: Login
- **Ator:** Usuário
- **Descrição:** Permite acesso à área de usuário.
- #### Fluxo Principal:
	1. O usuário acessa a tela de login.
	2. Informa e-mail e senha.
	3. O sistema valida as credenciais.
	4. Se corretas, redireciona o usuário.
	5. Caso contrário, exibe erro.
---

- ### Caso de Uso 8: Logout
- **Ator:** Usuário autenticado
- **Descrição:** Permite ao usuário sair da conta.
- #### Fluxo Principal:
	1. O usuário clica em "Sair".
	2. O sistema encerra a sessão e redireciona para a página inicial.
---

- ## 5. Recuperação e Alteração de Conta
- ### Caso de Uso 9: Esqueci Minha Senha
- **Ator:** Usuário
- **Descrição:** Recuperar senha via e-mail.
- #### Fluxo Principal:
	1. O usuário acessa "Esqueci minha senha".
	2. Informa seu e-mail.
	3. O sistema envia um link de redefinição.
	4. O usuário acessa o link e define nova senha.

- #### Pós-condição:
- O usuário redefine a senha com sucesso.
  
---
- ### Caso de Uso 10: Alterar Senha
- **Ator:** Usuário autenticado
- **Descrição:** Permite troca da senha atual.
- #### Fluxo Principal:
	1. O usuário acessa a área de "Alterar senha".
	2. Informa a senha atual.
	3. Informa nova senha e confirmação.
	4. O sistema valida e atualiza.

- #### Validações:
- Senha nova deve ser segura e diferente da anterior.
  
---
- ### Caso de Uso 11: Alterar E-mail
- **Ator:** Usuário autenticado
- **Descrição:** Permite alterar o e-mail de login.
- #### Fluxo Principal:
	1. O usuário acessa as configurações de conta.
	2. Informa novo e-mail e senha atual.
	3. O sistema valida os dados.
	4. O sistema atualiza o e-mail.
	5. O sistema notifica o usuário.

- #### Validações:
- O novo e-mail não pode estar em uso.
  
---
-
- ## 4. Arquitetura do Sistema
- ### Componentes Principais:
- **Frontend:** Interface com o usuário, utilizando HTML, CSS e JavaScript.
- **Backend:** Responsável pela lógica de negócios e interação com o banco de dados, utilizando Node.js ou outro framework.
- **Banco de Dados:** Onde os dados são armazenados, como SQLite ou MySQL.
- **Autenticação:** Utilização de JWT (JSON Web Tokens) para autenticação de usuários.
- ### Fluxo de Dados:
	1. O usuário faz login no sistema.
	2. O frontend envia uma requisição para o backend, que valida as credenciais.
	3. O backend consulta o banco de dados para obter as cartas salvas do usuário, se houver.
	4. O backend sorteia uma carta aleatória e a envia ao frontend.
	5. O frontend exibe a carta e animação.
---

- ## 5. Estrutura do Banco de Dados
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
- ## 6. Fluxo de Navegação (Wireframes)
  
  Descreva a navegação básica do sistema com imagens ou diagramas.  
  
	1. **Tela de Login:** O usuário faz login usando email e senha.
	2. **Tela Inicial:** Exibe a carta virada; o usuário pode clicar para ver a animação da carta.
	3. **Tela de Cartas Salvas:** O usuário pode visualizar, editar ou excluir cartas que ele salvou.
---

- ## 7. Regras de Negócio
  
  Defina as regras essenciais para o sistema funcionar corretamente.  
- **RN01:** Um usuário pode salvar apenas uma carta por vez. Caso queira salvar uma nova, deve excluir a carta anterior.
- **RN02:** O sistema garante que o email do usuário seja único.
- **RN03:** O sistema só permite o sorteio de uma carta nova uma vez a cada 24 horas.
  
---
- ## 8. Tecnologias Utilizadas
  
  Liste as tecnologias escolhidas para o desenvolvimento do sistema.  
- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Node.js, Express
- **Banco de Dados:** SQLite
- **Autenticação:** JWT (JSON Web Tokens)
  
---
- ## 9. Testes
  
  Descreva os tipos de testes que serão feitos para garantir o funcionamento do sistema.  
- **Testes Unitários:** Testar funções do backend isoladamente.
- **Testes de Integração:** Testar se o frontend, backend e banco de dados estão funcionando corretamente juntos.
- **Testes Funcionais:** Testar se o sistema atende aos requisitos funcionais definidos.
  
---
- ## 10. Plano de Lançamento
  
  Descreva as etapas para colocar o sistema em produção.  
  
	1. **Verificação de Testes:** Certifique-se de que todos os testes passaram.
	2. **Configuração do Ambiente de Produção:** Ajuste as configurações para produção.
	3. **Lançamento Beta:** Lançamento para um grupo pequeno de usuários para testes.
	4. **Ajustes Finais:** Corrigir bugs com base no feedback dos usuários beta.
	5. **Lançamento Oficial:** Colocar o sistema disponível para o público em geral.
---

- ## Conclusão
  
  Essa documentação oferece uma visão clara e estruturada sobre o seu sistema, abordando todos os aspectos necessários, desde os requisitos até o plano de lançamento. Ela deve servir como um guia fácil de seguir para o desenvolvimento do sistema, além de proporcionar clareza para qualquer pessoa que precise entender ou trabalhar no projeto.