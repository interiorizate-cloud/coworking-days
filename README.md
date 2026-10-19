# Coworking Days · INterioriza-te

Versão experimental independente para GitHub Pages.

Aplicação: https://interiorizate-cloud.github.io/coworking-days/

- Entrada: https://interiorizate-cloud.github.io/coworking-days/?acao=entrada
- Saída e avaliação: https://interiorizate-cloud.github.io/coworking-days/?acao=saida

## Funcionamento

A interface estática comunica diretamente com o serviço Google Apps Script existente através de pedidos POST CORS, sem cookies Google. Mantém a mesma base de dados, os utilizadores e as sessões. A lista de espaços reflete os espaços ativos configurados na base de dados.

Não contém credenciais, dados pessoais da base de dados nem código administrativo. O endereço público do serviço é configuração do cliente, não uma credencial.

GitHub Pages publica a raiz da branch main, com HTTPS obrigatório. A aplicação anterior e os respetivos códigos QR continuam disponíveis durante os testes.

## Verificação

Executar `node test-client.cjs` para validar seleção obrigatória do espaço, seis respostas obrigatórias por estrelas e múltiplas sessões no mesmo dia. Ligação CORS e resposta a credencial inválida verificadas no navegador. O teste completo com utilizador real deve ser feito antes de substituir os códigos QR existentes.
