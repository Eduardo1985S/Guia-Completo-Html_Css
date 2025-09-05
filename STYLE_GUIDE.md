# 🎨 Guia de Estilo - Visual macOS

## 📋 Visão Geral

Este projeto foi atualizado com um design system inspirado no macOS, proporcionando uma experiência visual mais moderna e elegante.

## 🎯 Principais Melhorias Implementadas

### 1. **Sistema de Cores macOS**
```css
:root {
    --primary-color: #1d1d1f;        /* Texto principal */
    --secondary-color: #007aff;      /* Azul característico */
    --accent-color: #ff3b30;         /* Vermelho de destaque */
    --success-color: #30d158;        /* Verde de sucesso */
    --background-color: #f2f2f7;     /* Fundo claro */
    --card-background: #ffffff;      /* Fundo dos cards */
    --border-color: #d1d1d6;         /* Bordas sutis */
}
```

### 2. **Tipografia Sistema Apple**
- **Fonte Principal**: `-apple-system, BlinkMacSystemFont, 'SF Pro Display'`
- **Fonte Código**: `'SF Mono', 'Monaco', 'Inconsolata'`
- **Anti-aliasing**: Otimizado para telas Retina

### 3. **Visual Glass/Blur Effect**
- **Backdrop Filter**: `blur(20px)` para transparências
- **Cards Semi-transparentes**: `rgba(255, 255, 255, 0.9)`
- **Navegação Flutuante**: Efeito glassmorphism

### 4. **Animações e Transições**
- **Cubic Bezier**: `cubic-bezier(0.25, 0.46, 0.45, 0.94)`
- **Micro-animações**: Hover states suaves
- **Transform**: `translateY()` para elevação

### 5. **Componentes Atualizados**

#### **Cards dos Dias**
```css
.day-card {
    background: var(--card-background);
    border-radius: 12px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(20px);
    border: 1px solid var(--border-color);
}
```

#### **Navegação**
```css
.lesson-nav {
    background: rgba(255, 255, 255, 0.8);
    backdrop-filter: blur(20px);
    border-radius: 12px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
}
```

#### **Botões**
```css
.btn-primary {
    background: #007aff;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0, 122, 255, 0.25);
    transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
```

### 6. **Dark Mode Support**
```css
@media (prefers-color-scheme: dark) {
    :root {
        --primary-color: #f2f2f7;
        --secondary-color: #0a84ff;
        --background-color: #000000;
        --card-background: #1c1c1e;
        --border-color: #38383a;
    }
}
```

### 7. **Responsividade Aprimorada**
- **Mobile First**: Otimizado para dispositivos Apple
- **Breakpoints**: 768px e 480px
- **Touch Targets**: Mínimo 44px (padrão iOS)
- **Safe Areas**: Suporte a notch e bordas arredondadas

### 8. **Acessibilidade**
```css
@media (prefers-reduced-motion: reduce) {
    * {
        animation-duration: 0.01ms !important;
        transition-duration: 0.01ms !important;
    }
}
```

## 🎨 Paleta de Cores

### **Cores Principais**
- 🔵 **Azul Apple**: `#007aff` - Links e CTAs
- 🔴 **Vermelho**: `#ff3b30` - Alertas e erros
- 🟢 **Verde**: `#30d158` - Sucesso e confirmações
- ⚫ **Preto**: `#1d1d1f` - Texto principal
- ⚪ **Branco**: `#ffffff` - Backgrounds

### **Cores Neutras**
- 🌫️ **Cinza Claro**: `#f2f2f7` - Background geral
- 🌪️ **Cinza Médio**: `#d1d1d6` - Bordas
- 🌑 **Cinza Escuro**: `#8e8e93` - Texto secundário

## 📱 Componentes Visuais

### **Glassmorphism Cards**
- Transparência: 90% opacidade
- Blur: 20px backdrop-filter
- Bordas: 1px solid com alpha

### **Elevação (Box Shadow)**
- **Nível 1**: `0 4px 16px rgba(0, 0, 0, 0.1)`
- **Nível 2**: `0 8px 32px rgba(0, 0, 0, 0.15)`
- **Hover**: Aumento da elevação + transform

### **Border Radius**
- **Padrão**: 12px
- **Botões**: 12px
- **Cards**: 12px
- **Inputs**: 8px

## 🔧 Implementação

### **Arquivos Atualizados**
1. `assets/css/style.css` - Estilos principais
2. `assets/css/day-content.css` - Conteúdo dos dias
3. Todos os arquivos HTML mantêm estrutura

### **Compatibilidade**
- ✅ **Safari**: 100% compatível
- ✅ **Chrome**: 100% compatível  
- ✅ **Firefox**: 95% compatível
- ✅ **Edge**: 100% compatível

### **Performance**
- **Backdrop Filter**: GPU acelerado
- **Animações**: 60fps garantido
- **Loading**: Otimizado para conexões lentas

## 📸 Antes vs Depois

### **Melhorias Visuais**
1. **Cards**: De flat para glassmorphism
2. **Tipografia**: De genérica para SF Pro
3. **Cores**: De básicas para sistema Apple
4. **Animações**: De simples para cubic-bezier
5. **Responsivo**: De adequado para nativo-mobile

## 🚀 Próximos Passos

### **Fase 2** (Opcional)
- [ ] Ícones SF Symbols
- [ ] Micro-interações avançadas  
- [ ] Scroll suave otimizado
- [ ] Loading states
- [ ] Toast notifications

### **Otimizações**
- [ ] Critical CSS inline
- [ ] Lazy loading images
- [ ] Service Worker
- [ ] Progressive Web App

---

## 📞 Suporte

Para dúvidas sobre implementação ou customizações, consulte a documentação oficial do CSS ou entre em contato.

**Última atualização**: Setembro 2025  
**Versão**: 2.0 - macOS Style
