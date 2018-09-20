Proposta: Criar um componente funcional de Joomla que permita o cadastro de clientes com os seguintes dados:

• Nome
• Sobrenome
• CPF
• Endereço
• Email
• Telefone
• Foto

O nome e sobrenome serão campos simples de texto, o CPF deverá contar com máscara no campo de texto e checagem simples do dígito verificador do CPF, o endereço deverá ser preenchido via webservice, o cliente deverá informar o CEP e o endereço irá se auto completar, email deverá ter checagem simples, telefone deverá ter máscara para nove dígitos, foto é uma imagem enviada pelo usuário.

Considerações: 
• Endereço: Tomar cuidado com CEP’s de município onde um só CEP abrange uma localidade e não uma rua.  Utilizar o webservice gratuito do site https://viacep.com.br/, pode integrar usando JS direto no site viacep ou utilizar JS para consultar o controlador do teu componente que por sua vez irá abrir uma requisição para o viacep via CURL e retornar por AJAX ao browser.
• CPF: verificar o digito verificador utilizando javascript, utilizar AJAX para consultar via controlador do seu componente se este CPF já está cadastrado, se já estiver avisar o usuário que já existe cadastro na base de dados.
• FOTO:deverá permitir o recorte para 640x640px fixos. O usuário irá recortar a imagem e somente a porção recortada será enviada ao servidor. A foto deverá ser gravada no diretório media/nomedoseucomponente/IDDOCADASTRO/foto. Utilizar qualquer script de JS para efetuar o corte NO BROWSER.
• Email: checagem simples via JS (regex) para conferir se há um email válido no campo.
• Requisições de AJAX efetuadas do browser para o componente deverão ser feitas EXCLUSIVAMENTE no controlador, visto que o padrão do Joomla é MVC, do mesmo modo NÃO efetue ações de modelo na visualização por exemplo. Cada código deve ir no seu devido lugar e organizado. Existem vários formatos de controlador no Joomla, normalmente para ajax é utilizado um controlador do tipo raw para retornar objetos JSON por exemplo, bastar colocar a extensão .raw.php no controlador, há documentação vasta sobre como fazer.
• Favor consultar as funções do framework do Joomla SEMPRE antes de inventar qualquer coisa, existe muita coisa pronta no framework, incluindo abstração de banco de dados, funções para tratar requests, geração de código HTML, layouts repetitivos, bibliotecas de CSS e JS etc…

Instruções básicas:

• Baixar e Instalar na máquina local a versão mais estável mais atual do CMS Joomla em joomla.org
• Utilizar um criador de componentes para Joomla, para gerar o esqueleto básico do componente recomendamos o component-creator.com, basta criar uma conta gratuita e utilizar.
• Ao criar o componente, levar em consideração e planejar o banco de dados, para que contenha colunas suficientes para os dados a serem cadastrados mais uma coluna chamada ID que atuará como chave primária. O CPF também deverá conter valores únicos
• Instalar o componente em sua instalação local.
• Desenvolver o exercício proposto APENAS NA TELA DE FRONT-END, a tela de administração é desejável que esteja funcional, porém não é o foco desde exercício.
• Utilizar Boostrap v3 para criar a grid do formulário.
• Para checagens via JS nos campos que requerem este tipo de funcionalidade, favor utilizar JS, jQuery ou preferencialmente jQuery Validator, um plugin especifico para isso que já está embutido no Joomla.
• Ao final, criar um backup do Joomla utilizando akeeba backup, renomear o arquivo de backup para seu nome e sobrenome, enviar o arquivo JPA para avaliação.

Qualquer dúvida esclarecer EXCLUSIVAMENTE por email, alexandre@isidora.com.br

Prazo: de entrega: 20/09 as 18h
Forma de entrega: link de GitHub, Wetransfer ou dropbox.
