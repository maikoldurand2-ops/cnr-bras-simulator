# 🏥 CNR Brás - Simulador Territorial

Simulador imersivo de abordagem territorial do **Consultório na Rua (CNR)** do Brás, São Paulo. Ferramenta educacional para treinamento de equipes de saúde em **Redução de Danos** e cuidado humanizado.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/Play-GitHub%20Pages-blue)](https://maikoldurand2-ops.github.io/cnr-bras-simulator/)
[![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

## 🎮 Como Jogar

### Online (Recomendado)
Acesse diretamente via GitHub Pages:
```
https://maikoldurand2-ops.github.io/cnr-bras-simulator/
```

### Localmente
1. Clone o repositório:
```bash
git clone https://github.com/maikoldurand2-ops/cnr-bras-simulator.git
cd cnr-bras-simulator
```

2. Abra `index.html` em seu navegador:
   - **Windows/Mac**: Clique duplo no arquivo
   - **Linux**: `python3 -m http.server 8000` (depois acesse `localhost:8000`)

## 🛠️ Tecnologias

| Tecnologia | Uso |
|-----------|-----|
| **HTML5 Canvas** | Renderização pixelada e gráficos |
| **JavaScript ES6+** | Lógica do jogo (sem dependências) |
| **Web Audio API** | Sons e feedback auditivo |
| **localStorage** | Sistema de salvamento de progresso |
| **CSS3** | Interface responsiva |

## 📱 Compatibilidade

✅ **Desktop**: Chrome, Firefox, Safari, Edge (versões recentes)  
✅ **Mobile**: Android e iOS (otimizado para touch)  
✅ **PWA**: Add to home screen (funciona offline)

## 🎯 Mecânicas de Jogo

### Mapa Interativo
Explore o bairro do Brás em estilo pixel art. Navegue para diferentes pontos de interesse onde pode atender a população em situação de rua.

### Abordagem Territorial
Escolha sua estratégia de aproximação baseada em **Redução de Danos**:
- 🤝 Abordagem empática e humanizada
- 💊 Oferta de insumos e recursos
- 🏥 Referenciamento para serviços de saúde
- 📋 Escuta ativa e vínculo

### Sistema de Pontuação
Acumule pontos baseado em:
- **Vínculo**: Qualidade da abordagem
- **Harm Reduction**: Aplicação de princípios de redução de danos
- **Encaminhamentos**: Sucessos em referenciamento
- **Continuidade**: Acompanhamento de casos

### Personagens
Cada encontro apresenta um personagem com histórico, necessidades e desafios únicos. Suas decisões impactam os resultados.

### Salvamento Automático
Seu progresso é salvo automaticamente via localStorage. Você pode pausar e retomar a qualquer momento.

## 🏗️ Estrutura do Projeto

```
cnr-bras-simulator/
├── index.html              # Arquivo principal do simulador
├── README.md               # Este arquivo
├── CONTRIBUTING.md         # Guia de contribuição
├── LICENSE                 # Licença MIT
├── .gitignore              # Arquivos ignorados pelo Git
│
├── assets/
│   ├── images/
│   │   ├── sprites.png     # Spritesheet de personagens e tiles
│   │   └── map.png         # Mapa do Brás
│   │
│   ├── sounds/
│   │   ├── click.mp3       # Som de clique
│   │   ├── success.mp3     # Som de sucesso
│   │   └── ambient.mp3     # Música de fundo
│   │
│   └── data/
│       ├── characters.json  # Dados dos personagens
│       ├── locations.json   # Pontos de interesse
│       └── scenarios.json   # Cenários de abordagem
│
├── docs/
│   ├── GAME_DESIGN.md      # Documento de design
│   ├── MECHANICS.md        # Explicação das mecânicas
│   └── TRAINING_GUIDE.md   # Guia para educadores
│
└── .github/
    └── workflows/
        └── deploy.yml      # CI/CD para GitHub Pages
```

## 🚀 Para Plataformas de IA

Este é um **HTML5 single-file game** facilmente importável em plataformas de desenvolvimento com IA:

- **[Lovable.dev](https://lovable.dev)** - Upload `index.html` ou URL do repo
- **[v0.dev](https://v0.dev)** - Forneça a URL do repositório
- **[Replit](https://replit.com)** - Clone direto do GitHub
- **[Glitch](https://glitch.com)** - Importe repositório GitHub
- **[GitHub Copilot Workspace](https://github.com/features/copilot)** - Abra direto no Workspace

## 📊 Dados do Simulador

### Personagens
Cada personagem possui:
- Nome e background
- Necessidades de saúde
- Barreira inicial
- Resposta a diferentes abordagens
- Histórico de encontros

### Locais (Brás)
- Praça da Sé
- Terminal Rodoviário
- Ponte do Brás
- Rua 25 de Março
- Albergues
- Unidades de saúde
- Pontos de tráfico (riscos)

### Cenários de Abordagem
Escolha entre:
1. **Estratégia Empática** - Foco em vínculo
2. **Acesso a Recursos** - Oferecimento de insumos
3. **Mobilização de Rede** - Referenciamento
4. **Escuta Ativa** - Diagnóstico de necessidades

## 🎓 Para Educadores

Use este simulador em treinamentos de equipes CNR:

1. **Briefing inicial** - Contexto do Consultório na Rua
2. **Gameplay guiado** - Facilitador passa por cenários
3. **Discussão reflexiva** - Debate sobre decisões tomadas
4. **Débriefing** - Aplicação em realidade territorial

→ Veja [TRAINING_GUIDE.md](docs/TRAINING_GUIDE.md) para roteiro completo

## 💾 Sistema de Salvamento

Os dados de progresso incluem:
- Encontros realizados
- Vínculo com personagens
- Encaminhamentos bem-sucedidos
- Pontuação total
- Timestamp do último progresso

**Localização**: Armazenado em `localStorage` do navegador (não requer servidor)

## 🔧 Desenvolvimento

### Requisitos
- Navegador moderno com suporte a Canvas
- Editor de texto (VS Code, Sublime, etc.)
- Git (opcional, para contribuir)

### Modificar o Jogo
1. Abra `index.html` em editor de texto
2. Edite diretamente o arquivo (contém CSS, JS e HTML)
3. Salve e recarregue no navegador

### Adicionar Conteúdo
- **Personagens**: Edite `assets/data/characters.json`
- **Cenários**: Edite `assets/data/scenarios.json`
- **Gráficos**: Substitua `assets/images/sprites.png`
- **Sons**: Adicione arquivos em `assets/sounds/`

## 🐛 Reportar Bugs

Encontrou um problema? Abra uma [Issue no GitHub](https://github.com/maikoldurand2-ops/cnr-bras-simulator/issues):

```
Título: [BUG] Descrição curta do problema
Descrição:
- Passos para reproduzir
- Comportamento esperado vs. atual
- Ambiente (navegador, SO, dispositivo)
```

## 💡 Sugestões de Melhorias

Tem ideias? Abra uma [Discussion](https://github.com/maikoldurand2-ops/cnr-bras-simulator/discussions) ou uma [Issue com label "enhancement"](https://github.com/maikoldurand2-ops/cnr-bras-simulator/issues/new?labels=enhancement)

## 🤝 Contribuindo

Este é um projeto de código aberto! Contribuições são bem-vindas.

Veja [CONTRIBUTING.md](CONTRIBUTING.md) para:
- Como configurar o ambiente de desenvolvimento
- Padrões de código
- Processo de Pull Request
- Código de conduta

## 📄 Licença

Este projeto está licenciado sob a **MIT License** - veja [LICENSE](LICENSE) para detalhes.

**Resumo**: Você pode usar, modificar e distribuir este software livremente, desde que inclua a licença original.

## 🌐 Links Úteis

- **GitHub**: https://github.com/maikoldurand2-ops/cnr-bras-simulator
- **Jogo Online**: https://maikoldurand2-ops.github.io/cnr-bras-simulator/
- **Consultório na Rua (PMSP)**: https://www.prefeitura.sp.gov.br/cidade/secretarias/saude/
- **Redução de Danos**: https://www.camara.leg.br/noticias/

## 👨‍💻 Autor

**Maikol Durand**  
GitHub: [@maikoldurand2-ops](https://github.com/maikoldurand2-ops)

## 🙏 Agradecimentos

- Equipes de Consultório na Rua da PMSP
- Profissionais de saúde mental e redução de danos
- Comunidade open-source de jogos educacionais

---

**Desenvolvido com ❤️ para educação em saúde e humanização do cuidado**
