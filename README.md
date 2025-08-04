# Política de Privacidade - EstudaAI

Este diretório contém a página da Política de Privacidade do EstudaAI, pronta para ser hospedada no Heroku.

## Estrutura dos Arquivos

- `index.html` - Página principal da política de privacidade
- `README.md` - Este arquivo com instruções

## Deploy no Heroku

### Opção 1: Deploy via Heroku CLI

1. Instale o Heroku CLI se ainda não tiver:

   ```bash
   # Windows
   winget install --id=Heroku.HerokuCLI
   ```

2. Faça login no Heroku:

   ```bash
   heroku login
   ```

3. Crie um novo app no Heroku:

   ```bash
   heroku create estudaai-privacy-policy
   ```

4. Configure o buildpack para sites estáticos:

   ```bash
   heroku buildpacks:set https://github.com/heroku/heroku-buildpack-static.git
   ```

5. Crie um arquivo `static.json` na raiz deste diretório:

   ```json
   {
     "root": ".",
     "clean_urls": true,
     "https_only": true
   }
   ```

6. Faça o deploy:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git push heroku main
   ```

### Opção 2: Deploy via GitHub

1. Crie um repositório no GitHub
2. Faça upload dos arquivos para o repositório
3. Conecte o repositório ao Heroku através do dashboard
4. Configure o buildpack estático
5. Faça o deploy

## Personalização

Antes do deploy, você pode personalizar:

1. **E-mail de contato**: Altere `privacy@estudaai.com` no arquivo `index.html`
2. **Endereço da empresa**: Substitua `[Endereço da empresa]` no arquivo `index.html`
3. **Cores e estilo**: Modifique o CSS no arquivo `index.html`
4. **Conteúdo**: Atualize o texto conforme necessário

## URL Final

Após o deploy, sua política de privacidade estará disponível em:
`https://estudaai-privacy-policy.herokuapp.com`

## Conformidade Legal

Esta política de privacidade está em conformidade com:

- LGPD (Lei Geral de Proteção de Dados)
- GDPR (Regulamento Geral de Proteção de Dados)
- Outras leis de privacidade aplicáveis

## Suporte

Para dúvidas sobre o deploy ou personalização, entre em contato através do e-mail configurado na política de privacidade.
