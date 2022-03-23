Site catálogo de Filmes

** Comando inicial para a criação do site:
composer create-project drupal/recommended-project catalogo-filmes

** Não consegui instar o drupal apartir do composer -> Banco de dados e senha
-- è possivel? 

**Instalando o admin toobal para facilitar a nevegação do site

composer require drupal/admin_toolbar

** Instalando o Drush 

composer global require drush/drush:11.X

** Iniciando o GIT 

git init

** Conectando ao repositorio 

git remote add orinig https://github.com/andrepaffrath/catalogo-filmes.git

** Verificando o statust

git status

** Adicionando o projeto ao git 

git add .

** Comitando 

git commit -M "Criação do CSS e Alteração Bloco e Menu"

** Criando a branch 

git branch -M main

** Publicando a versão

git push -u origin main

** Instalando bootstrap para criação do theme

composer require drupal/bootstrap

** Realizar as copias dos arquivos conforme orientação do theme

** Ir no site do drupal e instalar o theme criado

http://localhost/catalogo-filmes/web/admin/appearance

** Iniciando a customização do css

** Baixamos o Sass do bootstrap 

https://getbootstrap.com/docs/3.4/getting-started/#download

Incluimos na pasta do thema com o nome de bootstrap

** Compilando o scss com o kolala

Incluido a compilação na pasta css


** Após a criação do css vamos publicar no git a versão 1.1

git add .


** Alteramos o menu criando os catalogos dos filmes 

** Alteramos os blocos para exibir apenas o menu principal no topo de site

** Criado a pasta config para armazenar as configurações do drupal

drush cex

** Configurando o debug no twig  - alterar o arquivo settings.php


if (file_exists($app_root . '/' . $site_path . '/settings.local.php')) {
   include $app_root . '/' . $site_path . '/settings.local.php';

}

** Criado o arquivo settings.local.php copiado de example.settings.local.php

** Alterando o arquivo development.services.yml para gerar as tags de confguração

para 

parameters:
  http.response.debug_cacheability_headers: true
  twig.config:
    debug: true
services:
  cache.backend.null:
    class: Drupal\Core\Cache\NullBackendFactory



** Limpando o cache para atualizar o site

drush cr

** Limpando cache do git 

git rm -r --cached .


** Instalando o paragraphs para melhor adquação do layout

composer require drupal/paragraphs

http://localhost/catalogo-filmes/web/admin/modules

	






















