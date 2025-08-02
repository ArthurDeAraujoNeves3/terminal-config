# Linux Terminal

![Terminal](/docs/LINUX/terminal.png)

<div align="center">
<img src="https://img.shields.io/badge/Fedora-Distro?style=plastic&logo=fedora&logoColor=white&labelColor=%2351A2DA&color=%2351A2DA" />
<img src="https://img.shields.io/badge/zsh-shell?style=plastic&logo=zsh&logoColor=white&labelColor=%23F15A24&color=%23F15A24" />
</div>

## Links

1. [zsh download guide](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
2. [Oficial zsh Themes](https://github.com/ohmyzsh/ohmyzsh/wiki/themes)
3. [powerlevel10k Repository](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh)
4. [Nerd Fonts](https://www.nerdfonts.com/font-downloads)

## 1. Install **zsh**

```shell
sudo dnf install zsh
```

Change your default shell to zsh with this command
```shell
chsh -s $(which zsh)
```

## 2. Oh My Zsh

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Commnad to access the zsh config file
```shell
nano ~/.zshrc
```

### Themes

[powerlevel10k Repository](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh)

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"
```

```shell
...
ZSH_THEME="powerlevel10k/powerlevel10k" # ~/.zshrc
...
```

After that, reopen your terminal to complete the theme instalation, answer the first questions until your reach **Prompt Style**

Now, follow this steps: 

- Select **Classic**
- Select **Unicode**
- Select **Dark**
- Select **No**
- Select **Angled**
- Select **Sharp**
- Select **Flat**
- Select **One Line**
- Select **Compact**
- Select **Few Icons**
- Select **Concise**
- Select **No**

### Nerd Fonts

The font i'm use is **JetBrainsMono Nerd Font**.

To use this font, set the font family as **JetBrainsMono Nerd Font** in terminal configurations

![Font Family](/docs/LINUX/font.png)

[Download here](https://www.nerdfonts.com/font-downloads)

### Plugins

#### Syntax Highlight
```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git\
echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
source ./zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

#### Auto Suggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

```shell
...
plugins(... zsh-autosuggestions)
...
```
