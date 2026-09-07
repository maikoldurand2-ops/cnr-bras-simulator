# 🤝 Guia de Contribuição

Obrigado por se interessar em contribuir para o **CNR Brás - Simulador Territorial**! 

Este documento fornece diretrizes e instruções para ajudar você a contribuir de forma efetiva.

## 📋 Código de Conduta

Este projeto adota um código de conduta para garantir um ambiente acolhedor para todos. Ao participar, você concorda em:

- Ser respeitoso com todos os colaboradores
- Aceitar críticas construtivas
- Foco no que é melhor para a comunidade
- Mostrar empatia com outros membros

## 🚀 Como Começar

### Requisitos
- Git instalado
- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Editor de texto (VS Code recomendado)
- Conhecimento básico de HTML5, CSS3 e JavaScript ES6+

### Setup do Ambiente

1. **Fork o repositório** para sua conta GitHub
2. **Clone seu fork**:
```bash
git clone https://github.com/SEU-USUARIO/cnr-bras-simulator.git
cd cnr-bras-simulator
```

3. **Adicione o repositório original como upstream** (para manter sincronizado):
```bash
git remote add upstream https://github.com/maikoldurand2-ops/cnr-bras-simulator.git
```

4. **Crie uma branch** para sua feature:
```bash
git checkout -b feature/sua-feature
```

5. **Abra `index.html` em seu navegador** para testar

## 🐛 Reportando Bugs

