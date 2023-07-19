# Composer-Version-Manager
CVM - Composer Version Manager

# Intro
CVM allows you to quickly install and use different versions of composer via the command line.

Example:
```
$ composer --version
install composer version latest-stable
Composer version 2.5.8 2023-06-09 17:13:21
$ export COMPOSER_VERSION=1; composer --version
install composer version latest-1.x
Composer version 1.10.26 2022-04-13 16:39:56
$ export COMPOSER_VERSION=2; composer --version
install composer version latest-2.x
Composer version 2.5.8 2023-06-09 17:13:21
$ export COMPOSER_VERSION=2.1.0; composer --version
install composer version 2.1.0
Composer version 2.1.0 2021-06-03 11:30:09
$ export COMPOSER_VERSION=2.1.0; composer --version
Composer version 2.1.0 2021-06-03 11:30:09
```

It's as simple as that!

Afterwards you can continue simply callling "composer" - it's a wrapper script which will automatically forward commands to the actual composer binary.

# About
CVM is a version manager for composer, which installs wanted composer versions locally and run them transparency. CVM works on any POSIX-compliant shell (sh, dash, ksh, zsh, bash), in particular on these platforms: unix, macOS, and windows WSL.

# Install & Update
For installation, the Composer Wrapper should be added to one directory included in PATH, e.g. for a global installation on the host:
```
$ wget -O /usr/local/bin/composer https://raw.githubusercontent.com/Fabian123333/Composer-Version-Manager/main/composer
$ chmod +x /usr/local/bin/composer
```

It's also possible to install the composer Wrapper in the Userspace, e.g. by:
```
$ mkdir -p $HOME/.bin
$ wget -O $HOME/.bin/composer https://raw.githubusercontent.com/Fabian123333/Composer-Version-Manager/main/composer
$ echo 'export PATH="$HOME/.bin:$PATH"' >> $HOME/.bashrc
<restart the bash / ssh session>
```

# Additional Notes

The version is specified by default by the `$COMPOSER_VERSION` environment variable.
