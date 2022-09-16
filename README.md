# My build of st - simple terminal

[st](https://st.suckless.org/) is a simple terminal emulator for X which sucks
less.


## Requirements

In order to build st you need the Xlib header files.


## Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Additonal features in this build

- Colors from Xresources
- A blinking cursor
- Deleting with backspace and DEL keys
- Desktopentry for st (to find it in graphical application menus)
- Possibility of declaring multiple fonts (for correct visualization of special
  characters like emojis)
- Scrolling in terminal buffer using keyboard and mouse. Also works in
  software like 'less'
- Vertically center text in line (useful when having set a big chscale in
  config.h)
- Usage of only one clipboard (CLIPBOARD)
- Setting the default font size of the terminal using the '-z' option
