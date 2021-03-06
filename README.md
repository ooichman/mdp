
## mdp - A command-line based markdown presentation tool.

![image](https://cloud.githubusercontent.com/assets/2237222/4280231/d63178fa-3d2a-11e4-88a6-2b8e3608c4ca.gif)

---

***How to get started:***

mdp needs the ncursesw headers to compile.
So make sure you have them installed:
- on Ubuntu/Debian you need `libncursesw5` and `libncursesw5-dev`
- on Cygwin you need `libncursesw10` and `libncurses-devel`

Now download and install mdp:

    $ git clone https://github.com/visit1985/mdp.git
    $ cd mdp
    $ ./configure
    $ make
    $ make install
    $ mdp sample.md


- On Arch you can use the existing [AUR package](https://aur.archlinux.org/packages/mdp-git/).
- On Slackware, grab the SlackBuild here: (http://slackbuilds.org/apps/mdp/), or run `sbopkg -i mdp`
- On FreeBSD, you can use the port [misc/mdp](http://www.freshports.org/misc/mdp).
- On Redhat/Centos/Fedora you can use the mdp.spec file by tar the directory and rpmbuild it:

    $ tar -zcvf 0.93.0.tar.gz mdp/ && rpmbuild -ta 0.93.0.tar.gz
	
Most terminals support 256 colors only if the TERM variable is
set correctly. To enjoy mdp's color fading feature:

    $ export TERM=xterm-256color

---

***How to use it:***

Horizontal rulers are used as slide separator.

Supports basic markdown formating:

- line wide markup
    - headlines
    - code
    - quotes
    - unordered list

- in-line markup
    - bold text
    - underlined text
    - code

Supports headers prefixed by @ symbol.

- first two header lines are displayed as title and author
    in top and bottom bar

Review sample.md for more details.

---

***Controls:***

- h, j, k, l, Cursor keys,
    Space, Enter, Backspace,
    Page Up, Page Down - next/previous slide
- Home - go to first slide
- End - go to last slide
- 1-9 - go to slide n
- q - exit


---

***How to debug it:***

To make a debug version of `mdp`, just type:

    $ make DEBUG=1

