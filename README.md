# telegram-kybot
## A chatbot for Telegram, written in PHP

### Setting up tg to be used with telegram-kybot
In order to efficiently parse the output of tg, there were some changes needed to the source code of tg (in essence, the removal of color tags in the output).
I already have done this in my fork of the tg repository.

<pre>
mkdir /etc/telegram/
git clone https://github.com/kenniki/tg.git /etc/telegram/
cd /etc/telegram
./configure
make
</pre>

Make sure you have the needed dependencies installed for the compilation to succeed.
Refer to the tg README.
The tg fork will not be kept up to date, so if you want a current version of it, please use the official repository and make the changes yourself.

kybot expects tg to reside in <code>/etc/telegram</code>. If you change that, you will need to modify the kybot files accordingly.

After you installed tg, run it and complete the initial setup. Once done, you can install kybot.

Finally, install gentoo.

### Installing kybot
<pre>mkdir /var/dev/telegram-kybot/
git clone https://github.com/kenniki/telegram-kybot.git /var/dev/telegram-kybot/
cd src
./start.sh</pre>

That's basically it.
The path kybot resides in shouldn't matter, but it's possible I fuck up and hardcode some shit and then it will not work.
The above path is what I use.

### Writing modules
Take a look at the example module in the <code>modules</code> folder. It should be self-explanatory. If it isn't, don't write a module.

