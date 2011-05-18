# TermKit

![TermKit Icon](https://github.com/unconed/TermKit/raw/master/Illustrator/TermKit%20Icon%20128.png)

### Goal: next gen terminal / command application

Addresses following problems:

1. Monospace character grid with ansi colors is not rich enough to display modern files / media / visualizations / metadata. Cannot effectively handle large output, long/wide tables or direct interaction.
1. Relying on anonymous pipes to transfer data around is error-prone
 * Human-friendly text results in ambiguities
 * Need to match formats at pipe ends
 * Confusion between data output and notification output
1. Synchronous input/output makes you wait. SSH keystroke latency is frustrating.
1. String-based command line requires arcane syntax, results in mistakes, repeated attempts at escaping, etc.
1. Unix commands are "useless by default", and when asked, will only tell you raw data, not useful facts. e.g. "rwxr-xr-x" instead of "You can't edit this file."

![TermKit 0.3 alpha](https://github.com/unconed/TermKit/raw/master/Mockups/Shot-0.3.png)
![TermKit 0.3 alpha](https://github.com/unconed/TermKit/raw/master/Mockups/Shot-Self-Commit.png)
![TermKit 0.3 alpha](https://github.com/unconed/TermKit/raw/master/Mockups/Shot-Highlight.png)

### Warning: Alpha version, still under development. Nothing works yet.

## Some cool features

* Smart token-based input with inline autocomplete and automatic escaping
* Rich output for common tasks and formats, using MIME types + sniffing
* Asynchronous views for background / parallel tasks
* Full separation between front/back-end

## TermKit is not a...
* ...Web application. It runs as a regular desktop app.
* ...Scripting language like PowerShell or bash. It focuses on executing commands only.
* ...Full terminal emulator. It does not aim to e.g. host 'vim'.
* ...Reimplementation of the Unix toolchain. It replaces and/or enhances built-in commands and wraps external tools.

## How to use:

1. [Install node.js and npm](http://howtonode.org/how-to-install-nodejs).
2. install node-mime: `npm install mime`
3. Clone the TermKit repository: `git clone git@github.com:unconed/TermKit.git --recursive`
4. Run the NodeKit daemon: `cd TermKit; cd Node; node nodekit.js`
5. Unzip and run the Mac app in Build/TermKit.zip

*Tip:* Press ⌥⌘C to access the WebKit console.

Includes:
* “NSImage+QuickLook” by Matt Gemmell (http://mattgemmell.com/source).
* SyntaxHighlighter by Alex Gorbatchev (http://alexgorbatchev.com/SyntaxHighlighter/)
* jQuery and jQuery UI