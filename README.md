# Bioo Finanças
Aplicativo independente em React + Vite, em português, com valores em BRL e armazenamento local. Sem dados pessoais pré-carregados.

## Rodar no Windows (PowerShell)
```powershell
npm.cmd install
npm.cmd run dev
```
Abra o endereço exibido pelo Vite (normalmente http://localhost:5173).

## Publicar no Netlify
1. Envie o conteúdo desta pasta para um repositório GitHub (não envie node_modules).
2. No Netlify, importe o repositório como novo projeto.
3. Build command: `npm run build`; publish directory: `dist`. O netlify.toml já contém essas configurações.
4. Alternativamente, execute `npm.cmd run build` e envie a pasta dist pela opção de deploy manual.

## Testes
`npm.cmd test` valida centavos, virada de ano, parcelas e backup. `npm.cmd run build` verifica a compilação.

## Dados e limitações
Os lançamentos ficam no localStorage do navegador, separados por domínio e perfil. Não há login, criptografia própria, sincronização, conexão bancária ou notificações externas. Publicar o código no Netlify não publica os lançamentos armazenados no navegador. Não use em computador compartilhado. Exporte backup JSON regularmente e importe no novo endereço/dispositivo quando necessário. CSV exporta os lançamentos filtrados do mês. A repetição mensal usa o valor informado em cada mês; editar/excluir afeta somente a ocorrência escolhida. O saldo realizado representa o movimento do mês, não o saldo bancário acumulado. O orçamento é mensal e os vencimentos exibem o mês selecionado. A instalação e a compilação precisam ser executadas localmente, pois as dependências não estavam disponíveis no ambiente de criação.
