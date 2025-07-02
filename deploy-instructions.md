# Instruções de Deploy - HostGator

## Pré-requisitos
1. Acesso ao cPanel da HostGator
2. Projeto compilado (build)

## Passos para Deploy:

### 1. Compilar o projeto
```bash
npm run build
```

### 2. Acessar HostGator
- Entre no cPanel da HostGator
- Clique em "Gerenciador de Arquivos"
- Navegue até a pasta `public_html`

### 3. Upload dos arquivos
- Faça upload de TODOS os arquivos da pasta `dist` para `public_html`
- Faça upload do arquivo `.htaccess` para `public_html`

### 4. Configurar domínio
Se estiver usando um subdomínio ou domínio personalizado:
- Configure no cPanel > Subdomínios ou Domínios Addon

## Arquivos importantes:
- `dist/index.html` - Página principal
- `dist/assets/` - CSS, JS e imagens
- `.htaccess` - Configurações do servidor

## Observações:
- Este deploy é apenas para o frontend (landing page)
- Não inclui funcionalidades de backend
- Perfeito para páginas de vendas e marketing

## Teste:
Após o upload, acesse seu domínio para verificar se tudo está funcionando.