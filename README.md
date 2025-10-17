# Desafio-T-cnico-Quality-Assurance-na-Lacrei-Sa-de
Desafio da Lacrei com casos de teste
  
Caso de teste login de usuário
Funcionalidade: Login no sistema
Cenário: Usuário já tem cadastro.
Given que o usuário está na página de login
When preenchido o campo E-mail e Senha incorretamente
Then aparece a mensagem "E-mail ou senha incorretos. Esqueceu a sua senha? Clique em "Esqueci minha senha" para recuperá-la."
  
Caso de teste cadastro de usuário
Funcionalidade: Cadastro no sistema
Cenário: Usuário se cadastra com o botão criar conta
Given que o usuário está na página de login
When clicado no botão "Criar conta"
Then é redirecionado para página de cadastro para criar a conta
  
Caso de teste preenchimento de dados
Funcionalidade: Cadastro de usuário
Cenário: Preencher todos os campos com suas regras especificas e dados validos
Given os campos 'nome', 'sobrenome', 'e-mail', 'confirme e-mail', 'senha', 'confirme senha'
And os campos a serem marcados 'Li e concordo com os termos' e ' Tenho 18 anos ou mais'
When todos preenchidos corretamente validos
Then o botão 'Cadastrar' vai aparecer para clicar
And o usuário receberá um e-mail para confirmar cadastro
And ao clicar no link é redirecionado para o para página de login
And preenchido os dados certo é redirecionado para página de boas vindas com um botão 'Continuar cadastro'
  
Caso de teste continuação de cadastro
Funcionalidade: usuário vai preencher todos seus dados
Cenário são feitas 5 perguntas múltipla escolha para serem selecionadas
Given a página de boas vindas com o botão 'Continuar cadastro'
When clicar no botão 'Continuar cadastro' é redirecionado para o campo com 5 perguntas
And contem os títulos de 'pronome', 'etnia', 'gênero', 'sexualidade' e 'deficiência'
Then cada uma é marcada como a preferência de cada usuário
And clicando no botão 'Concluir'
And redirecionado para página 'Cadastro foi concluído'
  
Caso de teste Buscar profissional
Funcionalidade: encontrar profissional de sua preferência
Cenário: ao clicar no botão 'Buscar profissional' um campo onde você pode escolher o profissional
Given a tela de boas vindas com um campo onde você pode digitar e escolher o profissional da área de saúde
When digitar o médico ele te dará as opções
Then quando o usuário selecionar o médico ele deve agendar um horário e dia
  
Caso de teste Edição de perfil: inserir e atualizar informações
Funcionalidade: Permite você trocar seus dados
Cenário: na página de perfil você consegue ver todos seus dados e tem a opção de editar
Given suas informações na página de perfil
When o usuário clicar em 'Editar dados' 
Then redirecionar numa página onde contem todos os dados que podem ser mudados
And terá o campo 'data de nascimento' para preencher
And no final o botão de 'salvar'
And será redirecionado para página de perfil novamente
  
Caso de teste Recuperação de senha: fluxo completo de esqueci minha senha
Funcionalidade: o usuário precisa de uma senha nova
Caso de teste: usuário precisa gerar uma nova senha para fazer login novamente
Given página principal de login
And opção 'esqueci minha senha'
When o usuário clicar no 'esqueci minha senha'
Then é redirecionado para a página de redefinir senha
And um campo para colocar seu e-mail aparecerá
And clicando no botão 'enviar link' você recebera um e-mail
And será redirecionado e enviado a nova senha
______________________________________________________________________________________

Registro de Teste de Desempenho
Tempo de resposta nas operações críticas (ex.: cadastro e busca de profissional)
Ferramenta sugerida: Lighthouse

Given site https://paciente.lacreisaude.com.br na aba anonima
When feito os teste na tela cadastro
And busca profissional
And usando a ferramenta Lighthouse
Then os resultados encontrados foram registrados na planilha
_____________________________________________________________________________________

Teste de Carga com Apache JMeter

**Configuração do teste:**
- 30 usuários simultâneos
- Ramp-up: 30 segundos
- 10 repetições
- Endpoint: `https://paciente.lacreisaude.com.br`

**Resultados principais:**

| Métrica | Valor |
|----------|-------|
| Total de requisições | 300 |
| Avarege | 0 |
| Erros (%) | 100% |
| Throughput | 10.4 req/s |
| Avg. Bytes | 1126.0 |

*Print dos dados apresentado na tabela do link ao final*


