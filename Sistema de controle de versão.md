# Controle de versão

## O que é o controle de versão e porque eu preciso me preocupar?

Do termo em inglês Version Control System (VCS), o sistema de controle de versão ou sistema de versionamento é uma ferramenta poderosa e que pode ser usada em muitos lugares, não apenas na programação.

O controle de versão é um sistema que armazena as alterações para um arquivo ou um conjunto de arquivos através do tempo sendo possível recarregar versões especificas mais tarde.

Como programadores, nós estamos diariamente escrevendo novos códigos e alterando códigos antigos. Com o uso de um sistema de versionamento, somos capazes de ter um histórico completo das alterações feitas por cada pessoa que trabalhou dentro do projeto.

Esses sistemas armazenam os projetos dentro de repositórios, que na mais são que uma pasta contendo os arquivos do projeto e também os arquivos do sistema de controle de versão.

Dessa forma, é possível navegar através de uma linha do tempo, revendo quais arquivos foram alterados, comparando as versões de um determinado arquivo, criar linhas de tempo alternativas para manter o processo de desenvolvimento organizado e também retornar um arquivo ou o projeto todo para um determinado ponto da história.

Na prática, o uso de um VCS pode nos ajudar quando fazemos alguma alteração que quebra o projeto e precisamos reverter rapidamente para um estado anterior, sem maiores problemas.

Ao utilizar um sistema de controle de versão, podemos acabar com uma prática muito conhecida de controle de versão manual que acabamos fazendo localmente em nossas máquinas, que é através da cópia do arquivo com outro nome e se você for esperto vai adicionar uma data e hora ao nome.

Isso é uma técnica simples, porém, ineficiente em termos de segurança, pois seus arquivos ainda continuam apenas na sua máquina. Caso ocorra algo com o HD ou SSD da sua máquina, todos os seus arquivos poderão ser perdidos e dificilmente serão recuperados através de um processo caro e especializado de recuperação de dados.

## Sistemas de controle de versão cliente-servidor

Os sistemas de controle de versão cliente-servidor são um tipo de Centralized Version Control System (CVCS), os quais rodam dentro de um servidor dentro da empresa (on-premisse), ficando limitados a conexão local ou por acesso via VPN.

Esse tipo de sistema é centralizado e geralmente é um ponto de falha, pois, se não for gerenciado corretamente, com backups, atualizações e tudo que envolve a manutenção de um servidor on-premisse, corre-se o risco de perder todas as informações versionadas.

Por sua característica centralizada, toda vez que for necessário gravar um novo ponto na história, o que chamamos de commit, é necessário estar conectado com o servidor.

imagem: <https://git-scm.com/book/en/v2/images/centralized.png>

Como exemplos de sistemas de controle de versão cliente-servidor podemos citar dois: o SVN e o CVS.

O SVN ou Apache Subversion é um sistema de código aberto desenvolvido desde o ano 2000, inicialmente pela CollabNet, Inc. e atualmente é mantido pela Apache Foundation.
Seu funcionamento é baseado no bloqueio do arquivo ou dos arquivos pelo usuário. Ao efetuar o commit, o arquivo é liberado para ser editado ou atualizado.
Um dos maiores problemas com SVN é o do merge de arquivos quando mais de um usuário está trabalhando ao mesmo tempo, o que força o merge, que é o processo de mesclar as alterações, de forma manual entre a versão do servidor e a versão do usuário que está subindo no novo commit.

Para mais informações, acesse [https://subversion.apache.org/](https://subversion.apache.org/)

O CVS ou Concurrent Versioning System é um software livre, licenciado através da GNU GPL, criado originalmente por Dick Grune  para ser utilizado como forma de ajudar dois de seus alunos na manutenção do projeto ACK (Amesterdam Compiler Kit) em 1986. Como software livre teve seu desenvolvimento entre 1990 e 2008, sendo compatível com sistemas Unix-like e Windows. Dessa forma, não é recomendável seu uso principalmente por ser um software que não está mais recebendo atualizações.

## Sistemas de controle de versão distribuídos

Diferentemente dos sistemas cliente-servidor, os sistemas de controle de versão distribuídos ou Distributed Version Control Systems (DVCS) em inglês, não dependem diretamente de um servidor para poderem funcionar.

Nesse tipo de sistema, podemos ter vários servidores que armazenam uma cópia do repositório em um determinado ponto da história. Dessa forma, caso algo aconteça com nosso servidor, é possível reconstruí-lo enviando o repositório em nossa máquina para o novo servidor.

Dessa forma, os commits de novas versões são feitos localmente e periodicamente sincronizados com o servidor, bem como os commits de outros usuários podem ser sincronizados com o repositório local.

Também é possível trabalhar com linhas de tempo, chamadas de branches ou galhos em português. Um branch é uma ramificação usada para manter uma linha de tempo paralela ao branch principal, que é conhecido por master ou main.

<https://git-scm.com/book/en/v2/images/distributed.png>

Os dois principais sistemas de controle de versão distribuídos usados atualmente são o Mercurial e o Git.

### Mercurial

O Mercurial ou Mercurial SCM é uma ferramenta de controle e gerenciamento de bases de código, suportada por sistemas Unix-like como FreeBSD, macOS e Linux, bem como pelo Microsoft Windows.

Os principais objetivos do Mercurial incluem alta performance e escalabilidade, decentralização, desenvolvimento colaborativo totalmente distribuído, manipulação robusta tanto de arquivos de texto quanto de arquivos binários, além de capacidades de uso de branch e merge de forma avançada.

Ele é amplamente usado pelo Facebook, Google e Mozilla. Dentro do Facebook, é usado através de uma versão escrita em Rust chamada Mononoke feita para suportar repositórios multi-projeto.

Já no Google, ele é usado com o front-end para o produto monorepo baseado em cloud chamado Piper.

### Git