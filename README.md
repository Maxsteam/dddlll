telegram-bot
============

[![Donate button](https://img.shields.io/badge/nepal-donate-yellow.svg)](http://www.nrcs.org/donate-nrcs "Donate to Nepal Red Cross Society")

A Telegram Bot based on plugins using [tg](https://github.com/vysheng/tg).

[Installation](https://github.com/yagop/telegram-bot/wiki/Installation)
------------
```bash
# Tested on Ubuntu 14.04, for other OSs check out https://github.com/yagop/telegram-bot/wiki/Installation
sudo apt-get install libreadline-dev libconfig-dev libssl-dev lua5.2 liblua5.2-dev libevent-dev make unzip git redis-server g++ libjansson-dev libpython-dev expat libexpat1-dev
```

```bash
# After those dependencies, lets install the bot
cd $HOME
git clone https://github.com/yagop/telegram-bot.git
cd uzzbot
./launch.sh install
./launch.sh # Will ask you for a phone number & confirmation code.
```

Enable more [`plugins`](https://github.com/uziins/uzzbot/tree/master/plugins)
-------------
See the plugins list with `!plugins` command.

Enable a disabled plugin by `!plugins enable [name]`.

Disable an enabled plugin by `!plugins disable [name]`.

Those commands require a privileged user, privileged users are defined inside `data/config.lua` (generated by the bot), stop the bot and edit if necessary.


Run it as a daemon
------------
If your Linux/Unix comes with [upstart](http://upstart.ubuntu.com/) you can run the bot by this way
```bash
$ sed -i "s/yourusername/$(whoami)/g" etc/uzzbot.conf
$ sed -i "s_telegrambotpath_$(pwd)_g" etc/uzzbot.conf
$ sudo cp etc/uzzbot.conf /etc/init/
$ sudo start uzzbot # To start it
$ sudo stop uzzbot # To stop it
```


------------
Bot: [uzzbot](https://telegram.me/uzzbot)

[Join](https://telegram.me/joinchat/ALJ3iwFAhOCh4WNUHAyzXQ) on the TelegramBot Discussion Group.
or
[Join](https://telegram.me/joinchat/045d20af01e2c643263fec0188be277b) for uzzbot support.
