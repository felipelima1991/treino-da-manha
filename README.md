# Treino da Manhã

Página de treino de calistenia (aquecimento, circuito de 5 exercícios, cronômetro, checklist do dia, PSE e evolução das medidas), feita para o celular.

A página publicada aqui é **genérica**: perfil, medidas, metas e histórico não ficam no GitHub. Eles ficam no Google Drive de quem usa, através de um Google Apps Script próprio, no mesmo modelo da Agenda FoodLab.

## Como funciona

- **GitHub Pages** serve a página (`index.html` e as fotos em `img/`).
- **Apps Script** (`Code.gs`, que fica só na sua conta Google) guarda tudo num arquivo `treino-manha-dados.json` no seu Drive e devolve o seu plano pessoal (perfil, medidas iniciais, metas e marcos).
- A página guarda uma cópia neste aparelho e envia ao Drive cerca de 1,5 s depois de cada mudança. Sem internet, as mudanças esperam e vão quando a conexão volta.
- Se dois aparelhos salvarem ao mesmo tempo, a página junta os registros dos dois. Na mesma data, vale o do aparelho que está enviando.
- **Salvar planilha no Drive** cria um CSV na pasta "Treino da Manhã - exportações". **Baixar CSV** baixa o mesmo arquivo no aparelho.

## Configurar o Apps Script (uma vez)

1. Acesse [script.google.com](https://script.google.com) e crie um projeto novo chamado "Treino da Manhã".
2. Apague o conteúdo de `Code.gs` e cole o seu `Code.gs` privado (não está neste repositório).
3. No menu de funções, escolha `gerarChave`, clique em **Executar** e autorize o acesso ao Drive. Copie a chave que aparece no **Registro de execução**.
4. Clique em **Implantar → Nova implantação → App da Web**:
   - Executar como: **Eu**
   - Quem pode acessar: **Qualquer pessoa**
5. Copie o link do app da web (termina em `/exec`).
6. Abra a página no GitHub Pages, toque em **Conectar ao Google Drive** e cole o link e a chave.

Quem não tem a chave não consegue ler nem gravar nada: o Apps Script recusa a chamada.

Ao mudar o `Code.gs` depois, use **Implantar → Gerenciar implantações → Editar → Nova versão** para manter o mesmo link.

## Fontes

Fotos: Pexels (uso gratuito). Vídeos de apoio: YouTube, com título e canal em cada botão.
