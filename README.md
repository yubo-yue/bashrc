== Colored Manpages

$ mkdir ~/.terminfo/ && cd ~/.terminfo
Now get the terminfo description:
$ wget http://nion.modprobe.de/mostlike.txt
Now compile it using tic (the terminfo entry-description compiler)
$ tic mostlike.txt
(you may want to delete the mostlike.txt file after compiling)

And then just define an alias in the rc file of your favorite shell.
alias man="TERMINFO=~/.terminfo/ LESS=C TERM=mostlike PAGER=less man"
