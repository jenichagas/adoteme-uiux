# Projeto: Adoteme

**Disciplina:** Projeto de Interface com Usuário UI/UX
**Curso:** Analise e Desenvolvimento de Sistemas
**Semestre:** 2026/2
**Integrante:**
- Jeniffer Chagas - 6924206914

---

## 1. Resumo do Projeto

O **Adoteme** é uma plataforma digital que conecta animais resgatados, cães, gatos e outros pets, a famílias interessadas em adotar. O produto nasceu como um app/PWA (desenvolvido originalmente para o meu Trabalho de Conclusão de Curso) e, neste trabalho, sua interface foi adaptada e recriada como um **site institucional estático**, seguindo o mesmo design, paleta de cores e fluxo de navegação já validados no Figma.

O problema que o Adoteme resolve é a dificuldade de tutores temporários, protetores independentes e ONGs em divulgar animais resgatados para um público amplo, e a dificuldade de futuros adotantes em encontrar, filtrar e conversar diretamente com quem cuida do animal antes de decidir adotar.

O público-alvo são pessoas de 18 a 45 anos que já têm ou desejam ter um pet, moram em áreas urbanas e valorizam a adoção responsável em vez da compra de animais. O principal diferencial do Adoteme é permitir o contato direto entre tutor e adotante (chat/telefone), com perfis completos de cada animal (saúde, temperamento, peso, raça) , reduzindo a burocracia sem abrir mão da responsabilidade no processo.

---

## 2. UX Research

### 2.1. Persona

**Nome:** Laís Vicente
**Idade:** 29 anos
**Profissão:** Designer, trabalha em home office
**Biografia:** Laís mora sozinha em um apartamento em Cariacica (ES) e sempre quis ter um gato, mas nunca teve certeza de onde procurar um animal para adoção de forma confiável. Ela já resgatou informalmente alguns animais de rua e hoje cuida temporariamente da gata Amora, que está pronta para ser adotada por uma família definitiva.
**Objetivos:** Encontrar um lar responsável para os animais que resgata; adotar, no futuro, um segundo pet para fazer companhia ao primeiro.
**Dores:** Falta de um canal único e confiável para divulgar pets resgatados; dificuldade em avaliar se um possível adotante é realmente responsável; perder tempo com processos de adoção burocráticos ou pouco transparentes.

### 2.2. Mapa de Empatia

| Dimensão | Descrição |
|---|---|
| **Pensa e sente** | Quer garantir que o animal vá para um lar seguro; teme que a adoção não dê certo e o pet seja devolvido às ruas. |
| **Vê** | Grupos de Facebook e WhatsApp desorganizados cheios de anúncios de adoção sem nenhum filtro ou verificação. |
| **Fala e faz** | Publica fotos e vídeos dos animais resgatados; conversa bastante antes de aprovar um adotante; pede referências. |
| **Dores** | Processo lento, pouca visibilidade dos anúncios, dificuldade de organizar conversas com vários interessados ao mesmo tempo. |
| **Ganhos** | Um lugar único, visual e organizado, onde pode cadastrar o pet, conversar com interessados e acompanhar o status da adoção. |

### 2.3. Jornada do Usuário

Etapas da tarefa principal — **adotar um pet**:

1. **Descoberta** — o usuário acessa a home, vê o banner de destaque e entende a proposta do Adoteme.
2. **Busca** — usa a barra de busca ou filtra pets por categoria (gato, cachorro, hamster).
3. **Exploração** — navega pelo grid de pets disponíveis e identifica um que combina com ele.
4. **Avaliação** — abre o perfil detalhado do pet (sexo, raça, peso, descrição, tutor responsável).
5. **Contato** — entra em contato com o tutor por telefone ou mensagem para tirar dúvidas.
6. **Conversão** — preenche o formulário de interesse em adoção ou cria uma conta para continuar a conversa.

---

## 3. Arquitetura da Informação

### 3.1. Sitemap

