# kabug-rb
Repositório do projeto Kabug com Cucumber, Capybara e Ruby.


## Como executar o projeto

* Importante ter o Ruby instalado (versão 2.5 ou superior)

### Instalar o Bundler
'
gem install bundler
'

### Instalar as dependencias do ruby (projeto)
'
bundle install
'

### Executar localmente (minha maquina)
'
bundle exec cucumber
'

### Executar no servidor de CI (Jenkins) gerando reports JSON
'
bundle exec cucumber -p ci
'
