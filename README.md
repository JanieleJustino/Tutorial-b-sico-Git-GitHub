# ROADMAP GIT
 
 Olá! Me chamo Janiele Justino e fiz esse roadmap com intuito de facilitar o seu entendimento sobre o GIT. Nesse guia você verá os principais comandos, com auxílio de vários exemplos visuais. Usei o vs code com a linguagem DART mas os comandos GIT são os mesmos independente da linguagem. Sinta-se livre para sugerir ajustes. Bons estudos!
 
 <p align="left">
  <a href="https://www.linkedin.com/in/desenvolvedorajanielejustino/" alt="Linkedin">
  <img src="https://img.shields.io/badge/-Linkedin-0e76a8?style=for-the-badge&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/desenvolvedorajanielejustino/" height= "25xp" /></a>
</p> 


Partindo do pressuposto que você sabe criar projetos na IDE e tem o GIT instalado, Iremos configurar seu ambiente GIT.  
O GIT pode ser usado por vários usuários e por isso você precisa configurar seu ambiente com seu nome e e-mail para registros de commits!  
**Vou te falar sobre duas formas de configurar o GIT: configurar globalmente e configurar localmente.**  

Após instalar o GIT na sua máquina própria, você pode **configurar globalmente**, ou seja, informar que por default todos os seus repositórios terão a assinatura X. Essa configuração só precisa ser feita uma única vez, salvo se você desinstalar o git.

**Obs: Essa configuração não determina a conexão com repositório online.**

Para configurar seu ambiente **GIT global**, use os comandos:  

DIGITE: **git config --global user.name “SEU NOME”**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195098423-a2abd6a1-41ee-4071-93f2-deb0ddd2e8e5.png" width="600px" height= "45xp"/>
</div>  
<div align="center"> Não é esperado algum retorno. </div>  

DIGITE: **git config --global user.email “SEU EMAIL”**  
LEMBRE DE USAR O EMAIL CADASTRADO NO SEU GIT  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195099714-74717357-7249-40f3-b6b5-4074f2edfffb.png" width="600px" height= "45xp"/>
</div>  
<div align="center"> Não é esperado algum retorno. </div>  

**Obs: Para verificar se a configuração foi realizada com sucesso, use os mesmos comandos mas dessa vez sem passar informações de nome ou e-mail:**

DIGITE: **git config --global user.name**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195101531-f2eac6d5-51c1-4a40-ae72-16a77889df1d.png" width="500px" height= "100xp"/>
</div>

DIGITE: **git config --global user.email**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195102117-9b0cf4a9-d2b4-4911-8bfa-eef4708766f4.png" width="500px" height= "50xp"/>
</div> 

Veja abaixo um exemplo, onde inicializei o repositório, sem realizar uma configuração GIT local e por default meu commit ficou com minha assinatura global:
**Obs: Não se preocupe, os comandos utilizados ainda serão vistos nesse roadmap, esse print serve apenas para testificar o default do global.**

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195622915-947e731e-7d41-444d-8e1e-a29289c1d188.png" width="800px" height= "300xp"/>
</div>

<div align="center"> Nesse roadmap vou dar exemplos usando um projeto com arquivos criados na lib, conforme imagens abaixo:</div>

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/194966258-0705ef25-aaf0-458b-999e-ec4a380d1f27.PNG" width="200px" />
</div>
<div align="center">
 <img src="https://user-images.githubusercontent.com/110784724/194966081-19a677e7-4813-4466-a0a3-f4129438b7cc.PNG" width="350px" height= "200xp" />
  <img src="https://user-images.githubusercontent.com/110784724/194966394-0331170f-0641-4711-b83c-5604380b0f1c.PNG" width="350px" height= "200xp" />
</div>  

## Controle de versão

Para acompanhar as mudanças de um projeto, é necessário usar o controle de versão. O primeiro passo é verificar se você está dentro da pasta do projeto, no exemplo abaixo usei a linha de comando do terminal:


DIGITE: **ls**   
CLIQUE ENTER
 

O retorno do comando **ls** foi:  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/194969707-744b4de7-3434-42e5-b423-9aad2fb01df1.PNG" width="400px" height= "150xp"/>
</div>  

