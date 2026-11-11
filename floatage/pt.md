# Política de Privacidade do Floatage

Data de vigência: 6 de novembro de 2026
Última atualização: 6 de novembro de 2026

O Floatage (doravante "o Aplicativo") é um aplicativo de anotações que funciona apenas no seu dispositivo. Você registra uma ideia no momento em que ela surge e, mais tarde, acrescenta complementações, de modo que cada registro passa a formar uma linha do tempo própria. Esta política descreve quais informações o Aplicativo realmente trata e como elas são guardadas. Leia-a antes de começar a usar o Aplicativo.

## 1. Quais informações o Aplicativo armazena

Todo o conteúdo que você digita ou dita no Aplicativo é salvo no seu dispositivo, incluindo:

- o título e o texto de cada registro (o texto também é usado para gerar o resumo da lista);
- as complementações que você acrescenta a um registro, com a respectiva data e hora;
- a marca de status de cada registro e se ele está fixado;
- as datas de criação e de modificação dos registros e das complementações.

O Aplicativo também mantém localmente uma cópia de segurança dos dados anteriores, usada para recuperá-los se o arquivo de dados principal for corrompido (ver seção 2).

O Aplicativo não coleta modelo do dispositivo, versão do sistema operacional, identificadores do dispositivo (IDFV ou IDFA), dados de localização, contatos, fotos, câmera, dados de saúde ou informações de pagamento. A entrada de voz não cria arquivos de áudio nem mantém gravações: só o texto reconhecido é guardado, como conteúdo do registro, e também não registra seu comportamento de uso nem seus caminhos de navegação.

## 2. Onde suas informações ficam armazenadas

Os registros são mantidos como um arquivo JSON dentro do espaço de armazenamento privado do Aplicativo (Application Support/Flit), ao lado de uma cópia de segurança `.bak`. Ao salvar, o Aplicativo grava primeiro um arquivo temporário e depois substitui o arquivo principal de forma atômica, para reduzir o risco de corrupção se a gravação for interrompida; se não conseguir ler o arquivo principal, tenta restaurá-lo a partir da cópia de segurança.

O Aplicativo não possui servidor: não envia, não transmite nem sincroniza esse conteúdo com qualquer serviço em nuvem ou terceiro. Não temos acesso, não conseguimos ler e não podemos restaurar seus registros.

## 3. Acesso à rede, exportação e compartilhamento

O Aplicativo não faz nenhuma solicitação de rede e não usa servidor. Não contém código de rede, e o aplicativo compilado também não se vincula aos frameworks de rede da Apple, portanto seus registros nunca são enviados, transmitidos ou sincronizados para nenhum lugar.

Todos os recursos podem ser usados sem conexão de rede, inclusive a entrada de voz: a fala é reconhecida no seu dispositivo e o texto reconhecido é gravado apenas no arquivo de dados local. A disponibilidade da entrada de voz depende de o sistema ter recursos de ditado para o seu idioma e de o ditado do sistema estar ativado; se qualquer um dos dois faltar, a entrada de voz é desativada e o Aplicativo mostra um aviso de que o reconhecimento de voz no dispositivo não está disponível no momento e sugere verificar as configurações de ditado do sistema ou usar o teclado. Você pode continuar digitando, e o Aplicativo nunca muda para um método de reconhecimento que precise de conexão de rede.

A versão atual não oferece recursos de exportação ou compartilhamento e não entrega conteúdo a outros aplicativos pela folha de compartilhamento do iOS. Se uma versão futura os adicionar, explicaremos antes do uso e atualizaremos esta política.

Se um backup do dispositivo iOS (backup do iCloud ou do computador) inclui os arquivos de registro no sandbox do Aplicativo depende das configurações de backup do seu sistema. Esse backup é feito por um recurso do sistema da Apple e não tem relação com o Aplicativo.

## 4. Permissões do sistema e acesso ao dispositivo

A entrada de voz é o único recurso que exige permissão. Na primeira vez que você tocar no botão de entrada de voz, o iOS perguntará se o Aplicativo pode usar o microfone; dependendo da API do sistema usada pelo Aplicativo, o iOS também pode exibir uma solicitação de autorização para o reconhecimento de voz. O Aplicativo não solicita permissões de notificações, biblioteca de fotos, câmera, localização, contatos ou dados de saúde, nem acessa esses itens.

