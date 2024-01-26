# ZSH

**Maior produtividade no terminal linux**

Para instalar o **ZSH**, rode este comando:

    sudo apt install zsh

Com o ZSH instalado, vamos turbiná-lo com o **Oh My ZSH**. Para isso, rode:

    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Para definir como shell padrão, rode:

    sudo usermod --shell $(which zsh) $USER

É interessante reiniciar o computador antes de prosseguir.

---

As configurações do ZSH são feitas no arquivo `~/.zshrc`. Vamos habilitar alguns plug-ins e, para isso, precisamos editar o arquivo e inserir o nome do plug-in dentro da categoria `plugins=(xyz)`. Por exemplo:

    plugins=(
		    git
		    systemd
		    zsh-syntax-highlighting
		    zsh-autosuggestions
		    )
	ZSH_THEME="powerlevel10k/powerlevel10k"

Após cara alteração use o comando `source ~/.zshrc` para recarregar o arquivo e ativar os plug-ins.

---

**zsh-syntax-highlighting** - deixa os comandos verdes quando digitados corretamente, ou, do contrário, pode marcá-los em vermelho. Para instalar, rode:

    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

---

**zsh-autosuggestions** - sugere comandos com base no histórico de execuções.

    git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

---

Também podemos aplicar alguns temas para melhorar a cara do nosso terminal.

Vamos instalar o **Powerlevel10K**. Como estamos usando o Oh My ZSH, podemos executar este comando:

    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

Em seguida, vamos incluir a linha abaixo no arquivo `~/.zshrc`:

    ZSH_THEME="powerlevel10k/powerlevel10k"

Lembre-se de comentar a linha que estava habilitando o tema utilizado anteriormente.

Pronto, basta seguir os passos de configuração de acordo com suas preferências e utilizar o terminal customizado.

---

Referência: https://sgoncalves.tec.br/zsh-para-maior-produtividade-no-terminal-linux/