**Diretório: D:\Tutoriais** -> informa que estou na pasta Tutoriais  
**Length Name** ->informa a lista de pastas existentes dentro de Tutoriais  

Lembra que meu projeto se chama **basicogit** ? Então, para entrar na pasta correta, uso os seguintes comandos:  

DIGITE : **cd NOME DA PASTA**  
CLIQUE ENTER  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195092031-8d13bfb3-ad4a-4b4f-93c0-3c84545058ef.PNG" width="300px" height= "80xp"/>
</div>

Agora podemos ver o nome da pasta adicionado ao diretório. Mas também podemos digitar um novo ls  para checar se agora estamos na pasta correta:  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195093046-5015aa22-4002-43d7-99be-202566d0a936.PNG" width="500px" height= "300xp"/>
</div>  
<div align="center">Primeiro passo concluído!</div>

## Iniciar repositório

O primeiro comando GIT que usamos é para iniciar um repositório local(na máquina).  

DIGITE: **git init**  
CLIQUE ENTER  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195097101-54c415ee-d381-45a3-b95c-e9ce2c7ae76d.PNG" width="450px" height= "80xp"/>
</div>

O retorno do comando **git init** informa que foi iniciado um repositório e uma pasta chamada **.git** foi criada na pasta do projeto. Essa pasta fica oculta mas você pode torná-la visível. Nela, é onde podemos acompanhar as mudanças realizadas nos arquivos do projeto.

## Configurar ambiente GIT  
Ao iniciar um repositório, caso você precise usar uma assinatura diferente por exemplo o email da sua empresa, você deve configurar o GIT localmente. Isso irá alterar a assinatura do seu commit.  

DIGITE: **git config user.name “SEU NOME”**   
CLIQUE ENTER  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195611989-189e8554-cadd-4222-800a-da9a0736d78a.png" width="600px" height= "100xp"/>
</div>  
<div align="center"> Não é esperado algum retorno. </div>  

DIGITE: **git config user.email “SEU EMAIL”**  
LEMBRE DE USAR O EMAIL CADASTRADO NO SEU GIT  
CLIQUE ENTER  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195629713-63385476-6776-4261-87d9-c6f69d8f97ff.png" width="600px" height= "90xp"/>
</div>  
<div align="center"> Não é esperado algum retorno. </div>  

Para verificar se a configuração foi realizada com sucesso, use os mesmos comandos mas dessa vez sem passar informações de nome ou e-mail:

DIGITE: **git config user.name**  
CLIQUE ENTER  
DIGITE: **git config user.email**  
CLIQUE ENTER  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195612884-52c69f97-0e62-422f-957f-5b74dcc547a3.png" width="500px" height= "200xp"/>
</div>  

Você também pode verificar as configurações  (assinaturas) existentes, use os comandos:  

DIGITE: **git config --list**  
CLIQUE ENTER  

## Ambiente de preparo
O GIT possui diversos ambientes onde podemos salvar o estado de um arquivo, isso significa que você pode salvar cada alteração realizada no projeto, para poder voltar a algum estado específico sem ter que excluir as alterações e refazer o código até o ponto onde queria deixá-lo.
Isso é importante por exemplo quando quisermos testar outras formas de solucionar algo que já funciona mas queremos poder voltar atrás se der errado. 

Um dos ambientes de preparo é o standing e para adicionar arquivos nele podemos usar os seguintes comandos: 

**Obs: Lembre sempre de salvar localmente as alterações realizadas, pode usar o atalho ctrl+S no teclado, antes de enviar os arquivos para o standing.**

Adicionar um arquivo específico  
DIGITE: **git add NomeDoArquivo**  
CLIQUE ENTER

Para adicionar as mudanças de todos os arquivos, pode usar qualquer um deses tr~es comandos:  
DIGITE **git add *  _ou_  git add –all _ou_ git add -A**  
CLIQUE ENTER

Ao clicar ENTER não é esperado algum retorno:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195113512-aa29796f-cf38-4e74-b470-e155803e8563.png" width="400px" height= "50xp"/>
</div>

Mas você pode verificar o status das alterações realizadas com o seguinte comando:

DIGITE: **git status**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195115732-8370fdd2-4cc5-4271-94f5-541f21bed0ca.png" width="350px" height= "300xp"/>
</div>

O retorno mostra os arquivos que foram adicionados ao ambiente de preparo do standing e que estão prontos para serem confirmados para o commit. No meu caso todas essas pastas foram adicionadas porque todas elas foram alteradas(foram criadas!).

## Commit
Para realizar o commit (confirmação dos estados que serão salvos), usamos o seguinte comando:

DIGITE: **git commit -m “DIGITE UM TEXTO QUE DESCREVA O ESTADO DO ARQUIVO”**  
CLIQUE ENTER  
**Obs: A flag -m possibilita que deixemos um texto descritivo(boas práticas) mas não é opcional, uma mensagem vazia vai abortar o commit.**

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195117144-c200b462-c381-468f-9262-db8ca9279ad5.png" width="700px" height= "250xp"/>
</div>

**git status** para verificar se ainda existem alterações disponíveis para o standing:
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195117779-ea403c45-8629-46f0-8470-bec1d66b7943.png" width="300px" height= 80xp"/>
</div>
                                                                                                                         
O retorno fala apenas **On branch master** porque nesse projeto até o momento só tenho a branch master. Então ele informa que não existe nenhuma alteração no standing para ser confirmada(commit) e que a árvore de trabalho (local) está limpa!
                                                                                                                     
## Alterar nome da branch master
Aliás, que tal mudar o nome de “master” para “main”? Essa alteração é considerada como  boas práticas em algumas organizações. Use o seguinte comando:

DIGITE: **git branch -m main**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195118813-afa51422-75a4-4558-986f-bf1af9e77944.png" width="300px" height= "70xp"/>
</div>
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195119250-648f03ed-ee3e-4cef-85f2-84af9f74c0e7.png" width="300px" height= "80xp"/>
</div>  
<div align="center">O retorno agora informa “main”. Essa não é uma alteração que precisa de commit.</div>

## Verificar commits realizados 
Para verificar os commits realizados, use o seguinte comando:

DIGITE: **git log**  
CLIQUE ENTER

O retorno exibirá a lista de estados salvos. Cada estado possui informações de identificação:

**hash ->** chave de identificação composta por combinações de números e letras aleatórios  
**nome da branch ->** onde o estado está salvo  
**nome e e-mail do autor ->** responsável pela alteração  
**data e hora ->** registro do momento em que foi feito a confirmação(commit)  
**texto descritivo ->**  para saber do que aquele estado se trata  

No meu exemplo, tenho apenas uma branch e apenas um commit, veja:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195121667-ca044553-897c-4a50-b9d9-60d786867093.png" width="600px" height= "200xp"/>
</div>
                                                                                                                                              
## Gerenciar estados
Novamente, veja a importância de lembrar de salvar as alterações localmente antes de tentar enviar ao standing:
                                                                                                                                               
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195124768-73005a5d-725a-4ec0-b7e3-ad37a306f718.png" width="700px" height= "300xp"/>
</div>  
                                                                                                                                               
OBSERVE OS COMANDOS INDICADOS NAS LINHAS QUE COMEÇAM COM **PS**:
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195126298-11e832fa-2183-48b3-8b64-78d90247027f.png" width="700px" height= "400xp"/>
</div>  
                                                                                                                                               
Salvei a alteração no **arquivo_um.dart**  
**git status**  para verificar as alterações disponíveis para o standing  
**git add * .**  para salvar os estados no standing  
**git status** para ver os estados disponíveis para commit  
**git restore** –stage NOME DO ARQUIVO para retirar do standing  
**git status** para ver se saiu do standing  

E abaixo o print com o resultado do:  
**git restore NOME DO ARQUIVO** para desfazer as alterações no arquivo:
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195127729-7e794bd6-7968-4160-b86f-1eddf24114b8.png" width="700px" height= "400xp"/>
</div>                                                                                                                                            
<div align ="center"> Perceba que o print que eu tinha adicionado na classe foi retirado!</div>  

