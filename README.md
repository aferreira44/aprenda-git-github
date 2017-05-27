# Udacity - Como Usar o Git e o GitHub

## Reflexões

### Lição 1

**Como a visualização de um diff entre duas versões de um arquivo ajuda você a ver o bug que foi introduzido?**

Um diff é capaz de mostrar as alterações realizadas em um arquivo, ficando muito fácil de identificar onde foram introduzidos os bugs.

**Como ter fácil acesso a todo o histórico de um arquivo pode torná-lo um programador mais eficiente no longo prazo?**

No caso de um bug, posso voltar para uma versão estável, além de descobrir quais alterações causaram o bug.

**Na sua opinião, quais são os prós e contras de escolher manualmente quando criar um commit, como ocorre no Git, v. o salvamento automático de versões, como no Google Docs?**

Prós: definir e separar logicamente o que será incluído em cada commit, facilitando o entedimento do histórico
Contras: Se não fizer uma separação lógica clara das alterações em cada commit, o histórico ficará difícil de entender e de resolver possíveis bugs.

**Por que você acha que alguns sistemas de controle de versão, como o Git, permitem salvar vários arquivos em um commit, enquanto outros, como o Google Docs, tratam cada arquivo separadamente?**

Pois os arquivos de código-fonte no Git são dependentes e relacionados entre si. No Google Docs cada arquivo é independente.

**Como usar os comandos git log e git diff para visualizar o histórico dos arquivos?**

git log -> mostra o histórico de commits realizados
git log --stat -> mostra o histórico de commits realizados com estatísticas
git diff b0678b161fcf74467ed3a63110557e3d6229cfa6 f19cb1b80fe27e938e4d72770ca0a42f25e99ecc -> mostra aa alterações nos arquivos entre dois commits

**De que modo o controle de versão pode dar a você mais segurança para fazer alterações que podem danificar algo?**

Pois a qualquer momento posso utilizar "git checkout" para voltar as alterações de um determinado commit e utilizar "git diff" para descobrir o que causou o bug

**Agora que você já configurou a sua área de trabalho, você quer usar o Git para quê?**

Para ter um controle do código produzido, resolver bugs e facilitar o dia a dia do desenvolvimento.

---

### Lição 2

**O que acontece ao iniciar um repositório? Por que você precisa fazer isso?**

Ao rodar o comando "git init", o git cria a pasta oculta /.git onde salva os metadados do repositório e exibe a mensagem que um repositório vazio foi criado.

**Em que se difere a área de preparação do diretório de trabalho e do repositório? Qual valor você acha que ela oferece?**

É uma área onde é possível preparar somente as alterações para enviar como commit ao repositório.
Com isso, é possível enviar as alterações de acordo com uma lógica, sem ter que adicionar todas as alterações de uma só vez ao repositório.

**Como você pode usar a área de preparação para garantir que tenha um commit por alteração lógica?**

Separando somente os arquivos e as alterações de acordo com a alteração lógica na staging area antes de dar um commit no repositório.

**Quais são algumas das situações em que branches seriam úteis para manter seu histórico organizado? Como branches ajudariam?**

Ao adicionar uma nova funcionalidade, fazer traduções ou corrigir bugs, um branch pode ser criado para separar essas alterações do código principal

**Como os diagramas ajudam a visualizar a estrutura de branches?**

Eles ajudam a entender o histórico de commits e em quais branches eles estão localizados

**Qual é o resultado da mesclagem de dois branches? Por que o representamos no diagrama dessa forma?**

Os commits e alterações dos arquivos de um branch são adicionados ao outro

**Quais são os prós e contras da mesclagem automática do Git v. sempre fazer mesclagens manualmente?**

O Git tenta resolver os merges automaticamente sempre que não há confiltos nas mesmas linhas do código entre dois branchs.
Se houver código diferente em linhas iguais, os conflitos devem ser resolvidos manualmente

Isso agiliza o trbalho e fica fácil de resolver problemas de trabalho em equipe

---

### Lição 3

**Quando gostaria de usar um repositório remoto em vez de manter o trabalho local?**

Quando eu quiser manter um backup online do meu repositório local ou quando tiver a colaboração de outras pessoas no projeto
