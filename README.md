# zsh-clipboard

This is a copy of the [clipboard][1] library from [oh-my-zsh][2], packaged as a zsh plugin to be used with your favorite zsh plugin manager.

[1]: https://github.com/robbyrussell/oh-my-zsh/blob/master/lib/clipboard.zsh
[2]: https://github.com/robbyrussell/oh-my-zsh
[3]: http://zsh.sourceforge.net/

## Requirements

* [ZSH][3] >= 4.3.0

## Install

### antigen

    antigen bundle twang817/zsh-clipboard

### zgen

    zgen load twang817/zsh-clipboard
    
### antibody

    antibody bundle twang817/zsh-clipboard
    
## Usage

System clipboard integration

This file has support for doing system clipboard copy and paste operations from the command line in a generic cross-platform fashion.

On OS X and Windows, the main system clipboard or "pasteboard" is used.  On other Unix-like OSes, this considers the X Windows CLIPBOARD selection to be the "system clipboard", and the X Windows `xclip` command must be installed.

### clipcopy - Copy data to clipboard

    <command> | clipcopy  - copies stdin to clipboard    
    clicopy <file>        - copies a file's contents to clipboard
    
### clippaste - "Paste" data from clipboard to stdout

    clippaste             - writes clipboard's contents to stdout
    clippaste | <command> - pastes contents and pipes it to another process
    clippaste > <file>    - paste contents to a file