```
Adoteme
├── Home (index.html)
├── Pets (pets.html)
│   └── Detalhe do Pet (pet.html)
├── Sobre (sobre.html)
└── Contato (contato.html)
    ├── Formulário de adoção/mensagem (#adotar)
    └── Entrar / Cadastrar (#entrar)
```

### 3.2. User Flow — Adotar um pet

```
[Home] → [Busca / Categoria] → [Pets (catálogo)] → [Detalhe do Pet]
   → [Contato com o tutor] → [Formulário de adoção em Contato] → [Confirmação]
```

---

## 4. Wireframes

O wireframe e a identidade visual originais do projeto foram desenvolvidos no Figma, como parte do TCC "Adoteme":

🔗 **Figma:** https://www.figma.com/design/cBK0lnEhJfxNLUaupqb5mv/adotepet

As páginas HTML deste trabalho recriam, em formato de site responsivo, as principais telas do protótipo: onboarding/hero, busca e categorias, listagem de pets, detalhe do pet, chat/contato e conta do usuário.

---

## 5. Identidade Visual

### 5.1. Paleta de cores

| Cor | Hex | Uso |
|---|---|---|
| Primária (roxo) | `#7C6BAA` | Botões principais, links ativos, ícones de destaque |
| Primária escura | `#5F4F8A` | Hover de botões, texto sobre fundo claro |
| Primária clara | `#EDE9F7` | Fundos suaves, tags, chips |
| Superfície | `#FFFFFF` | Fundo principal |
| Superfície suave | `#F7F5FC` | Fundos alternados, campos de formulário |
| Texto | `#2E2A3D` | Títulos e texto principal |
| Texto secundário | `#726D85` | Legendas, texto de apoio |
| Coração / favoritos | `#E8544E` | Ícone de "favoritar" |

### 5.2. Tipografia

- **Display (títulos):** Poppins — pesos 600/700/800, fonte geométrica e arredondada que transmite acolhimento.
- **Corpo de texto:** Nunito Sans — pesos 400/600/700, alta legibilidade em telas pequenas.

### 5.3. Componentes

- **Botões:** pílula (`border-radius: 999px`), com variantes primária (preenchida) e outline; efeito de elevação sutil no hover.
- **Cards de pet:** cantos arredondados, sombra suave, imagem com proporção 5:4 e botão de favoritar sobreposto.
- **Chips de categoria:** ícone circular + texto, usados para filtros e navegação por categoria.
- **Campos de formulário:** fundo levemente tonalizado, borda que reage ao foco/preenchimento.

---

## 6. Estrutura do Código

```
262.uiux/
├── README.md
├── index.html        → Home (hero, busca, banner, categorias, pets em destaque)
├── pets.html          → Catálogo completo, filtros e tabela-resumo por categoria
├── pet.html           → Perfil detalhado de um pet (Amora)
├── sobre.html         → Missão, impacto, como funciona e valores
├── contato.html       → Formulário de adoção/contato e acesso à conta
├── style.css          → Arquivo único de estilos, organizado por seções comentadas
└── assets/
    └── img/           → Ícones em SVG (favicon, logo, categorias, avatar) e fotos reais dos pets e do banner (PNG/JPG/WEBP)
```

O menu mobile (hambúrguer) foi implementado apenas com HTML e CSS, usando a técnica do *checkbox hack*, sem depender de JavaScript, conforme exigido no enunciado.

---

## 7. Instruções de Execução

Abra o arquivo `index.html` diretamente no navegador, ou utilize a extensão **Live Server** do VS Code para navegar entre as páginas com atualização automática.

---

## 8. Referências

- Protótipo original no Figma: *Adotepet* (TCC da autora)
- MDN Web Docs — HTML e CSS: https://developer.mozilla.org
- Google Fonts — Poppins e Nunito Sans: https://fonts.google.com
- Documentação da disciplina 262.UIUX — Projeto de Interface com Usuário
