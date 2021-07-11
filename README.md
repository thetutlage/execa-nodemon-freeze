# Execa node freezes

The repo has a total of three files

- `index.js` just require the `nodemon` package
- `exec.js` runs the `node index.js` using the `execa` function.
- `exec-node.js` runs the `index.js` using `execa.node` function.

The `exec-node.js` freezes forever. I see that `nodemon` listens for `process.on('message')` event in `lib/utils/bus.js:28` file and if I remove this code form the `nodemon` source, then the `exec-node.js` script also dies successfully.
