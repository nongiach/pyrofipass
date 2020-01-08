# QuicKeepass
QuicKeepass is a tool that allows you to quickly paste password from your Keepass database using keyboard shorcuts.

# How to use
* Type <Alt+u> to start QuicKeepass
* Enter your keepass Master Passwod
* Type <Enter> to Autofill username and password

## Keyboard shortcuts

* $mod+u      =>      Start QuicKeepass
* Enter       =>      Autofill username and password
* Alt+Enter   =>      Autofill type password only

## How to install
```sh
$ sudo pip3 install quickeepass
```

## How to configure

Add one of the bellow lines to your ~/.config/i3/config

### i3 Basic configuration: Master Password
```
bindsym $mod+u exec "quickeepass REPLACE_WITH_YOUR_KEEPASS.kdbx"
```

### i3 Advanced configuration 1: Keyfile

If you use a keyfile you want need to type the master password everytime.
Please read about keepass keyfile option.

```
bindsym $mod+u exec "quickeepass REPLACE_WITH_YOUR_KEEPASS.kdbx --keyfile your.key"
```

### i3 Advanced configuration 2: Keyfile and Password

```
bindsym $mod+u exec "quickeepass REPLACE_WITH_YOUR_KEEPASS.kdbx --keyfile your.key --password"
```

### Rofi theme

Add the bellow arguments to change the theme

```--rofi_args '-theme solarized'```

### For other Window manager

This should work perfectly, just see the above commands and adapt the start command, pull requests are welcom.

    # rofi_conf = f'-matching fuzzy' # fuzzy matching is not that good here
    # -theme solarized  # if you want to change theme

## Warning
QuicKeepass is not a replacement to Keepass it only wraps Keepass to allow you to efficiently paste your passwords on Linux.

----
By [@chaignc][] [#HexpressoTeam][hexpresso].


[hexpresso]:     https://hexpresso.github.io
[@chaignc]:    https://twitter.com/chaignc
