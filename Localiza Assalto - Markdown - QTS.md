### Página de Login

Funcionalidade: 
Entrar ou Cadastrar-se no site


Contexto: 
    Dado que usuário não possui cadastro no sistema

Cenário: Cadastro de conta
    E usuário preenche todas as informações do formulário obrigatórias corretamente
Quando aciona a opção de "Cadastrar"
Então obtém sua conta
E é redirecionado para a área de Login


Contexto:
    Dado que o usuário possui cadastro no sistema

Cenário: Login válido  
    E usuário preenche o formulário com credenciais válidas
Quando ele aciona a opção "Entrar"
Então é redirecionado para a página Home

Cenário: Login com credenciais incorretas
    E o usuário preenche o formulário com credencias inválidas
Quando ele aciona a opção "Entrar"
Então deve ser exibida uma mensagem "Email ou senha inválidos" 
E o usuário deve preencher as credenciais novamente

Cenário: Usuário esqueceu sua senha
    E o usuário preenche o formulário com a senha incorreta
Quando ele aciona a opção "Entrar"
Então deve ser exibida uma mensagem "Senha incorreta"
Quando o usuário acionar a opção "Esqueci minha senha"
Então o usuário pode criar uma nova senha 
E é redirecionado para a área de login

### Página de Contato

Funcionalidade: Entrar em Contato

Contexto: 
    Dado que o usuário está preenchendo o formulário.

Cenário: Contato válido
    E usuário preenche todos os campos
Quando ele aciona o botão "enviar"
Então nos envia uma mensagem. 

Cenário: Contato inválido
    E usuário deixou um o mais campos vazios
Quando ele aciona o botão "enviar" 
Então deve ser exibida uma mensagem "Preencha o campo vazio"
    
### Página de Assalto

Funcionalidade: Registrar um Assalto

Contexto: 
    Dado que o usuário está logado
E tenta registrar um assalto

Cenário: Assalto registrado com sucesso
    E usuário aciona o botão "Registrar Assalto"
E usuário preenche todos os campos
Quando ele aciona o botão "registrar"
Então o assalto é registrado com êxito 
E exibe uma mensagem "Assalto Registrado."
    
Cenário: Assalto não registrado
    E usuário aciona o botão "Registrar Assalto"
E usuário não preenche todos os campos corretamente 
Quando ele aciona o botão "Registrar"
Então exibe uma mensagem "Preencha os campos corretamente"
    
Contexto: 
    Dado que o usuário não está logado
E tenta registrar um assalto
    
    Cenário: Assalto não registrado
    E usuário aciona o botão "Registrar Assalto"
Então exibe uma mensagem "É preciso estar logado"
E é redirecionado para a área de Login/Cadastro
    
    



