# Resolvendo o vínculo de 500+ contatos no Supabase com Python
Criei esse script para resolver um problema real que tive no meu projeto de sistema de cashback. Eu tinha os clientes cadastrados no banco de dados (Supabase), mas os telefones estavam em uma planilha separada. Precisava ligar um ao outro usando o ID do banco, e fazer isso na mão seria impossível.

# O que eu usei:
Python (Pandas): Usei para fazer o "PROCV" inteligente entre as tabelas.

Google Colab: Onde rodei todo o código.

Supabase: Meu banco de dados onde os dados finais foram parar.

# O que o projeto faz:
O maior desafio aqui foi que os nomes na planilha de telefones nem sempre batiam 100% com o banco (tinha espaço sobrando, letra maiúscula, etc).

O script faz o seguinte:

Limpa os nomes tirando espaços vazios que atrapalham o cruzamento.

Faz um Merge (união) das tabelas. O Python olha o nome do cliente na planilha, acha o ID dele no banco e "cola" um do lado do outro.

Remove os números duplicados para o banco de dados não dar erro na hora de subir.

Gera um arquivo CSV prontinho só para importar no Supabase.

# Resultado:
Consegui organizar mais de 500 contatos de uma vez só. Agora, cada telefone está vinculado ao ID certinho do cliente. Isso é fundamental para a minha próxima etapa: criar a automação que vai mandar mensagem avisando que o cashback expirou!
No começo apanhei um pouco para os nomes que estavam diferentes nas duas planilhas, tive que ir testando e ajustando o script para funcionar.
O script me economizou muito trabalho, em outro projeto não sabia como fazer o script e fiz limpeza em telefones manualmente para deixar no padrao 55.
