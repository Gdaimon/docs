# Cygwin

```
Install-Package cygwin
```

## Check packages

- ssh
- nano
- wget
- git
- fish

## Configure HOME

```
mkpasswd -l -p "$(cygpath -H)" > /etc/passwd
```

* Manually edit `/etc/passwd` to set default to `zsh` or `bash`.

## Configure ZSH

```
git clone git@github.com:robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

## Configure Oh My Fish

```
git clone https://github.com/oh-my-fish/oh-my-fish
cd oh-my-fish
bin/install --offline
```


## Configure PATH Start

```
nano etc/fish/conf.d
Edit:
	# Start in $HOME
	if not set -q CHERE_INVOKING
		cd /path

	end
```


## Configure fish

```
nano etc/nsswitch.conf
add end line:
db_shell: /usr/bin/fish
```

## Install theme Oh My Fish
```
 omf install agnoster
```
