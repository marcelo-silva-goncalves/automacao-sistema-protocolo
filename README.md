# PROJETO DE AUTOMATIZAÇÃO DE ACOMPANHAMENTO DE PROCESSOS ELETRÔNICOS

![Gif inicial](https://user-images.githubusercontent.com/74038190/241765440-80728820-e06b-4f96-9c9e-9df46f0cc0a5.gif)

Este projeto visa automatização da tarefa de acompanhamento de processos eletrônicos no sistema de protocolo do Governo do Estado do Pará.

O objetivo foi de trazer maior produtividade na rotina de trabalho, impactando diretamente no tempo de execução desta tarefa, o que resultou em uma redução de 60 minutos para 8minutos.

A execução do script é específica para a atividade realizada na Secretaria de Estado de Planejamento - SEPLAD, contudo, podem ocorrer adaptações ou inspiração para aplicação em outras rotinas administrativas similares a do projeto.

## Índice 📝

- [Visão Geral](#Visão-Geral)
- [Metodologia](#Metodologia)
- [Requisitos](#Requisitos)
- [Contribuições](#Contribuições)
- [Licenças](#Licenças)
- [Créditos](#Créditos)

## Visão Geral 🔎

O projeto de automação de acompanhamento de processos eletrônicos no sistema de protocolo do Governo do Estado do Pará foi desenvolvido com o propósito de automatizar as rotinas de acompanhamento de processos de contratações para a Diretoria de Administração e Finanças, vinculada à SEPLAD.

O tempo é um recurso valioso e que precisa ser usado para, em nivel de Diretoria, focar em soluções e inovações que podem ser aplicadas na gestão.

O objetivo da automatização foi de trazer maior produtividade na rotina de trabalho, com o uso da linguagem Python, impactando diretamente no tempo de execução desta tarefa, garantindo assim que o tempo de trabalho seja dispendido em questões estratégicas.

A disponibilização do projeto e dos scripts é benéfico à comunidade que trabalha com automação e dados. Contudo, pode ser necessário adaptações para aplicação em outras rotinas administrativas similares a do projeto.

Inicia-se com o script "leitura_google_sheets.ipynb", que realiza a leitura da planilha contendo informações essenciais dos processos a serem acompanhados. O acesso ao Google Sheets é feito através da API, e ao final dessa etapa, um arquivo Excel é gerado a partir dos dados da planilha.

Em seguida, o script "acesso_sistema_protocolo.ipynb" automatiza o login no sistema de protocolo, utilizando a biblioteca Selenium para inserir automaticamente os dados dos processos em campos específicos. Durante esse processo também ocorre a extração das informações sobre em qual setor cada processo se encontra, utilizando técnicas de Web Scraping.

É importante ressaltar que em ambas as etapas, existe o processo de ETL para adequar os dados ao formato esperado pelo sistema de protocolo. Além disso, durante o script de acesso ao sistema, ocorre a conversão de DataFrame do Pandas para o formato Excel.

Por fim, o script "atualizar_localizacao_processos_sheets.ipynb" realiza a atualização do setor na planilha do Google Sheets e gera uma planilha gerencial que é entregue diariamente ao Diretor do setor.

O script "atualizacao.ipynb" realiza a importação dos scripts ora mencionados a fim de rodar todas as etapas.

Os principais resultados obtidos através desse projeto de automação são:

- Aumento da produtividade diária: após automação do acompanhamento dos processos prioritários, houve a redução de 60min para 8min no processo de pesquisa e locação. Redução de aproximadamente 75% de tempo gastos com a aplicação da automação.

- Aprimoramento do gerenciamento: ocorreu a melhora no processo de acompanhamento dos processos, conferindo celeridade aos processos quando estes estão dentro do organograma da Diretoria de Administração e Finanças.

- Suporte aos demais setores: além dos benefícios ora apontados, a planilha de gerenciamento também deu maior celeridade junto as demais unidades administrativas da SEPLAD visto o acompanhamento dos processos.

## Metodologia 📝

A metodologia e as etapas aplicadas ao projeto são:
Quando você automatiza um processo, geralmente segue uma metodologia que envolve as seguintes etapas:

1. Análise e Planejamento: identificação das etapas da automatização do acompanhamento dos processos, que darão suporte a fase de codificação; 

2. Design da Automação: com base na análise, projetou-se a solução da automação. A escolha da linguagem Python, além de ser estratégica por ser open source, facilitou o processo de arquitetura dos scripts e da automação. 

3. Desenvolvimento: escrita dos scripts para integração das plataformas necessárias ao processo de automação, a saber, planilha presente no Google Sheets e sistema web de protocolo. 

4. Testes e Validação: realização de testes para implantar a automação, validar tempo de carregamento web para aprimoramento dos scripts.
Além disso, foi fundamental verificar se os dados foram transformados para aceitação no processo de input no sistema de protocolo, visto a existência de duas versões de protocolo - PAE 3.0 e PAE 4.0.

5. Implantação: após passar pelos testes e validações, ocorreu a automação do processo de acompanhamento de processos apenas ao nível local, ou seja, os scripts rodam em um computador específico.

6. Monitoramento e Manutenção: uma vez que a automação está em execução, o monitoramento ocorre instantaneamente, visando garantir o seu pleno funcionando. Isso inclui o monitoramento de logs, o gerenciamento de erros e a resolução de problemas conforme necessário. Além disso, podem ser necessárias atualizações e melhorias ao longo do tempo para manter a eficiência e a eficácia da automação;

7. Documentação: Durante todo de construção dos scripts, houve o cuidado de realizar citações para que terceiros consigam entender a dinâmica da construção do código;

8. Avaliação Contínua: Visto que as plataformas utilizadas não são gerenciadas pela Secretaria, automação é avaliada continuamente para garantir que ela atenda aos objetivos estabelecidos. À medida que as necessidades mudam ou novos requisitos surgem, ajustes na automação poderão ser necessários.

## Requisitos 💻

- Python 3.6 ou superior
- OS
- Pandas
- google-api-python-client
- Time
- Csv
- Ipynb
- Selenium
- Sistema Git

## Contribuições 🗂️

Fique à vontade contribuir para o aprimoramento do mesmo. Para fazer isso, realize os procedimentos básicos a seguir:

1. Configure o nome de usuário para seus commits: git config --global user.name "seu nome"
2. Defina o e-mail do usuário para seus commits: git user.email "seuemail@email.com"
3. Inicie um repositório Git em um diretório existente: git init
4. Clone o repositório deste projeto: git clone https://github.com/marcelo-silva-goncalves/analise-campanha-marketing
5. Renomeie a branch para "main" (o padrão é "master"): git branch -m main
6. Verifique a presença de arquivos modificados no seu diretório local: git status
Adicione o arquivo para o estado de preparo, a fim de ser commitado: git add nomedoarquivo.ipynb
7. Registre uma mensagem sobre o arquivo alterado: git commit -m "mensagem que descreve o commit"
8. Submeta as alterações para o repositório no GitHub: git push
9. Caso ocorra um conflito entre as versões local e remota do repositório, use git pull para sincronizar as alterações antes de enviar as suas: git pull

## Licenças 📑

Este projeto está licenciado sob a licença MIT. Para obter mais informações clique [aqui](https://docs.github.com/pt/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository#disclaimer).

## Créditos 🔗

- [Etapas para ativação da API do Google Sheets](https://developers.google.com/sheets/api/quickstart/python?hl=pt-br)
- [Modelo de integração com Google Sheets](https://www.hashtagtreinamentos.com/integracao-do-python-com-google-sheets-python?gad=1&gclid=Cj0KCQjwx5qoBhDyARIsAPbMagCQZoQPHPCya4zHI01EV-6e7SeIvoAlX6HgbEB-2Hkj-1tJCXsVyPEaAjtjEALw_wcB)
- [Sistema web do Governo do Estado do Pará](https://www.sistemas.pa.gov.br/governodigital/public/main/index.xhtml)
