# CHAVE SSH E TOKEN

## CHAVE SSH 🔑
É uma forma de estabelecer uma conexão segura e incriptada entre duas máquinas, ou seja, vamos nos conectar ao servidor do GITHUB e vamos configurar nossa máquina local como uma máquina confiável para o GITHUB, estabelecendo essa conexão com duas chaves (chave pública e privada).

 - Comando para gerar par de chaves: ssh-keygen -t ed25519 -C "seu e-mail"
 - Comando para visualizar as chaves: cd/c/users/nome/.ssh/ (depois coloque ls para listar as chaves)
 - Comando para visualizar o conteúdo das chaves: cat id_ed25519.pub
 - Comando para inicializar a chave ssh: eval $(ssh-agent -s)
 - Comando para entregar nossa chave para entidade: ssh-add id_ed25519


## TOKEN DE ACESSO PESSOAL 🔐
O token de acesso pessoal serve como uma forma segura de autenticação para clonar um repositório através do caminho HTTPS .

Instruções: 

 - Gere um token no seu perfil do GITHUB e guarde em sua máquina. Sempre que fizer um commit, o Git pedirá um usuário e senha para você. Quando for por a senha, ao invés de colocar a senha de login, você utilizará o token de acesso pessoal para confirmar que você é o autor.
 - Comando para clonar repositório (caminho ssh): git clone "caminho ssh" (depois confirme com yes)
 - Comando para clonar repositório (caminho https): git clone "caminho https" (depois coloque seu login e token de acesso pessoal)
