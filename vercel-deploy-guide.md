# Deploy no Vercel - Guia Completo

## Método 1: Via Interface Web (Recomendado)

### Passo 1: Preparar o Projeto
1. Certifique-se que seu projeto está funcionando localmente
2. Commit e push para GitHub (se ainda não fez)

### Passo 2: Criar Conta no Vercel
1. Acesse: https://vercel.com
2. Clique em "Sign Up"
3. Conecte com sua conta do GitHub

### Passo 3: Importar Projeto
1. No dashboard do Vercel, clique "Add New Project"
2. Selecione o repositório do seu projeto
3. Configure as opções:
   - **Framework Preset**: Vite
   - **Root Directory**: deixe em branco (.)
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
   - **Install Command**: `npm install`

### Passo 4: Deploy
1. Clique "Deploy"
2. Aguarde o processo (2-3 minutos)
3. Receba a URL do seu site (exemplo: `seu-projeto.vercel.app`)

## Método 2: Via CLI (Alternativo)

### Instalar Vercel CLI
```bash
npm i -g vercel
vercel login
vercel --prod
```

## Configurações Importantes

### Variáveis de Ambiente (se necessário)
No dashboard do Vercel:
1. Vá em Settings > Environment Variables
2. Adicione variáveis como:
   - `NODE_ENV=production`
   - Outras variáveis que sua app precisa

### Domínio Personalizado
1. Vá em Settings > Domains
2. Adicione seu domínio personalizado
3. Configure o DNS seguindo as instruções

## Vantagens do Vercel
- ✅ Deploy automático a cada push
- ✅ HTTPS grátis
- ✅ CDN global
- ✅ Suporte a Node.js
- ✅ Preview de branches
- ✅ Domínio personalizado grátis

## Limitações Gratuitas
- 100GB de largura de banda/mês
- 1000 deploys/mês
- Geralmente suficiente para projetos pequenos/médios

## Após o Deploy
- Teste todas as páginas do seu funil
- Verifique se as imagens carregam
- Teste no mobile
- Configure Google Analytics se necessário