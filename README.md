P07_Algaworks_ebook-jsf-financeiro
==================================
testado e funcionando

originalmente pego do GitHub em:
https://github.com/algaworks/ebook-jsf-financeiro/tree/master/src/main/java/com/algaworks/financeiro/util
Thanks para Algaworks ! Muito bom !

para manipular no Git:
1) Clonar local: http://www.gujavasc.org/2013/08/03/clonar-um-projeto-do-github-com-o-plugin-egit-para-o-eclipse/
2) Exportar para GitHub: http://blog.camilolopes.com.br/usando-o-git-no-eclipse/
3) url local de acesso:
mudei o contexto para P07
http://localhost:8080/P07/Login.xhtml

originalmente era:
http://localhost:8080/ebook-jsf-financeiro/Login.xhtml

Login: admin
pw: 123

para funcionar:

1) ir no persistente.xml e mudar o acesso para o MySQL (user e pw);

2) criar 2 tabelas no MySQL

    a) lancamento
    
    CREATE TABLE `lancamento` (
      `id` bigint(20) NOT NULL AUTO_INCREMENT,
      `pessoa_id` bigint(20) NOT NULL,
      `descricao` varchar(80) NOT NULL,
      `tipo` varchar(255) NOT NULL,
      `valor` decimal(10,2) DEFAULT NULL,
      `data_pagamento` date DEFAULT NULL,
      `data_vencimento` date DEFAULT NULL,
      PRIMARY KEY (`id`)


    b) pessoa
    
    CREATE TABLE `pessoa` (
      `id` bigint(20) NOT NULL AUTO_INCREMENT,
      `nome` varchar(60) NOT NULL,
      PRIMARY KEY (`id`)


