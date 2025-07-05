## Login - Entrar no Software:
1. Inicia a execução do usuário.
2. Renderiza a página de login.
3. Aceita comandos do usuário para navegar entre as opções.

## Login - Sair do Softare:
1. Executa a função quit().

## Gerenciar tarefas - Adicionar:
1. Pega o título da tarefa a ser adicionada.
2. Pega o nome da lista selecionada atualmente
3. Percorre o banco de dados até entrar dentro da tag dela.
4. Cria uma nova tarefa (task_[number+1]) dentro da tag dela.
	a. Pra fazer isso ela escreve uma série de novas tags dentro dessa task: task_title, status, priority, detail, subtasks.
	b. O usuário preenche esses dados, com exceção do task_title, depois de criar ela.
	c. Guarda esses dados preenchidos em um dicionário e escreve no banco de dados .xml.
5. Dá um refresh na tela da aplicação.

## Gerenciar tarefas - Remover:
1. Pega o título da tarefa a ser removida.
2. Pega o nome da lista selecionada atualmente.
3. Percorre todas as tags que representam tasks dentro dela.
4. Apaga a que tem o seu título correspondente ao do escolhido pelo usuário.
5. Dá um refresh na tela da aplicação.

## Gerenciar Tarefas - Editar:
1. Pega o título da tarefa a ser editada.
2. Pega o nome da lista selecionada atualmente.
3. Percorre todas as tags que representam as tasks dentro dela e posiciona a agulha logo na tag da task a ser editada.
4. Abre um menu de edição (igual o menu de configuração da primeira vez)
5. Aguarda as edições feitas pelo usuário.
6. Captura essas edições dentro de um dicionário.
7. Escreve todas as edições no banco de dados .xml.
8. Dá um refresh na tela da aplicação.

## Gerenciar lista de Tarefas - Adicionar:
1. Abre um prompt pedindo o título da lista a ser adicionada.
2. Guarda esse valor dentro de uma variável.
3. Percorre o banco de dados .xml procurando o nome da lista acima, se não houver, ele só adiciona uma nova mesmo.
4. escreve uma nova tag com o seguinte modelo: <list_[nameList]></list_[nameList]>.
5. Dá um refresh na tela da aplicação.

## Gerenciar Lista de Tarefas - Remover:
1. Captura o nome da lista selecionada.
2. Percorre o banco de dados dentro da tag <data></data>.
3. Apaga por completo a tag que contém o nome no seguinte padrão <list_[nameList]></list_[nameList]>
4. Dá um refresh na tela da aplicação.

## Gerenciar Lista de Tarefas - Editar:
1. Captura o nome da lista selecionada.
2. Percorre o banco de dados dentro da tag <data></data>.
3. Edita o título da lista e/ou posição que ela ocupa dentro do documento.