### Microfone e entrada de voz

- Para que serve: o Aplicativo converte o que você fala em texto de um registro, que você pode editar antes de salvar. O texto reconhecido é gravado apenas no arquivo de dados local do Aplicativo (cards.json); nada além disso é criado.
- Quando é solicitada: apenas na primeira vez que você usa a entrada de voz. O Aplicativo não abre o microfone ao iniciar nem em segundo plano, e a gravação termina assim que você conclui o ditado, sai do editor ou fecha o Aplicativo.
- O áudio não é guardado nem enviado: o Aplicativo não cria arquivo de áudio nem mantém gravações. A entrada de voz usa o reconhecimento de voz do próprio dispositivo, portanto o áudio é processado apenas no seu dispositivo: não é enviado aos servidores da Apple nem a nós, e o texto reconhecido fica no arquivo de dados local do seu dispositivo. Para isso é preciso haver recursos de ditado para o seu idioma no sistema e o ditado do sistema estar ativado; caso contrário, a entrada de voz é desativada e o Aplicativo mostra um aviso de que o reconhecimento de voz no dispositivo não está disponível no momento e sugere verificar as configurações de ditado do sistema ou usar o teclado. Nunca recorre a um método de reconhecimento que precise de conexão de rede.
- Se você não conceder a permissão: todos os outros recursos continuam disponíveis, e você pode continuar adicionando e editando registros pelo teclado. Você pode conceder a permissão depois nos Ajustes do iOS ou revogá-la a qualquer momento; nesse caso a entrada de voz deixa de funcionar.

Caso uma versão futura inclua algum recurso que exija outra autorização, exibiremos a solicitação padrão do iOS antes do primeiro uso, explicaremos sua finalidade e atualizaremos esta política nesta página. Você pode revogar a qualquer momento as permissões concedidas nos Ajustes do iOS; nesse caso, o recurso correspondente poderá ficar indisponível.

## 5. Retenção e exclusão

- Os registros permanecem no seu dispositivo até que você os exclua.
- Você pode excluir um registro inteiro dentro do Aplicativo, bem como excluir separadamente cada complementação de um registro.
- Desinstalar o Aplicativo no iOS também apaga o arquivo de dados principal e o arquivo de backup do espaço de armazenamento do Aplicativo.
- A exclusão não pode ser desfeita. Como os dados existem apenas no seu dispositivo e o Aplicativo não oferece função de exportação, não conseguimos restaurá-los para você; exclua com cuidado.

## 6. SDKs de terceiros, análise e publicidade

O Aplicativo não inclui nenhum SDK de terceiros — nem de análise, nem de publicidade, nem de atribuição, nem de relatório de falhas. Ele não exibe anúncios, não rastreia você entre aplicativos ou sites, não usa IDFA e não solicita autorização de App Tracking Transparency. O envio de diagnósticos e registros de falhas do sistema à Apple depende da opção que você escolher em Ajustes do iOS > Privacidade e Segurança > Análises e Melhorias, e não tem relação com o Aplicativo.

## 7. Privacidade de crianças

O Aplicativo não é destinado a crianças e não coleta informações pessoais de ninguém. Como todos os registros ficam apenas no armazenamento local do dispositivo, nunca obtemos, guardamos ou compartilhamos nada do que uma criança escreva. Se você é pai, mãe ou responsável legal e acredita haver algum problema, entre em contato conosco pelos dados abaixo.

## 8. Alterações nesta política

Sempre que esta política for alterada, atualizaremos a data de "Última atualização" no início desta página. Se a alteração afetar a forma como suas informações são tratadas, indicaremos isso no Aplicativo ou nas notas de versão publicadas na App Store. Continuar usando o Aplicativo após a entrada em vigor de uma alteração significa que você aceita a política atualizada.

## 9. Fale conosco

Se você tiver dúvidas sobre esta política ou quiser exercer qualquer direito relacionado aos seus dados, entre em contato:

- E-mail de contato: yufei.cjn@outlook.com
