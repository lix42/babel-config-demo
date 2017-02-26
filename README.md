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

For apps, you can use a mixed approach:

* Use Babel helpers and – if necessary – the Regenerator runtime via module imports, as explained for libraries.
* Install the ES6 standard library globally. Modules have the advantage that a bundler will only deploy the functionality that is actually used by the app. But a global polyfill lets you write code that will eventually run natively without any changes. I find that more important.
* Given that Regenerator is already taken care of, you don’t need babel-polyfill; core-js is enough.