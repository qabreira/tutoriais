## OpenJDK

**Instalação do Java no linux para a utilização de recursos para desenvolvimento.**

Por padrão, as distros linux já trazem o OpenJDK instalado.
Vamos remover todas as versões instaladas e então fazer a instalação da que desejamos.

    sudo apt autoremove 'openjdk-*' --purge

Após isso, se digitarmos `java --version` ou `javac --version` no terminal, não deve retornar nenhuma opção disponível.

Então vamos instalar o OpenJDK desejado com o comando:

    sudo apt install openjdk-17-jdk

A versão 17 é uma das últimas LTS neste momento.

---

Feita a instalação, vamos configurar as variáveis de ambiente.
O primeiro passo é identificar o locar onde o Java está instalado através do comando:

    sudo update-alternatives --config java

É provável que retorne algo como:

    /usr/lib/jvm/java-17-openjdk-amd64/bin/java

Deste endereço, o que nos interessa é apenas o caminho até a versão: `/usr/lib/jvm/java-17-openjdk-amd64`

Vamos definir a variável no arquivo `~/.zshrc` ou `~/.bashrc`, dependendo do que está em uso no sistema operacional.
Editamos o arquivo e inserimos as seguintes linhas (caso não estiverem disponíveis):

    JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
    export JAVA_HOME
    export PATH=$PATH:$JAVA_HOME

Após isso basta fechar e abrir ou terminal, ou então, recarregar o arquivo de configuração com `source ~/.zshrc`.
Pronto, agora para garantir que a configuração funcionou, rodamos `echo $JAVA_HOME` e deve retornar o que acabamos de configurar.
