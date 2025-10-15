# Desafio-T-cnico-Quality-Assurance-na-Lacrei-Sa-de
Desafio da Lacrei com casos de teste

Caso de teste login de usuário
Funcionalidade: Login no sistema
Cenário: Usuário já tem cadastro.
Dado que o usuário está na página de login
Quando preenchido o campo E-mail e Senha incorretamente
Então aparece a mensagem "E-mail ou senha incorretos. Esqueceu a sua senha? Clique em "Esqueci minha senha" para recuperá-la."


Caso de teste cadastro de usuário
Funcionalidade: Cadastro no sistema
Cenário: Usuário se cadastra com o botão criar conta
Dado que o usuário está na página de login
Quando clicado no botão "Criar conta"
Então é redirecionado para página de cadastro para criar a conta


Caso de teste preenchimento de dados
Funcionalidade: Cadastro de usuário
Cenário: Preencher todos os campos com suas regras especificas e dados validos
DADO os campos 'nome', 'sobrenome', 'e-mail', 'confirme e-mail', 'senha', 'confirme senha'
E os campos a serem marcados 'Li e concordo com os termos' e ' Tenho 18 anos ou mais'
Quando todos preenchidos corretamente validos
Então o botão 'Cadastrar' vai aparecer para clicar
E o usuário receberá um e-mail para confirmar cadastro
E ao clicar no link é redirecionado para o para página de login
E preenchido os dados certo é redirecionado para página de boas vindas com um botão 'Continuar cadastro'

Caso de teste continuação de cadastro
Funcionalidade: usuário vai preencher todos seus dados
Cenário são feitas 5 perguntas múltipla escolha para serem selecionadas
Dado a página de boas vindas com o botão 'Continuar cadastro'
Quando clicar no botão 'Continuar cadastro' é redirecionado para o campo com 5 perguntas
E contem os títulos de 'pronome', 'etnia', 'gênero', 'sexualidade' e 'deficiência'
Então cada uma é marcada como a preferência de cada usuário
E clicando no botão 'Concluir'
E redirecionado para página 'Cadastro foi concluído'

Caso de teste Buscar profissional
Funcionalidade: encontrar profissional de sua preferência
Cenário: ao clicar no botão 'Buscar profissional' um campo onde você pode escolher o profissional
Dado a tela de boas vindas com um campo onde você pode digitar e escolher o profissional da área de saúde
Quando digitar o médico ele te dará as opções
Então quando o usuário selecionar o médico ele deve agendar um horário e dia

Caso de teste Edição de perfil: inserir e atualizar informações
Funcionalidade: Permite você trocar seus dados
Cenário: na página de perfil você consegue ver todos seus dados e tem a opção de editar
Dado suas informações na página de perfil
Quando o usuário clicar em 'Editar dados' 
Então redirecionar numa página onde contem todos os dados que podem ser mudados
E terá o campo 'data de nascimento' para preencher
E no final o botão de 'salvar'
E será redirecionado para página de perfil novamente

Caso de teste Recuperação de senha: fluxo completo de esqueci minha senha
Funcionalidade: o usuário precisa de uma senha nova
Caso de teste: usuário precisa gerar uma nova senha para fazer login novamente
Dado página principal de login
E opção 'esqueci minha senha'
Quando o usuário clicar no 'esqueci minha senha'
Então é redirecionado para a página de redefinir senha
E um campo para colocar seu e-mail aparecerá
E clicando no botão 'enviar link' você recebera um e-mail
E será redirecionado e enviado a nova senha
