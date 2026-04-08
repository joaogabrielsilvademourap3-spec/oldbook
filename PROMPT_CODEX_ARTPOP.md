# Prompt para Codex — App estilo ARTPOP (PWA sem dependências)

## Contexto
Você é um engenheiro front-end sênior. Construa um app web inspirado no espírito do ARTPOP: imersivo, experimental, visualmente orgânico e com navegação radial.

## Objetivo
Desenvolver um **PWA completo e offline-first**, sem bibliotecas externas, com:
- Interface não tradicional (radial/circular/orbital)
- Núcleo interativo chamado **AURA**
- Módulos integrados de Música, Arte, Social e Perfil
- Visual Frutiger Aero + neon + glassmorphism

## Restrições técnicas (obrigatórias)
1. **Não usar NPM, CDN, frameworks ou libs externas**.
2. Somente:
   - HTML
   - CSS
   - JavaScript puro (Vanilla)
3. Dados persistidos localmente via **LocalStorage** (simulação de API local).
4. App instalável como PWA com `manifest.json` + `service-worker.js`.
5. Funcionar offline após primeiro carregamento.
6. Código com estrutura modular e sem erros no console.

## Estrutura de arquivos esperada
```txt
/app
  index.html
  /css
    style.css
  /js
    app.js
    aura.js
    music.js
    social.js
    art.js
  /assets
    sounds/
    images/
  manifest.json
  service-worker.js
```

## Experiência principal (AURA CORE)
Criar tela principal com:
- Esfera central animada (AURA)
- Itens orbitais ao redor da esfera:
  - Música
  - Galeria
  - Social
  - Perfil
  - Criar Arte

Interações:
- Arrastar para girar o “sistema solar”
- Clique/toque para entrar em módulo
- Hover/touch com resposta orgânica (escala, brilho, leve distorção)

## Direção visual (obrigatória)
- Estilo: Frutiger Aero + glass + rave conceitual
- Paleta base:
  - Azul neon `#00d4ff`
  - Rosa `#ff2fd1`
  - Verde ácido `#39ff14`
- Fundo com gradientes fluidos + partículas
- Botões em formato blob orgânico (não retangulares)
- Uso de blur/transparência (`backdrop-filter`)
- Glow dinâmico e profundidade por camadas
- Parallax suave

## Módulo Música
Implementar player custom (sem UI padrão visível):
- Play/Pause
- Próxima/Anterior
- Loop
- Lista local de faixas (JSON interno)
- Visualização reativa (barras/partículas pulsando)

## Módulo Art Creator
Canvas de criação visual com:
- Formas orgânicas
- Ajuste de cor, tamanho e movimento
- Salvar criação no LocalStorage
- Reabrir e remixar criação existente

## Módulo Social (offline/local)
Feed local com posts simulados:
- Cada post: imagem gerada + texto
- Ações: curtir, remixar
- Badge especial: “visualizado pelo sistema 👁️” (simulado)

## Módulo Perfil/Aura
Perfil com:
- Nome
- Cor da aura
- Nível de usuário

Regras:
- Nível aumenta com uso/interações
- Cor/estado da aura muda com atividade (música, arte, social)

## Animações e performance
- Usar `requestAnimationFrame` para órbitas e partículas
- Microinterações suaves (`ease-in-out`)
- Modo “Performance” para reduzir animações em dispositivos lentos
- Tema dinâmico (claro/escuro) se possível

## Critérios de aceite
1. Interface principal radial funcional.
2. Todos os módulos navegáveis e persistentes via LocalStorage.
3. PWA instalável e funcionando offline.
4. Sem dependências externas.
5. Sem erros no console.
6. Experiência visual coerente com conceito “universo vivo”.

## Entrega solicitada
Entregue em etapas nesta ordem:
1. Código completo de `index.html`
2. Código completo de `css/style.css`
3. Código completo de `js/app.js`
4. Código completo de `js/aura.js`
5. Código completo de `js/music.js`
6. Código completo de `js/social.js`
7. Código completo de `js/art.js`
8. Código completo de `manifest.json`
9. Código completo de `service-worker.js`
10. Guia rápido de execução local e teste offline

No final, inclua checklist de validação e próximos passos de evolução.
