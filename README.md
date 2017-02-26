# Babel configuration demo

Playground for examining how various options affect the output of Babel 6.

* Install (everything you need is installed locally):

    ```
    cd babel-config-demo/
    npm install
    ```

* Build once:

    ```
    npm run build
    ```

* Watch files, build whenever there are changes:

    ```
    npm run watch
    ```

For libraries, you must not touch global variables, which is why everything must come from imports:

* Babel helpers: babel-plugin-transform-runtime and babel-runtime work well.
* Regenerator runtime: The previous combo also provides the regenerator runtime via imports. If you don’t use or transpile generators then you can switch off this part of babel-plugin-transform-runtime.
* Standard library: I don’t like that babel-plugin-transform-runtime enables ES6 methods (e.g. Array.prototype.repeat()) via non-standard global methods (e.g. Array.repeat()). It’d switch this part of the plugin off and use core-js directly.