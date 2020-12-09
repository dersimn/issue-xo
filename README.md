
Run `npm i` of course, then:

1) `npx xo`
    - Runs without errors
2) `cat index.js | npx xo --stdin`: 
    - Returns: `✖  2:5  myGlobalFunction is not defined.  no-undef`
    - However the `space: 4` option is respected.
    - `cat index.js | npx xo --globals myGlobalFunction --stdin` works
    - Maybe because `rules` are simply forwarded to eslint and all other options are parsed by XO ?

## Issues

xojs/xo#509
xojs/SublimeLinter-contrib-xo#17
