## Hadoop Shell Command Auto-completion

## Usage

Similar to the Bash auto-completion you use every day, press the <kbd>TAB</kbd> key twice: <kbd>TAB</kbd><kbd>TAB</kbd>.

## Installation without [Bash Completion](http://bash-completion.alioth.debian.org)

* Get the script, assuming you save it to `~/bin/hadoop-completion.sh`:

```
    curl https://raw.githubusercontent.com/guozheng/hadoop-completion/master/hadoop-completion.sh -so ~/bin/hadoop-completion.sh && chmod +x ~/bin/hadoop-completion.sh
```
* Add to your `~/.bash_profile` (for Mac) or `~/.bashrc` for (other platform) to call the script:

```
    if [ -f ~/hadoop-completion.sh ]; then
      . ~/hadoop-completion.sh
    fi
```
* Either source your `~/.bash_profile` (for Mac) or `~/.bashrc` for (other platform), or open a new terminal and start using `hadoop-completion` script.


## Installation with [Bash Completion](http://bash-completion.alioth.debian.org)

### On Mac OS X

* Install [Homebrew](http://brew.sh), see instructions on its website.

* Install Bash Completion using Homebrew: `brew install bash-completion`.

* Add to your `~/.bash_profile` to use Bash Completion:

```
    if [ -f $(brew --prefix)/etc/bash_completion ]; then
      . $(brew --prefix)/etc/bash_completion
    fi
```

* Install `hadoop-completion.sh` to the Bash-Completion script directory `/usr/local/etc/bash_completion.d`.

```
    curl https://raw.githubusercontent.com/guozheng/hadoop-completion/master/hadoop-completion.sh -so ~/bin/hadoop-completion.sh && chmod +x ~/bin/hadoop-completion.sh
```

* Either source your `~/.bash_profile` or open a new terminal and start using `hadoop-completion` script.


### On other platforms

* Install Bash Completion according to the [instructions on its website](http://bash-completion.alioth.debian.org/#installing).

* Add `hadoop-completion` script to one of the following directories:

  * `/etc/bash_completion.d`
  * `/usr/local/etc/bash_completion.d`
  * `~/bash_completion.d`

For example:
```
    curl https://raw.githubusercontent.com/guozheng/hadoop-completion/master/hadoop-completion.sh -so ~/bash_completion.d/hadoop-completion.sh && chmod +x ~/bash_completion.d/hadoop-completion.sh
```

* Either source your `~/.bashrc`, or open a new terminal and start using `hadoop-completion` script.


## Credits

Inspired and modified based on the hadoop completion script from [Facebook/hadoop-20](https://github.com/facebook/hadoop-20/blob/master/src/contrib/bash-tab-completion/hadoop.sh), which does not work with my hadoop installed using [Homebrew](http://brew.sh), so I modified it and also added a couple more commands.