Se encontrou um bug, abra uma [Issue](https://github.com/maikoldurand2-ops/cnr-bras-simulator/issues):

**Template sugerido:**
```markdown
## Descrição do Bug
[Descrição clara do problema]

## Passos para Reproduzir
1. Clique em...
2. Selecione...
3. Observe o comportamento

## Comportamento Esperado
[O que deveria acontecer]

## Comportamento Atual
[O que realmente acontece]

## Ambiente
- Navegador: Chrome 120
- SO: Windows 11
- Dispositivo: Desktop / Mobile
- Versão do jogo: [versão ou data do clone]
```

## 💡 Sugerindo Melhorias

Tem uma ideia? Abra uma [Discussion](https://github.com/maikoldurand2-ops/cnr-bras-simulator/discussions) ou Issue com label `enhancement`:

**Template sugerido:**
```markdown
## Descrição da Melhoria
[Explicar a ideia clara e concisamente]

## Problema que Resolve
[Qual necessidade ou problema isso atende]

## Benefícios
- Benefício 1
- Benefício 2
- Benefício 3

## Exemplos ou Mockups
[Se aplicável, adicione imagens ou exemplos]
```

## 📝 Submetendo Pull Requests

### Antes de Começar
1. Verifique se já existe Issue ou PR relacionada
2. Abra uma Issue descrevendo sua proposta
3. Aguarde feedback dos mantenedores
4. Inicie o trabalho apenas após aprovação

### Processo

1. **Mantenha sua branch atualizada**:
```bash
git fetch upstream
git rebase upstream/main
```

2. **Faça commits significativos**:
```bash
git commit -m "feat: adicionar novo tipo de personagem"
git commit -m "docs: atualizar guia de treinamento"
git commit -m "fix: corrigir bug no salvamento"
```

3. **Push para seu fork**:
```bash
git push origin feature/sua-feature
```

4. **Abra um Pull Request** no repositório original com:
   - **Título claro**: `[TIPO] Descrição breve`
   - **Descrição detalhada**: O que muda e por quê
   - **Link para Issue**: `Closes #123`
   - **Screenshots/GIFs**: Se aplicável
   - **Checklist de verificação**

### Template de PR

```markdown
## Descrição
[Explicar as mudanças e o motivo]

## Tipo de Mudança
- [ ] Bug fix (mudança que corrige um problema)
- [ ] Nova feature (adição de funcionalidade)
- [ ] Breaking change (mudança que quebra compatibilidade)
- [ ] Documentação

## Checklist
- [ ] Meu código segue o estilo do projeto
- [ ] Realizei auto-review do meu código
- [ ] Adicionei comentários em partes complexas
- [ ] Atualizei documentação se necessário
- [ ] Testei em navegadores modernos
- [ ] Testei em mobile (se aplicável)
- [ ] Nenhum aviso ou erro novo foi gerado

## Screenshots (se aplicável)
[Adicione imagens das mudanças]

## Closes
Closes #[ISSUE_NUMBER]
```

## 🎨 Padrões de Código

### JavaScript

✅ **Recomendado:**
```javascript
// Usar const por padrão, let para variáveis que mudam
const player = { x: 0, y: 0 };
let score = 0;

// Usar arrow functions
const calculateDistance = (x1, y1, x2, y2) => 
  Math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2);

// Usar template literals
const message = `Olá, ${playerName}!`;

// Usar desestruturação
const { x, y } = position;

// Adicionar comentários em lógica complexa
// Sistema de redução de danos com ponderação
const calculateHarmReductionScore = (approaches) => {
  return approaches.reduce((sum, approach) => {
    return sum + (approach.empathy * 0.4 + approach.resources * 0.3);
  }, 0);
};
```

❌ **Evitar:**
```javascript
var player = { x: 0, y: 0 }; // Usar const/let
function calculateDistance() {} // Usar arrow functions
msg = `Olá, ${name}`; // Sem ;
```

### HTML/CSS

- Use semantic HTML5 tags
- Mantenha classes CSS com nomes descritivos (kebab-case)
- Comente seções principais do código
- Indentação de 2 espaços

### Comentários

```javascript
/**
 * Calcula o impacto de uma abordagem no vínculo com o paciente
 * @param {Object} character - Dados do personagem
 * @param {string} approach - Tipo de abordagem ('empathy', 'resources', 'referral')
 * @returns {number} Mudança no vínculo (-100 a +100)
 */
const calculateApproachImpact = (character, approach) => {
  // ... implementação
};
```

## 📁 Estrutura de Arquivos

```
cnr-bras-simulator/
├── index.html              # Game + HTML/CSS/JS unificado
├── assets/
│   ├── data/              # JSON com dados de jogo
│   ├── images/            # Sprites e gráficos (futura expansão)
│   └── sounds/            # Áudio (futura expansão)
├── docs/                  # Documentação
│   ├── GAME_DESIGN.md
│   ├── MECHANICS.md
│   └── TRAINING_GUIDE.md
└── .github/
    └── workflows/         # CI/CD (futura configuração)
```

## 🧪 Testando Suas Mudanças

### Teste Local
```bash
# Abra index.html no navegador
# Ou use um servidor local:
python3 -m http.server 8000
# Acesse: http://localhost:8000
```

### Checklist de Testes
- [ ] Funciona no Chrome
- [ ] Funciona no Firefox
- [ ] Funciona no Safari
- [ ] Funciona no Edge
- [ ] Responsivo em mobile
- [ ] Touch/mouse funcionam corretamente
- [ ] localStorage funciona (salva e carrega)
- [ ] Console sem erros
- [ ] Performance adequada (60 FPS)

## 📊 Tipos de Contribuição

### 🎮 Gameplay
- Novos personagens
- Novos cenários/locais
- Mecânicas de jogo
- Balanceamento

### 🎨 Design/UX
- Melhorias visuais
- Acessibilidade
- Interface
- Animações

### 📚 Documentação
- README
- Guias de contribuição
- Comentários no código
- Guias de treinamento

### 🐛 QA/Testing
- Reportar bugs
- Testar em diferentes ambientes
- Sugerir melhorias

### ⚙️ Infraestrutura
- CI/CD
- Build tools
- Deployment
- Performance

## 🏆 Reconhecimento

Todos os contribuidores serão reconhecidos em:
- Seção "Contributors" do README
- [CONTRIBUTORS.md](CONTRIBUTORS.md)
- GitHub Insights

## ❓ Dúvidas?

- Abra uma [Discussion](https://github.com/maikoldurand2-ops/cnr-bras-simulator/discussions)
- Comente em uma Issue existente
- Envie email para o mantenedor

## 📝 Licença

Ao contribuir para este projeto, você concorda que suas contribuições serão licenciadas sob a [MIT License](LICENSE).

---

**Obrigado por contribuir! Sua ajuda é fundamental para fazer este simulador melhor.** 🚀❤️
