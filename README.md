# HOW TO USE
    
    export LANG=en
    python tt.py
    >>> I love you

    export LANG=zh_CN.utf8
    python tt.py
    >>> 我爱你


# Notes about gettext

When you want to use gettext in your application. Follow 4 steps:

* Import gettext, and wrapp string you want to translate in _()
* Insert the entry point of your code: gettext.install()
    
    gettext.install(domain[, localedir[, unicode[, codeset[, names]]]])
    
    :domain is the name of *.mo file. For example, if mo file named
    nova.mo, then `gettext.install('nova')`
    
    :localedir: the path of locale dir, if not specified, use
    `/usr/share/locale`. The structure of locale dir may like.
    
    locale
    ├── uk
    │   └── LC_MESSAGES
    ├── vi
    │   └── LC_MESSAGES
    ├── wa
    │   └── LC_MESSAGES
    ├── wo
    │   └── LC_MESSAGES
    ├── xh
    │   └── LC_MESSAGES
    ├── zh_CN
    │   └── LC_MESSAGES
    ├── zh_HK
    │   └── LC_MESSAGES
    ├── zh_TW
    │   └── LC_MESSAGES
    └── zu
        └── LC_MESSAGES

    And the *.mo file should be located in LC_MESSAGES.

* Set the system language. For example: 

    export LANG=zh_CN.utf8

* Run the program.
