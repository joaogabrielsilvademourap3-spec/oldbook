# Prompt para o Codex — App estilo ARTPOP (PWA offline, sem dependências)

## Papel
Você é um engenheiro front-end e de experiência interativa. Construa um app web **inspirado no conceito do ARTPOP** (estética futurista/caótica + exploração radial), sem copiar marcas registradas, assets protegidos ou identidade proprietária.

## Objetivo
Criar um **PWA completo e instalável**, com visual imersivo e arquitetura modular, onde a navegação acontece em torno de um núcleo chamado **AURA**.

## Restrições técnicas (obrigatórias)
1. **Sem NPM, sem CDN, sem bibliotecas externas**.
2. Apenas:
   - HTML
   - CSS
   - JavaScript vanilla
3. Persistência local com **LocalStorage** (ou IndexedDB, se necessário), sem backend externo.
4. Deve funcionar offline (Service Worker + cache).
5. Código sem erros de console.
6. Acessibilidade mínima: foco visível, labels em botões e contraste aceitável de texto.

## Estrutura de arquivos obrigatória
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
    /sounds
    /images
  manifest.json
  service-worker.js
```

## Conceito de UX/UI
- App como “universo interativo”.
- Núcleo central AURA + módulos orbitando.
- Navegação radial/circular, com arrasto para girar os módulos.
- Estética: **Frutiger Aero + glassmorphism + neon**.

### Paleta base
- Azul neon: `#00d4ff`
- Rosa elétrico: `#ff2fd1`
- Verde ácido: `#39ff14`
- Fundo escuro profundo com gradientes fluidos.

### Linguagem visual
- Botões não retangulares (blobs/orgânicos).
- Camadas com profundidade + leve parallax.
- Glow dinâmico e blur.
- Feedback de interação: escala + brilho + “respiração”.

## Telas e módulos

### 1) Tela Principal — AURA CORE
- Esfera central animada (CSS ou canvas).
- Módulos orbitais clicáveis:
  - Música
  - Galeria/Arte
  - Social
  - Perfil
  - Criar
- Arrastar/touch move gira o anel orbital.
- Clique abre módulo com transição suave.

### 2) Música
- Player custom (não exibir UI nativa do `<audio>`).
- Lista local de faixas (JSON local).
- Controles: play/pause, próxima, anterior, loop.
- Visualizador reativo com barras/partículas simuladas sincronizadas com estado do player.

### 3) ART CREATOR
- Área canvas para criar formas orgânicas.
- Controles: cor, tamanho, intensidade de movimento.
- Salvar criação localmente.
- Remix: abrir criação salva e editar novamente.

### 4) Social (simulado offline)
- Feed local com posts (texto + imagem gerada/captura do canvas).
- Ações: curtir, remixar.
- Selo visual “visualizado pelo sistema” (efeito especial, sem referência de marca real).

### 5) Perfil/AURA
- Nome do usuário.
- Cor principal da aura.
- Nível baseado em atividade (interações, posts, criações).
- Estado da aura evolui com uso (cor, brilho, partículas).

## Sistema de estado
- Criar store local simples em JS para:
  - `user`
  - `aura`
  - `music`
  - `artworks`
  - `posts`
  - `settings`
- Salvar no LocalStorage com versionamento simples (`schemaVersion`).
- Migrar dados antigos quando necessário.

## Animações (obrigatórias)
- `requestAnimationFrame` para órbitas e partículas.
- Parallax suave no fundo conforme ponteiro.
- Transições `ease-in-out`.
- Modo performance para reduzir efeitos:
  - menos partículas
  - menor blur
  - animações simplificadas

## PWA (obrigatório)
- `manifest.json` com nome, ícones, tema e display standalone.
- `service-worker.js` com:
  - cache de app shell
  - fallback offline
  - versionamento de cache
- Registrar SW em `app.js`.

## Critérios de aceite
1. App abre offline após primeiro carregamento.
2. Navegação radial funciona por mouse e toque.
3. Módulos principais funcionam sem dependências externas.
4. Persistência de perfil, posts e artes ao recarregar.
5. Sem erros no console durante uso básico.
6. Layout responsivo para mobile (>=360px) e desktop.

## Entrega esperada do Codex
Implemente em etapas, nesta ordem:
1. Estrutura de arquivos + HTML base.
2. Sistema de layout e tema visual (CSS).
3. Núcleo AURA e navegação orbital.
4. Módulos (music, art, social, perfil).
5. Persistência local + estado global.
6. PWA (manifest + SW).
7. Polimento de animações + modo performance.
8. Checklist final de testes manuais.

## Importante
- Não simplificar para menu tradicional.
- Não usar frameworks.
- Não usar assets externos remotos.
- Manter estética experimental, porém com usabilidade mínima.
