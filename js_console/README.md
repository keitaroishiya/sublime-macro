#sublime-macro to generate javascript console.log()
=============

Macro files and key setting for Sublime Text 2 to generate console.log() automatically.

[super+shift+l] use a word(variable) the caret points, and generates
console.log(word);

[super+shift+ctrl+l] use a word(variable) the caret points, and generates
console.log("word:" word);

[super+shift+alt+l] generate just
console.log(": " + );


##Activation

Please copy sublime-macro files to Packages/User/ Directory (Of course, you can choose your own)
Then, open "Preferences Key Bindings - User"
and add key bind settings below.

```
[
    {
        "keys": ["super+shift+alt+l"],
        "command": "run_macro_file",
        "args": {
            "file": "Packages/User/console_log.sublime-macro"
        }
    },
    {
        "keys": ["super+shift+ctrl+l"],
        "command": "run_macro_file",
        "args": {
            "file": "Packages/User/console_log_paste.sublime-macro"
        }
    },
    {
        "keys": ["super+shift+l"],
        "command": "run_macro_file",
        "args": {
            "file": "Packages/User/console_log_simple.sublime-macro"
        }, 
        "context":[
            { "key": "selection_empty", "operator": "equal", "operand": true, "match_all": true }
        ]
    }
]
```