Obs:  o comando **git restore –stage NOME DO ARQUIVO** também pode ser substituído por **git reset HEAD NOME DO ARQUIVO** trazendo o mesmo resultado que é retirar do standing.                                                                                                                                               
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195129272-a13ce180-cd75-448e-8a97-3474088c485f.png" width="700px" height= "400xp"/>
</div>                                                                                                                                               

## Deletar arquivo
                                                                                                                                               
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195130728-6d58cf8c-51e9-45d6-9a1c-0c4048cfa193.png" width="600px" height= "400xp"/>
</div> 
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195131449-f6f5313b-4b4c-4a55-9d2f-7457e71821a8.png" width="500px" height= "200xp"/>
<img src="https://user-images.githubusercontent.com/110784724/195132537-89409f25-b8a2-42a8-88c3-f7d612047798.png" width="300px" height= "200xp"/>
</div>

Ao excluir um arquivo do seu diretório local, esse arquivo some da lista de arquivos, porém continua disponível para finalizar a exclusão ou cancelar a exclusão, pois em um repositório git, uma deleção também é um evento que precisa de commit. Por isso o GIT já sinaliza que existe uma alteração disponível para o standing. 

Também podemos checar isso, realizando o **git status**: 
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195148055-3035b78d-6409-431d-a9bb-8af0a16014c4.png" width="600px" height= "200xp"/>
</div>                                                                                            

**git add/rm** têm a mesma finalidade, levar a alteração ao standing. O **add** significa adicionar a remoção e o **rm** significa remover.
o **git restore** como já vimos antes permite restaurar o arquivo, veja:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195193031-46b0732e-b876-4147-87de-5a7b87e52532.png" width="700px" height= "300xp"/>
</div>

Mas vamos seguir com a deleção...
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195194412-592357e0-86d4-4fd2-9e0b-6c938033f703.png" width="800px" height= "400xp"/>
</div>  

Viu como o retorno é igual a quando colocamos **git add** para adicionar ao standing?  
Agora é só usar os comando já vistos:  
**git commit -m “texto descritivo”** para deletar de vez  
**git restore –stage NOME DO ARQUIVO** ou  **git reset HEAD NOME DO ARQUIVO** para tirar do standing  
**git restore NOME DO ARQUIVO** para desistir da deleção  

## Gerenciar logs(registros de commits) 

Vou criar um novo commit, você lembra como faz? No arquivo desejado, realize a alteração e salve-a localmente. Em seguida use os comandos já vistos:

**git status**  
**git add NOME DO ARQUIVO**  
**git commit -m “Texto descritivo”**  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195196459-52f47d21-f6b3-4b0b-968a-f1820c43139b.png" width="800px" height= "400xp"/>
</div>

Agora tenho dois commits:
<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195198300-82040370-0cad-4d91-bc09-f04ba9a09d83.png" width="700px" height= "300xp"/>
</div>

Os commits são identificados pelo texto descritivo e pelo hash.  
Você pode usar o hash para trazer o commit do log para o ambiente de trabalho.  

Vou usar o hash do primeiro commit, observe a mudança na tela:  
DIGITE: **git checkout HASH**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195199877-5439a608-2480-493b-b5b4-2c9173751b92.png" width="600px" height= "500xp"/>
</div>

Nesse modo você pode fazer alterações, commits, cancelar commits mas nada ficará salvo. Se você quiser realmente salvar alguma alteração, deverá criar um novo ramo a partir da branch main.

A partir do momento em que você entra em um estado, é como se fosse um mundo alternativo em que você pode fazer qualquer coisa que não vai alterar o estado da main. Por exemplo, se você realizar um **git log** verá que ele só mostra os próprios commits:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195202509-bd6ee14e-5199-4116-850e-a659a76b0fe4.png" width="600px" height= "500xp"/>
</div>

Veja esse exemplo em que eu fiz outros commits dentro desse “mundo paralelo”:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195203524-9e8b3893-1b8c-40af-8a23-a9da56745686.png" width="600px" height= "500xp"/>
</div>

E se você quiser sair desse estado e ir para a branch main? Simples, siga os seguintes passos:  

DIGITE:  **git branch**  
CLIQUE ENTER

