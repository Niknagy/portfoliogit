# Portfólio Flutter Web — Nikolas

Portfólio desenvolvido em **Flutter Web** a partir de um layout sugerido em texto, publicado no **GitHub Pages**.

🔗 **Acesse online:** https://niknagy.github.io/portfoliogit/

📦 **Repositório:** https://github.com/niknagy/portfoliogit

---

## Sobre o projeto

A página apresenta um projeto em destaque (um dashboard de e-commerce em tempo real) em formato de estudo de caso. O foco foi traduzir o layout em wireframe de texto para uma interface moderna, responsiva e escura, usando apenas widgets do Flutter, sem imagens externas.

## Seções da página

| Seção | Descrição |
|---|---|
| **Navbar** | Logo, nome e menu (Projetos, Sobre, Contato) com rolagem suave até cada seção. No celular vira um menu de três linhas. |
| **Card de destaque** | Tags, título, resumo e botões para o código no GitHub e o deploy em produção. |
| **Área visual** | Mockup de dashboard desenhado com widgets: KPIs e gráfico de barras. |
| **Problema e solução** | O desafio enfrentado e como foi resolvido. |
| **Arquitetura e tecnologias** | Tecnologias usadas, com badge e motivo da escolha. |
| **Características principais** | Cards de features (UI/UX responsivo, gráficos dinâmicos, autenticação). |
| **Resultados e lições** | Ganho de desempenho e aprendizados. |
| **Call to action** | Botões para contato por e-mail e LinkedIn. |

## Tecnologias

- [Flutter](https://flutter.dev/) (Web)
- [Dart](https://dart.dev/)
- [url_launcher](https://pub.dev/packages/url_launcher) para abrir links externos e e-mail
- GitHub Pages para hospedagem

## Responsividade

O layout se adapta ao tamanho da tela com `MediaQuery`:

- **Telas largas (≥ 820 px):** cards lado a lado e menu completo na barra superior.
- **Telas estreitas:** cards empilhados e menu em formato de lista suspensa.

## Como rodar localmente

Pré-requisito: [Flutter SDK](https://docs.flutter.dev/get-started/install) instalado. No Windows, é necessário ativar o **Modo de Desenvolvedor** para compilar projetos com plugins.

```bash
git clone https://github.com/niknagy/portfoliogit.git
cd portfoliogit/flutter_application_1
flutter pub get
flutter run -d chrome
```

## Como publicar no GitHub Pages

1. Gerar o build com o `base-href` igual ao nome do repositório:

   ```bash
   flutter build web --base-href /portfoliogit/ --release
   ```

2. Enviar o conteúdo de `build/web` para a branch `gh-pages`:

   ```bash
   cd build/web
   git init
   git add .
   git commit -m "Deploy Flutter Web"
   git branch -m gh-pages
   git remote add origin https://github.com/niknagy/portfoliogit.git
   git push -u origin gh-pages --force
   ```

3. No repositório, abrir **Settings → Pages**, selecionar a branch `gh-pages` com a pasta `/ (root)` e salvar.

Em 1 a 2 minutos o site fica disponível em `https://niknagy.github.io/portfoliogit/`.

## Estrutura

```
flutter_application_1/
├── lib/
│   └── main.dart        # Toda a aplicação (páginas, widgets e configurações)
├── web/                 # Arquivos da plataforma web (index.html, manifest)
└── pubspec.yaml         # Dependências do projeto
```

Os dados pessoais e os links (GitHub, deploy, e-mail e LinkedIn) ficam concentrados na classe `Cfg`, no topo do `main.dart`, o que facilita personalizar o portfólio.

## Autor

**Nikolas**

- GitHub: [@niknagy](https://github.com/niknagy)
