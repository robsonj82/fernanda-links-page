# 🔗 Página de Links - Estilo Linktree

Uma página de links moderna e responsiva, perfeita para centralizar todos os seus links importantes em um só lugar!

## ✨ Funcionalidades

- 📱 Design 100% responsivo
- 🎨 Gradiente moderno e personalizável
- ⚡ Animações suaves
- 🎯 Ícones para redes sociais
- 🚀 Fácil de personalizar
- 🔒 Segurança com `rel="noopener noreferrer"`
- 📊 Preparado para adicionar analytics

## 🎨 Como Personalizar

### 1. Informações do Perfil

Edite o arquivo `links/index.html` e localize a seção de perfil:

```html
<div class="profile-section">
    <img src="SUA_FOTO_AQUI" alt="Foto de Perfil" class="profile-image">
    <h1 class="profile-name">SEU NOME AQUI</h1>
    <p class="profile-bio">
        SUA BIO AQUI - Conte sobre você!
    </p>
</div>
```

**Dicas para foto:**
- Use uma URL de imagem hospedada (imgur, cloudinary, etc)
- Tamanho recomendado: 400x400px
- Formato: JPG ou PNG

### 2. Modificar os Links

Encontre a seção `links-container` e edite os links:

```html
<a href="SEU_LINK_AQUI" target="_blank" rel="noopener noreferrer" class="link-button instagram">
    <i class="fab fa-instagram"></i>
    <span>TEXTO DO BOTÃO</span>
</a>
```

**Classes de cores disponíveis:**
- `instagram` - Gradiente do Instagram
- `whatsapp` - Verde WhatsApp
- `youtube` - Vermelho YouTube
- `linkedin` - Azul LinkedIn
- `twitter` - Azul Twitter
- `tiktok` - Preto TikTok
- `email` - Vermelho Gmail
- `website` - Roxo/Azul

### 3. Adicionar Novos Links

Para adicionar um novo link, copie e cole este template:

```html
<a href="https://seulink.com" target="_blank" rel="noopener noreferrer" class="link-button">
    <i class="fas fa-star"></i>
    <span>Novo Link</span>
</a>
```

**Ícones disponíveis:** Consulte [Font Awesome](https://fontawesome.com/icons) para mais ícones.

### 4. Remover Links

Simplesmente delete o bloco `<a>...</a>` completo do link que não deseja.

### 5. Personalizar Cores

No `<style>`, modifique as variáveis CSS:

```css
:root {
    --bg-gradient-start: #667eea;  /* Cor inicial do gradiente */
    --bg-gradient-end: #764ba2;    /* Cor final do gradiente */
    --link-bg: #ffffff;            /* Cor de fundo dos links */
    --link-hover: #f0f0f0;         /* Cor ao passar o mouse */
}
```

**Sugestões de gradientes:**
- Roxo: `#667eea` → `#764ba2`
- Azul: `#00c6ff` → `#0072ff`
- Rosa: `#f857a6` → `#ff5858`
- Verde: `#56ab2f` → `#a8e063`
- Laranja: `#ff6a00` → `#ee0979`

### 6. Alterar Fonte

Para mudar a fonte, adicione no `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
```

E no CSS:

```css
body {
    font-family: 'Poppins', sans-serif;
}
```

## 📊 Adicionar Analytics (Opcional)

Para rastrear cliques, integre com Google Analytics:

1. Adicione seu código do GA no `<head>`
2. Os cliques já estão sendo logados no console
3. Modifique o JavaScript para enviar eventos:

```javascript
link.addEventListener('click', function(e) {
    const linkName = this.querySelector('span').textContent;
    // Google Analytics 4
    gtag('event', 'click', {
        'event_category': 'Link',
        'event_label': linkName
    });
});
```

## 🚀 Deploy

O projeto está configurado para deploy automático via GitHub Actions:

1. Configure os secrets no repositório:
   - `FTP_SERVER`
   - `FTP_USERNAME`
   - `FTP_PASSWORD`

2. Faça push para a branch `main`
3. O deploy será automático!

## 📱 Teste Local

Para testar localmente, simplesmente abra o arquivo `links/index.html` no navegador.

## 🎯 Estrutura do Projeto

```
fernanda-links-page/
├── .github/
│   └── workflows/
│       └── deploy.yml          # Workflow de deploy automático
├── links/
│   └── index.html              # Página principal
└── README.md                   # Este arquivo
```

## 💡 Dicas

1. **Imagens otimizadas:** Comprima suas imagens antes de usar
2. **Links curtos:** Use encurtadores como bit.ly para links longos
3. **Teste mobile:** Sempre teste em dispositivos móveis
4. **Atualize regularmente:** Mantenha seus links atualizados
5. **Backup:** Faça backup do arquivo antes de grandes mudanças

## 🆘 Precisa de Ajuda?

- Problemas com cores? Use [Adobe Color](https://color.adobe.com/)
- Precisa de ícones? Visite [Font Awesome](https://fontawesome.com/)
- Gradientes legais? Confira [UI Gradients](https://uigradients.com/)

## 📄 Licença

Livre para usar e modificar como quiser!

---

Feito com ❤️ usando HTML, CSS e JavaScript puro.
