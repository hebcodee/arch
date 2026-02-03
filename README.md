# Instalação e Configuração de um Ambiente de Desenvolvimento Moderno com Arch Linux e Hyprland

Minhas configurações do HyprLand e WayBar


## **Personalização do Ambiente**

> Caso queira, você pode clonar esse repositório, que contém algumas configurações básicas para Hyprland, Waybar, Kitty, Zsh e outros programas:

```bash
git clone https://github.com/hebcodee/arch
```

### **Ajustes Importantes no `hyprland.conf`**

#### **Modo Escuro do Sistema**

```bash
sudo pacman -S xdg-desktop-portal-gtk xdg-desktop-portal-hyprland qt6ct
```

```ini
exec = gsettings set org.gnome.desktop.interface gtk-theme "adw-gtk3-dark"
exec = gsettings set org.gnome.desktop.interface color-scheme "prefer-dark"
env = QT_QPA_PLATFORMTHEME,qt6ct
```

#### **Gaps, teclado, atalhos e animações**

Ajuste livremente no mesmo arquivo, conforme o estilo desejado. Veja o arquivo `hyprland.conf` clonado para exemplos.

#### Waybar

Waybar é uma barra de status altamente personalizável para ambientes Wayland, como o Hyprland. Ela pode exibir informações úteis, a mais útil delas sendo as diferentes workspaces do hyprland. Também pode ser usada pra uma infinidade de outras funções, como mostrar a hora, uso de CPU, memória, rede, bateria e muito mais.

```
sudo pacman -S waybar
```

> Verifique alguns exemplos de configuração [aqui](https://github.com/Alexays/Waybar/wiki/Examples)

- Topicos:

  - [Por que Linux?](#por-que-linux)
  - [Por que Arch Linux?](#por-que-arch-linux)
  - [Arch Wiki](#arch-wiki)
  
## **Por que Linux?**

Linux é a base da maior parte da infraestrutura moderna: servidores, nuvem, containers, dispositivos embarcados e etc. O que significa que desenvolver em Linux coloca você no mesmo ecossistema usado em produção pelo mercado inteiro. As ferramentas mais poderosas disponíveis são nativas, o ambiente favorece automação e escrita de scripts, e a estabilidade geral torna o sistema previsível para trabalho diário.

Além disso, a filosofia open source permite auditar, modificar e ajustar praticamente qualquer componente, dando ao usuário um entendimento real do que está acontecendo “por baixo do capô”. Isso reduz limitações, aumenta a transparência e cria um ambiente onde o desenvolvedor não fica preso a decisões externas, mas constrói exatamente o sistema que precisa.

Como muitos, também interagi com computadores primeiro a partir do sistema da Microsoft, mas a realidade é que o ambiente não foi projetado tendo o desenvolvedor como público principal, o que resulta em ferramentas menos integradas, pipelines mais complexos e uma experiência que frequentemente depende de camadas adicionais e curativos: WSL, gerenciadores de pacotes externos, emuladores ou adaptações; vários componentes necessários para alcançar o mesmo fluxo natural que sistemas Unix-like oferecem nativamente.

## **Por que Arch Linux?**

O **Arch Linux** é uma distribuição independente, minimalista e flexível, construída sobre o princípio de entregar apenas o essencial: um sistema base limpo, pacotes próximos do **upstream** (a versão original mantida pelos desenvolvedores do software) e ferramentas simples que não escondem o funcionamento interno. Nada vem pré-configurado além do básico, e tudo o que compõe o ambiente é escolhido e entendido pelo próprio usuário.

Para desenvolvimento, esse modelo oferece um equilíbrio entre simplicidade e controle. O sistema não força estruturas rígidas nem impõe camadas de abstração que atrapalham a manutenção. Você monta um ambiente exatamente com as versões, serviços e bibliotecas que precisa e com documentação clara. Isso reduz atrito no dia a dia e evita a sensação de estar trabalhando contra o próprio computador.

O modelo **rolling release** complementa isso: você recebe atualizações contínuas, com versões recentes e compatíveis entre si, evitando o acúmulo de pacotes antigos que costuma gerar o **dependency hell**. Em vez de grandes atualizações que quebram tudo de uma vez, o sistema evolui de forma incremental e síncrona. Para quem desenvolve e precisa de ferramentas atualizadas sem perder estabilidade, esse fluxo é extremamente vantajoso.

## **Arch Wiki**

A **Arch Wiki** é uma das documentações mais completas e respeitadas do mundo Linux. Ela não só cobre o ecossistema do Arch Linux, mas também explica conceitos gerais de sistemas Unix-like que se aplicam a praticamente qualquer distribuição. É um recurso que incentiva autonomia, entendimento profundo do sistema e uma abordagem mais consciente sobre como cada componente funciona.

