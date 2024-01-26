## ASDF
**Instalar e gerenciar versões para trabalhar com diferentes linguagens de programação.**

O processo de instalação está bem detalhado na página do projeto:
https://asdf-vm.com/guide/getting-started.html

Porém, caso utilize o terminal ZSH com o Oh My ZSH, então estes passos são o suficiente.

1 - Baixar o ASDF na pasta desejada:

    git clone https://github.com/asdf-vm/asdf.git ~/.asdf

2 - Declarar o plug-in do ASDF no arquivo `~/.zshrc`:

    plugins=(asdf)

Com isso ele já deve estar disponível para a utilização.

---

Exemplos de uso:

    asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git
    asdf list all nodejs
    asdf install nodejs latest
    asdf global nodejs latest
    asdf local nodejs latest
