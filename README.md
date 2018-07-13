twinejs
-------

### A NOTE ABOUT YARN

Any time you read `npm` below, you can also use `yarn` ([more
information](https://yarnpkg.com/)). Using `yarn` is a little more foolproof, as
it ensures that everyone is using the exact same version of dependencies.

### INSTALL

Run `npm install` at the top level of the directory to install all goodies.

### BUILDING

Run `npm start` to begin serving a development version of Twine to
http://localhost:8080. This server will automatically update with changes you
make. You can also create a dev build at `build/` with `npm run build`.

`npm run lint` and `npm test` will lint and test the source code respectively.

`npm run clean` will delete existing files in `build/` and `dist/`.

