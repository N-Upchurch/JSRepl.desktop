# JSRepl.desktop
*A .desktop file that launches a quick JavaScript REPL in KWrite and Konsole*

If you're anything like me:
* You're an avid KDE user
* You've been using tools like [RunJS](https://github.com/lukehaas/RunJS) to try things out, fix bugs, format text, et cetera, but... 
    * you think [Electron](https://github.com/electron/electron) should die in a fire,
    * you want to use FLOSS tools where at all possible, 
    * ...and you don't really need all sorts of fancy features anyway. 

Well, here you go, friend. This quick and dirty .desktop file creates `repl.js` in the liminal space that is your `/tmp/` directory, opens it in KWrite, and opens up a Konsole window that watches `/tmp/repl.js` for changes and runs them in node using nodemon (IE, gives you a barebones JavaScript REPL).

## Screenshot:
![image](https://user-images.githubusercontent.com/8893713/223494042-20b4915b-382e-43b2-8d4b-16dbc265be56.png)

## Dependencies:
* KWrite
* Konsole
* Node
* Nodemon

## Installation:
Drop JSRepl.desktop wherever it needs to live on your system:
```bash
wget https://raw.githubusercontent.com/N-Upchurch/JSRepl.desktop/main/JSRepl.desktop -P ~/.local/share/applications/
```
## Use:
1. Open your application launcher and click on JSRepl to launch
2. Write some JavaScript
3. Save to run your code (or if you're really fancy, and brave, turn on autosave in KWrite)

## FAQs:
* Does it work with TypeScript? 
    * My guy, if I wanted *types* I'd learn a *real* programming language.
* Does it have X feature?
    * Probably not; it's just a .desktop file. Feel free to submit a PR if you have ideas.
* Do I have to use KWrite and Konsole?
    * Not if you change the program names in JSRepl.desktop, but you're on your own there.
* What happens to repl.js when I'm done with it?
    * It's deleted the next time you restart your machine.
* What if I want to keep repl.js or save it somewhere else? 
    * Either save a copy somewhere else using KWrite, or copy it from `/tmp/`:
    `sudo cp /tmp/repl.js /my/new/dir/`
