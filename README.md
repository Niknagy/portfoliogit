# Portfólio Flutter Web — Nikolas

Portfólio desenvolvido em **Flutter Web** a partir de um layout sugerido em texto, publicado no **GitHub Pages**. O próprio portfólio é o projeto em destaque, e a página também reúne os exercícios feitos durante o curso de Desenvolvimento de Software Multiplataforma (FATEC).

🔗 **Acesse online:** https://niknagy.github.io/portfoliogit/

📦 **Repositório:** https://github.com/niknagy/portfoliogit

---

## Sobre o projeto

O objetivo foi traduzir um wireframe em texto para uma interface moderna, responsiva e escura, usando apenas widgets do Flutter, sem imagens externas. O layout é organizado como um estudo de caso, com problema, solução, tecnologias, features e resultados.

## Seções da página

| Seção | Descrição |
|---|---|
| **Navbar** | Logo, nome e menu (Projetos, Sobre, Contato) com rolagem suave até cada seção. No celular vira um menu de três linhas. |
| **Card de destaque** | Tags, título, resumo e botões para o código no GitHub e o site publicado. |
| **Área visual** | Mockup desenhado com widgets: cards de informação e gráfico de barras. |
| **Problema e solução** | O desafio de transformar um layout em texto em uma interface real e como foi resolvido. |
| **Arquitetura e tecnologias** | Flutter, Dart e GitHub Pages, com o motivo de cada escolha. |
| **Características principais** | UI/UX responsivo, widgets customizados e deploy no GitHub Pages. |
| **Resultados e lições** | Resultado final e aprendizados do projeto. |
| **Exercícios das aulas** | Cards com os exercícios desenvolvidos no curso (veja abaixo). |
| **Call to action** | Botões para contato por e-mail e LinkedIn. |

## Exercícios das aulas

| Exercício | O que aborda |
|---|---|
| 👋 **Hello World** | Primeiro app em Flutter: AppBar, texto, imagem dos assets e ícone em uma `Column`. |
| 📦 **TechStorage** | Gestão de inventário no terminal com `List`, `Map`, parâmetros nomeados e relatório de depreciação. |
| ⚔️ **RPG de Turno** | Combate por turnos com orientação a objetos: herança, encapsulamento, classes abstratas, composição e polimorfismo. |
| 🎲 **Batalha entre Jogadores** | Jogo de batalha no terminal com `Map`, `Random`, laços e validação de dados. |

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

> Se a versão antiga continuar aparecendo depois de publicar, abra o site em uma aba anônima: o Flutter Web guarda o app em cache.

## Estrutura

```
flutter_application_1/
├── lib/
│   ├── main.dart        # Página principal (navbar, destaque, seções e contato)
│   └── aulas.dart       # Seção "Exercícios das aulas"
├── web/                 # Arquivos da plataforma web (index.html, manifest)
└── pubspec.yaml         # Dependências do projeto
```

Os dados pessoais e os links (GitHub, site, e-mail e LinkedIn) ficam concentrados na classe `Cfg`, no topo do `main.dart`, o que facilita personalizar o portfólio.

## Autor

**Nikolas**

- GitHub: [@niknagy](https://github.com/niknagy)