O retorno será a lista de branchs, a que estiver marcada em verde é a branch que você está!

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195203964-75838544-00a2-42ea-a600-e51f40966712.png" width="300px" height= "100xp"/>
</div>

Para sair, faça a mudança para a branch principal, a main.  
DIGITE: **git checkout main**  
CLIQUE ENTER

O retorno será uma informação:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195204365-0b0af108-270d-4e5d-a1a2-ae2cd090118d.png" width="600px" height= "250xp"/>
</div>

Pronto, você já está na branch main e o retorno diz que você tem dois commits não associados a branch, que estão sendo deixados para trás mas se você quiser mantê-los, pode criar um novo ramo usando o comando **git branch NOME DA NOVA BRANCH 4fcff8a**  mas caso não queira, continue seu trabalho.

**Esse código é específico do meu exemplo e não um padrão de comando, e só irá aparecer um código para criar uma branch nesse tipo de ocasião.**

Verificando os logs da branch main:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195205080-771caccb-1db8-439c-b862-7e13e96e2afe.png" width="600px" height= "500xp"/>
</div>

## Controle de estados com ramos(novas branches)

A partir da branch principal podemos criar um novo ramo com o seguinte comando:  

DIGITE: **git branch NOME DO NOVO BRANCH**  
CLIQUE ENTER

Não é esperado algum retorno.

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195205847-05b166ed-0eed-4f9f-ae33-97b67b4b969d.png" width="450px" height= "100xp"/>
</div>

Verificar branches existentes:  
DIGITE: **git branch**   
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195206723-03d4ab9e-68a7-42fb-85fc-e15eeae5690e.png" width="450px" height= "100xp"/>
</div>

Mudar de branch:  
DIGITE: **git checkout NOME DA BRANCH**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195207195-f488989b-e734-415c-ab67-ee663acfd476.png" width="500px" height= "200xp"/>
</div>  

Criar uma branch a partir da atual e mudar para ela:  
DIGITE: **git checkout -b NOME DA BRANCH**  
CLIQUE ENTER  

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195636713-05940e63-102d-4f03-bbb9-cb79102ef6ae.png" width="400px" height= "100xp"/>
</div>  

Essa branch é como um clone da branch main, você só vai acrescentar informações a partir do que já existia, veja:

**Como a branch desenvolvimento foi criada:**

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195207637-87f28a5c-90b1-4ba5-b3c2-72f2aaa905eb.png" width="600px" height= "300xp"/>
</div>  

**Branch desenvolvimento alterada:**

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195209147-b445c1d0-6c17-41b8-9658-380d7e242f75.png" width="600px" height= "500xp"/>
</div>

Digamos que você gostou do resultado e quer implementar na branch main, faça um **MERGE!**

## Merge  

É basicamente a união das duas branches.
O merge só é possível a partir do main, então faça o checkout do branch como já te ensinei e em seguida use os comandos:

DIGITE: **git merge desenvolvimento**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195209758-e8ef1d9a-ae2d-4490-a824-9ff7b40dd481.png" width="600px" height= "500xp"/>
</div>

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195210116-e7a214a4-4c98-4208-8a91-76a61953505a.png" width="600px" height= "500xp"/>
</div>

## Alterar o nome de alguma branch existente

Você pode fazer isso a partir de qualquer branch:  

DIGITE: **git branch -m NomeAtual NomeNovo**  
CLIQUE ENTER

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195211097-c4da3c9a-ddba-43ca-bb0e-132d7530c783.png" width="600px" height= "500xp"/>
</div>

## Deletar branch

Quer deletar uma branch que não será mais usada após o merge?

DIGITE: **git branch -D NOME DA BRANCH**  
CLIQUE ENTER

Você deve fazer isso a partir da branch principal, pois após deletar qualquer branch você permanecerá na main, se você estiver dentro da branch que quer deletar o retorno será um erro, veja:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195211863-ed7dc33e-4d8c-42a7-887e-1b42da2f2d86.png" width="600px" height= "100xp"/>
</div>

Seguindo os passos corretos:

<div align="center">
<img src="https://user-images.githubusercontent.com/110784724/195212411-12a46a6b-a7e7-4e89-9291-5167610783b2.png" width="600px" height= "250xp"/>
</div>












