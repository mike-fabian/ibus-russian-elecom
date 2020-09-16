# ibus-russian-elecom

Russian [ibus](https://github.com/ibus/ibus) layout for using a Japanese Elecom keyboard

I type in English, Russian and Japanese, all using a Japanese keyboard.
These are mostly like a regular US QWERTY keyboard, but with some exceptions, e.g. extra keys and non-letter characters in odd locations.

The existing ibus layouts for Russian don't seem to work well with this keyboard, so I made my own using instructions from [here](http://www.studymongolian.net/technical/how-to-create-linux-input-method-editor/).

## The layout

![layout.png](layout.png)

## Install instructions

```
git clone git@github.com:mpenkov/ibus-russian-elecom.git
sudo ibus-table-createdb -n /usr/share/ibus-table/tables/russian-elecom.db -s ibus-russian-elecom/russian-elecom.txt
ibus-daemon -drx
ibus-setup
```

The last command will open the ibus configuration utility.
Go to the "Input method" tab, click on "Add", then "Russian", and "Russian - Russian (Elecom)" should show up.
