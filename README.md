
# Desafio 1 - Planejamento de testes

<b>Estudo exploratório</b>

Para o planejamento dos testes realizei análises no site (https://evento.moblee.com.br/ByKtijSZQ), tendo em vista de que não tenho disponível especificação de requisitos (regras de negócios, interfaces) para me basear. Para isso, explorei o site de forma a encontrar caminhos e fluxos para realização da compra de ingressos. Sendo assim, abaixo descrevo as análises realizadas e métodos adotados para criação dos casos de testes.

Sobre o site

1. Existem linguagens que podem ser selecionadas antes de iniciar o processo de compra, sendo: inglês, português e espanhol.
Nos casos de testes utilizei a linguagem português, no entanto, pode ser necessário executar os casos de testes em cada linguagem para analisar exposição de conteúdo e funcionalidades.

2. Existem caminhos diferentes que chegam no mesmo lugar, neste caso, na compra de ingressos. Sendo: botão “Inscreva-se”, botão “Garanta sua vaga”, botão “Compre o seu ingresso”, botão “Faça sua inscrição”. Para os casos de testes utilizei o botão “Inscreva-se” como caminho principal, todos botões devem apresentar o mesmo resultado, tendo em vista que possuem a mesma funcionalidade, no entanto, também pode ser necessário aplicar os casos de testes utilizando os botões alternativos.

<b>Métodos</b>

1. Para identificar as validações que são feitas em cada formulário, criei uma tabela localizada no diretório `1_planejamento\CamposPorFormulario`, em que analiso o que é verificado em cada campo dos formulários, classificando eles como obrigatório, se há validação, máscara, quantidade mínima e máxima de caracteres. Dessa forma, é possível ter uma visão mais clara dos possíveis casos de testes para validação desses campos. 

2. Fluxos de navegação
Para melhor compreensão sobre todos os possíveis casos de testes, sem a especificação de requisitos, realizei um levantamento descritivo de fluxos em uma especificação de caso de uso, levando em consideração:

    1. Fluxo principal: Acessa por meio do botão “inscreva-se”, seleciona 1 ingresso pago, preenche todos os campos com informações válidas, realiza pagamento com cartão em 1X.
    2. Fluxos alternativos: Pode-se comprar ingressos por meio dos botões: “Garanta sua vaga”, “Compre o seu ingresso” e “Faça sua inscrição”, comprar ingressos pagos via boleto bancário, compra de ingressos pagos por estrangeiro, compra de ingressos gratuitos, aplicação do cupom de desconto, zerar o temporizador no preenchimento do formulário na compra do ingresso pago, zerar o temporizador no preenchimento do formulário na compra do ingresso gratuito.

O arquivo com a especificação de caso de uso está localizado no diretório `1_planejamento\CasoDeUso`.

3. Teste cross-browser

Para realização dos testes optei pelo navegador Chrome por ser amplamente utilizado. No entanto,  é necessário uma análise de quais navegadores são de uso habitual dos clientes, a fim de aplicar os casos de testes em cada um. O intuito de utilizar diferentes navegadores é garantir que o usuário consiga realizar as funções sem enfrentar eventuais problemas.

<b>Casos de testes</b>

Os casos de testes criados estão localizados no diretóro `1_planejamento/casos de testes`, contém um planilha com 24 casos de testes, podendo ser identificados pelo ‘Títuto + CT número sequencial’, cada um especifica um passo a passo para realização dos procedimentos identificados nas etapas anteriores. Na falta da especificação de requisitos, os resultados esperados em alguns casos de testes são exatamente o que o site produz, não sendo possível comparar se está certo ou não.
Na planilha “Caso de testes” existe uma guia com todos os casos de testes chamada “Casos de testes”, nele há os títulos + códigos de totos os casos, contém também o passo a passo de cada um, porém estão ocultos na planilha. Caso haja necessidade, existe uma guia para caso de teste com seus procedimentos, eles estão identificados pelo seus códigos 'CT00X'. 

# Desafio 2 - Execução dos testes

<b>1. Execução dos testes</b>

Os testes foram executados seguindo a ordem dos casos de testes, os registros estão localizados no diretório `2_execucao\ExecucaoDosTestes`. A planilha de registro de execução contém duas guias, “Orientações” e “Relatório de execução”:

1. Orientações: Estão localizadas informações do produto testado e as siglas que utilizei com seu respectivo significado. 
	
2. Relatório de execução: Contém todos os testes e resultado das execuções. A planilha está organizada da seguinte forma: código do teste, o código do caso de teste, o nome, a data de execução, o executor, status (“passou”, “falhou” e “não executado”), quantidade de execuções, código do defeito (referência da planilha com registro de defeitos) e observações.

Os defeitos/falhas encontradas na execução dos testes estão documentadas na planilha “Registro de defeitos” localizado no diretório `2_execucao\RegistoDeDefeitos`. A planilha contém três guias, “Orientações”, “Registro de defeitos” e “Informações Gerais”.

1. Orientações: Contém siglas que utilizei nos registros de defeitos e seu respectivo significado.
	
2. Registro de defeitos: Contém todos os defeitos encontrados e o passo a passo para reprodução. A planilha está organizadas da seguinte forma: Id do defeito (referenciado na planilha de execução de testes), código do caso de teste, descrição do problema, passo a passo, status (em aberto, corrigido), severidade (1,2,3,4), versão, data de abertura e data de fechamento.

3. Informações gerais: Contém informações extraídas do registro de defeitos, tais como: Quantidade de testes planejados, aprovados, falhos e não executados, quantidade de defeitos por severidade e quantidade de defeitos por status. Servem para tirar conclusões dos testes,realizar melhorias nos que não apresentam eficiência, identificar módulos mais dificeis de testar e com dados representativos,pode-se realizar comparações e evolução das versões.


# Desafio 3 - Automação

Para realizar a automação dos testes foi utilizado o Selenium IDE, que é uma extensão para os navegadores Firefox e Chrome. É uma ferramenta de fácil utilização, que permite gravar os testes realizados e executa-los, normalmente usado em testes mais básicos, contudo, pode-se exportar o arquivo e incrementa-los. Na automação utilizei a extensão para o Chrome, o arquivo que contém as instruções de configuração, execução e o arquivo gerado pela ferramenta estão no diretório `3_automacao`.
 






