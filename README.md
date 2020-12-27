## Portal Noticias

### Portal Noticias
<!--ts-->
   * [Sobre](#Sobre)
   * [Instalação](#Instalação)
   * [Baixar_Projeto](#Baixar_Projeto)
   * [Executar_Projeto](#Executar_Projeto)
   * [Autor](#Autor)
<!--te-->

# Sobre
Portal de Noticias contém um formulário de inclusão de noticias uma, home com as 5 noticias mais novas, uma aba noticias com todas as noticias e uma aba com o detalhe da noticia.
O projeto foi feito utilizando Node, JavaScript, HTML e CSS.
Com o intuito de aprender a Linguagem node, foi utilizado neste projeto as seguintes dependencias:
    "body-parser": "^1.17.2",
    "consign": "^0.1.6",
    "ejs": "^2.5.6",
    "express": "^4.15.3",
    "express-validator": "3.2.0",
    "mysql": "^2.13.0"


# Instalação
	Para a execução do projeto será necessário ter instalado o Node, em sua máquina, que pode ser baixado no link abaixo:
	https://nodejs.org/en/download/
	Neste link será sugerido a versão compatível  com sua máquina, basta baixar e instalar.
	Será necessário também ter o MySQL, que pode ser baixado em: https://dev.mysql.com/downloads/  
	Ao entrar no link acima, basta baixar a versão compatível com o seu sistema operacional e instalar.

# Baixar_Projeto
	Para baixar o projeto basta ter o git instalado na sua maquina, caso não tenha baixe-o em: https://git-scm.com/downloads e instale, lembrando sempre de escolher a versão compativel com o seu S.O.
	Crie uma pasta onde ficará o projeto.
	Execute o Git Bash e navegue até à pasta criada
	Já na pasta, basta colocar o comando: git clone  https://github.com/dougrgarcia/PortalNoticias.git

# Executar_Projeto
#### Para executar o projeto deve ter um banco de dados chamado "portal_noticias" com o usuário "root" senha "1234" criado, assim como a tabela "noticias".
	Para criar o banco de dados, deve abrir o CMD, e navegar pelo caminho de instalação do MySQL até o diretório "/bin".

	Depois deve acessar o client com o usuário root usando o comando abaixo;
	mysql -h localhost -u root -p
	Após apertar o enter, será solicitado a senha, deve digitar "1234" e apertar o enter.

	Agora pode crair o banco de dados conforme abaixo:
	create database portal_noticias;

	Abra o banco de dados:
	use portal_noticias;

	E por fim crie e tabela noticias:
	CREATE TABLE `noticias` (
	  `id_noticia` int NOT NULL AUTO_INCREMENT,
	  `titulo` varchar(100) DEFAULT NULL,
	  `noticia` text,
	  `data_criacao` timestamp NULL DEFAULT CURRENT_TIMESTAMP,
	  `autor` varchar(200) DEFAULT NULL,
	  `data_noticia` date DEFAULT NULL,
	  `resumo` varchar(200) DEFAULT NULL,
	  PRIMARY KEY (`id_noticia`)
	) ENGINE=InnoDB AUTO_INCREMENT=5 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

#### Para subir o projeto, basta executar os passos abaixo:
	Navegar até a pasta onde está o projeto.
	executar o comando: npm install
	depois: nodemon app

# Autor
#### Douglas Rodrigues Garcia
#### e-mail: dougrgarcia92@gmail.com
