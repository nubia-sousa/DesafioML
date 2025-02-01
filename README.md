# DesafioML
Desafio de projeto de Machine Learning do Curso Fundamentos de IA

Abra o https://portal.azure.com/?azure-portal=true, selecione Entrar no canto superior direito da tela. Use o e-mail e a senha associados à sua assinatura do Azure para entrar.
selecione Criar um novo recurso no menu lateral esquerdo. 
No campo de pesquisa, digite Machine Learning
Na página Marketplace, selecione Azure Machine Learning
Na página Criar um recurso
, configurar vários detalhes para criar seu recurso. Configure-o com as seguintes configurações:
o	Assinatura : sua assinatura do Azure .
o	Grupo de recursos : selecione ou crie um grupo de recursos com um nome exclusivo .
o	Região : Escolha qualquer região disponível. Se estiver no leste dos EUA, use “East US 2” .
o	Nome : Insira um nome exclusivo .
o	Nível de preço : F0 grátis
Selecione Examinar + Criar e revise a configuração. Em seguida, selecione Criar. A tela indicará quando a implantação estiver concluída.
Quando a implantação estiver concluída, selecione Ir para o Recurso, e em seguida Lauch Studio, retornando para o Safety Content Studio.
No menu lateral esquerdo, selecione ML Automatizado e em seguida Novo Trabalho de ML Automatizado
Crie um novo trabalho de ML automatizado com as seguintes configurações, usando Avançar conforme necessário para avançar pela interface do usuário:
Configurações básicas :
o	Nome do trabalho : O campo Nome do trabalho já deve estar preenchido previamente com um nome exclusivo. Mantenha-o como está.
o	Novo nome do experimento :mslearn-bike-rental
o	Descrição : Aprendizado de máquina automatizado para previsão de aluguel de bicicletas
o	Marcas : nenhuma
Tipo de tarefa e dados :
o	Selecione o tipo de tarefa : Regressão
o	Selecionar dados: Crie um novo conjunto de dados com as seguintes configurações:
o	Tipo de dados :
	Nome :bike-rentals
	Descrição :Historic bike rental data
	Tipo : Tabela (mltable)
o	Fonte de dados :
	Selecione De arquivos locais
o	Tipo de armazenamento de destino :
	Tipo de armazenamento de dados : Azure Blob Storage
	Nome : workspaceblobstore
o	Seleção de MLtable :
	Pasta de upload : Baixe e descompacte a pasta que contém os dois arquivos que você precisa enviar https://aka.ms/bike-rentals
Selecione Criar . Após a criação do conjunto de dados, selecione o conjunto de dados bike-rentals e em seguida Avançar.
Configurações da tarefa :
o	Tipo de tarefa : Regressão
o	Conjunto de dados : bike-rentals
o	Coluna de destino : rentals (integer)
o	Configurações adicionais :
o	Métrica primária : NormalizedRootMeanSquaredError
o	Explique o melhor modelo : Não selecionado
o	Habilitar empilhamento de conjunto : Não selecionado
o	Usar todos os modelos suportados : Não selecionado. Você restringirá o trabalho para tentar apenas alguns algoritmos específicos.
o	Modelos permitidos : Selecione apenas RandomForest e LightGBM — normalmente você tentaria o máximo possível, mas cada modelo adicionado aumenta o tempo necessário para executar o trabalho.
o	Limites : Expandir esta seção
o	Máximo de avaliações :3
o	Máximo de avaliações simultâneas :3
o	Máximo de nós :3
o	Limite de pontuação métrica : 0.085
o	Tempo limite do experimento :15
o	Tempo limite de iteração :15
o	Habilitar rescisão antecipada : Selecionado
o	Validação e teste :
o	Tipo de validação : Divisão de validação de treinamento
o	Porcentagem de dados de validação : 10
o	Conjunto de dados de teste : Nenhum
Computação :
o	Selecione o tipo de computação : Sem servidor
o	Tipo de máquina virtual : CPU
o	Camada de máquina virtual : Dedicada
o	Tamanho da máquina virtual : Standard_DS3_V2*
o	Número de instâncias : 1
* Se sua assinatura restringir os tamanhos de VM disponíveis para você, escolha qualquer tamanho disponível.
Envie o trabalho de treinamento. Ele inicia automaticamente.
Espere o trabalho terminar. Pode levar um tempo 
