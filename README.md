### .zschrc
```javascript
autoload -U compinit && compinit
zmodload -i zsh/complist

# auto-completion
if [ -f /opt/local/etc/profile.d/bash_completion.sh ]; then
  . /opt/local/etc/profile.d/bash_completion.sh
fi

function parse_git_branch() {
    git branch 2> /dev/null | sed -n -e 's/^\* \(.*\)/[\1]/p'
}

setopt PROMPT_SUBST
export PROMPT='%F{grey}%n%f %F{cyan}%~%f %F{green}$(parse_git_branch)%f %F{normal}$ %f'
```



### Git Commands
  - Commit para alguns dias anteriores ..... ```git commit --date="3 day ago" -m "happy new year" ```
  - Configurando o nome do usuário ......... ```git config --global user.name "FIRST_NAME LAST_NAME"```
  - Configurando o email do usuário ........ ```git config --global user.email "MY_NAME@example.com"```
  - Reverter todas as alterações ........... ```git checkout .```
  - Copiar um repositório .................. ```git clone```
  - Adicionar todas as alterações .......... ```gitt add -A```
  - Criando o commit ....................... ```git commit -M```
  - Enviando o commit ...................... ```git push origin [BRANCH_NAME]```
