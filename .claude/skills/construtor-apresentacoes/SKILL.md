---
name: construtor-apresentacoes
description: Gere apresentações HTML refinadas a partir de roteiros de vídeo, outlines ou briefs de tema. Produz um deck HTML completo em arquivo único, com CSS e JavaScript embutidos, usando as referências de design e templates de slides fornecidas.
---

## Descrição

Gere apresentações HTML refinadas a partir de roteiros de vídeo, outlines ou briefs de tema.

Esta skill transforma conteúdo bruto em um deck de slides `.html` completo, em arquivo único, com:
- navegação com scroll-snap
- navegação por teclado
- navegação por pontos
- animações suaves
- hierarquia visual forte
- design dark-tech premium

O output deve ser sempre um **único arquivo HTML** com CSS e JavaScript embutidos.  
Nenhuma dependência externa é permitida, exceto Google Fonts.

Esta skill DEVE usar os arquivos de referência fornecidos:
- `references/design-system.md` → define sistema visual, cores, tipografia, espaçamento e direção estética
- `references/slide-templates.md` → define padrões HTML e limites de conteúdo para cada tipo de slide
- `assets/template.html` → estrutura base, motor de layout, navegação e sistema de animação

Essas referências não são opcionais — elas devem guiar todas as decisões.

---

## Princípios Centrais

- Toda apresentação deve parecer **intencional e premium**
- Nunca gere slides genéricos ou com aparência padrão
- O design deve seguir uma **estética escura, moderna, de alto contraste**
- Os slides devem ser **limpos, legíveis e focados**
- Uma ideia clara por slide

---

## Processo

### 1. Analise o Input

Leia o roteiro, outline ou tema e extraia:
- narrativa central (qual é a história?)
- seções principais
- transições entre ideias
- elementos-chave (listas, comparações, citações, etapas, visuais etc.)

---

### 2. Mapeie o Conteúdo para Tipos de Slide

Associe cada parte do conteúdo ao tipo correto de slide usando `slide-templates.md`.

Exemplos:
- abertura → Slide de Título
- afirmação forte → Citação / Declaração
- múltiplos itens → Grade de Conteúdo
- comparação → Layout de duas colunas
- etapas → Lista Numerada
- métricas → Slide de Estatísticas
- UI / visual → Slide de Screenshot
- encerramento → CTA

NÃO invente novos layouts, a menos que seja absolutamente necessário.

---

### 3. Aplique o Sistema de Design

Use `design-system.md` para definir:
- paleta de cores (variáveis CSS)
- tipografia (combinação de Google Fonts)
- ritmo de espaçamento e layout
- estilo de componentes (cards, grades, estatísticas etc.)
- tom visual (escuro, premium, focado em tecnologia)

Toda apresentação deve parecer personalizada, não baseada em template genérico.

---

### 4. Construa a Apresentação

Comece a partir de `assets/template.html`.

Para cada slide:
1. Selecione o padrão HTML correto em `slide-templates.md`
2. Insira o conteúdo respeitando os limites
3. Aplique as classes `.animate` e `.delay-N`
4. Mantenha estrutura e espaçamento limpos
5. Garanta que o slide caiba em uma viewport

---

### 5. Verifique

Antes de finalizar:

- Todo slide cabe em `100vh`
- Não existe rolagem interna
- Screenshots têm seus próprios slides
- A navegação (pontos + teclado) funciona
- As animações disparam corretamente
- A numeração dos slides está correta
- As fontes foram carregadas corretamente

---

## Regras

1. Uma viewport por slide. Nunca deixe transbordar.  
2. Screenshots devem ficar isolados.  
3. O output deve ser um único arquivo HTML.  
4. Scroll-snap é obrigatório.  
5. A navegação por teclado deve funcionar.  
6. A navegação por pontos deve existir e sincronizar com os slides.  
7. As animações devem ser suaves e escalonadas.  
8. A numeração dos slides deve estar presente.  
9. Evite design genérico a todo custo.  
10. Respeite os limites de conteúdo de `slide-templates.md`.

---

## Formato de Output

Sempre retorne:
- um arquivo `.html` completo  
- pronto para abrir no navegador  
- sem explicações, apenas o conteúdo do arquivo  

---

## Objetivo

Transformar ideias brutas em **apresentações de slides de alta qualidade e prontas para produção**  
que pareçam ter sido criadas por um profissional — não geradas.
