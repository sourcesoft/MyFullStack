My own (Neo)Vim configuration which focuses on JS(React, Vue, TypeScript, Flow), CSS(and styled-components), GraphQL and GO, however also works with C#, Java, Python and Rust.
Configuration is based on Tmux, iTerm2, OSX but I also use it on Ubuntu.
I use Alt/CMD for some key mappings, so it's more suitable for Mac+iTerm.

![Vim](https://github.com/sourcesoft/dotfiles/blob/master/images/vim.png "vim")

![ZSH](https://github.com/sourcesoft/dotfiles/blob/master/images/zsh.png "vim")


## Installation

#### 1. Install required binaries
1. Have (Neo)Vim and Git installed ofcourse
2. Install Tmux and [plugins](https://github.com/sourcesoft/my-long-list/blob/master/.tmux.conf)
3. If using OSX: `brew install reattach-to-user-namespace`
4. [Rainbarf](https://github.com/creaktive/rainbarf)
5. [Oh My ZSH](https://github.com/robbyrussell/oh-my-zsh)
6. If you're running OSX install iTerm and [Dash.app](https://kapeli.com/dash)
7. Install [GO](https://golang.org/doc/install)
8. [The Silver Searcher](https://github.com/ggreer/the_silver_searcher)
9. Free `Inconsolata` font

#### 2. Backup your old configuration and get new ones
1. Backup the old one first: `mv ~/.vimrc ~/.vimrc.bak`
2. Replace it: `wget -O ~/.vimrc https://raw.githubusercontent.com/sourcesoft/my-long-list/master/.vimrc`
3. NeoVim uses XDG configuration: `ln -s ~/.vimrc ~/.config/nvim/init.vim`
4. Vim uses old `.vimrc` location so there's no need to create symlink.
5. Copy other config files in the repository like `.bash_profile`, `.gitconfig`, `.tern-config`, `.tmux.conf`, `.zshrc`, `.eslintrc.js`, `prettierrc`, `.gitignore`, `.prettierignore` and configure more if feel comfortable.
6. install [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md) and [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md) custom plugins for zsh.

#### 3. Download and install more (in order)
1. Before opening (Neo)Vim:
- Install necessary global node packages by running `npm install -g typescript neovim`
- Install global node packages for eslint `npm i -g eslint eslint-config-airbnb eslint-config-airbnb-base eslint-config-prettier eslint-plugin-import eslint-plugin-prettier prettier eslint-import-resolver-webpack eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react eslint-plugin-redux-saga redux-saga webpack babel-eslint` or install them in the project directory as a dev dependency.
- Compile [YouCompleteMe](https://github.com/Valloric/YouCompleteMe#mac-os-x). Remeber to have `xbuild`, `go`, `tsserver` ,`npm`, `node`, `cargo`, `rustc`, Java JDK installed to use `--all` flag.
- Open tmux running `tmux` and install tmux plugins with `Prefix + I`
- [Install vim-plug](https://github.com/junegunn/vim-plug)
- Download and install `Knack Nerd Font` from [here](https://github.com/enricobacis/.dotfiles/blob/master/osx-fonts/Library/Fonts/Knack%20Regular%20Nerd%20Font%20Complete.ttf) and configure iTerm2 to use it.
- Install plugins by running `vim +PlugInstall +qall` or `nvim +PlugInstall +qall` in terminal
2. Open (Neo)Vim and:
- Run `:UpdateRemotePlugins` in vim at the end.
- Open NeoVim(Vim) and run :GoInstallBinaries and then :TmuxLine
- Learn key bindings by reading this file

## Mappings and Environment

It's much easier to use right CMD or Alt instead of reaching out escape.
I also use Caps Lock for Control, since it's closer and easier to hit.
- Escape -> Right CMD or Right Alt
- Control -> Caps Lock

Tools to setup the key bindings:
- OSX: Use Karabiner to map
  - Visit: https://github.com/tekezo/Karabiner-Elements
- Ubuntu: Install xcape (https://github.com/alols/xcape)
  - Use the following command: `xcape -e 'Alt_R=Escape;ISO_Level3_Shift=Escape'`


#### Hex code mappings for iTerm:
- cmd-o: 0x01 0x29 --- tmux next session
- cmd-i: 0x01 0x28 --- tmux previous session
- cmd-j: 0x2C 0x73 0x6A --- vim jump page down
- cmd-k: 0x2C 0x73 0x6B --- vim jump page up
- cmd-m: 0x2C 0x6D --- vim quickfix previous
- cmd-n: 0x2C 0x6E --- vim quickfix next
- cmd-n: 0x2C 0x71 --- vim quickfix toggle
- cmd-p: 0x2C 0x70 --- vim run tmux command
- cmd-r: 0x2C 0x72 --- vim run last tmux command
- cmd-f: 0x2C 0x66 --- vim toggle fullscreen
- cmd-;: 0x2C 0x3B --- list buffers
- cmd-a: 0x2C 0x61 --- search current buffer subdirectory
- cmd-s: 0x2C 0x73 0x73 --- run ALEFix
- ctrl-space: 0x2C 0x76 --- lookup Dash.app docs

#### Troubleshooting to get NeoVim, iTerm and Tmux all work together smoothly:
- https://github.com/neovim/neovim/wiki/FAQ#how-can-i-change-the-cursor-shape-in-the-terminal
- https://github.com/neovim/neovim/wiki/FAQ#my-ctrl-h-mapping-doesnt-work
- https://github.com/neovim/neovim/issues/2048
- http://stackoverflow.com/questions/6778961
- http://stackoverflow.com/questions/39645253
- http://www.nthelp.com/ascii.htm
- http://superuser.com/questions/259614


### Tools as a developer
- [NeoVim](https://neovim.io) / [vimrc](https://github.com/sourcesoft/my-long-list/blob/master/.vimrc) / [ag](https://github.com/ggreer/the_silver_searcher) - Can't live without ya'll, not even a day.
- [iTerm2](https://www.iterm2.com/) / [zsh](https://github.com/robbyrussell/oh-my-zsh) / [tmux](https://tmux.github.io/) - Performant terminal and shell everywhere.
- [SourceTree](https://www.sourcetreeapp.com) - I can't remember all those weird hard to memorize git commands, so this is my GUI.
- [Transmit](https://panic.com/transmit/) - I'm using it for what it is and It's got everything I want.
- [Paw](https://paw.butt/) - Advanced REST client for testing my backend
- [Little Snitch](https://www.obdev.at/products/littlesnitch) - Sometimes I need to monitor I/O of an application I'm developing.
- [Charles](https://www.charlesproxy.com/) - Monitoring using all the tools even the ones I have no idea what they are.
- [Fritzing](fritzing.org/) - Easily design electronic circuits for Arduino in no time.
- [OsmondCocoa](www.osmondpcb.com/) - Sometimes I need to build a ready to print for some home-made circuits.

