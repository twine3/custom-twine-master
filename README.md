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

### DEPLOYMENT

Twine3 is deployed with Google's [Firebase](https://firebase.google.com/). First, install firebase with 

``` bash
npm install -g firebase-tools
```

To begin actual deployment, first run the command: 

``` bash
npm run build
```

After that, you'll need to login with firebase with 

```bash
firebase login
```

From the root directory of Twine, run the following command:

``` bash
firebase init
```

For each of the questions, answer as follows: 

#### Question 1

``` bash
? Which Firebase CLI features do you want to setup for this folder? Press Space to select features, then Enter to confirm your choices. (Press <space> to select)
```

``` bash
Hosting
```

#### Question 2

``` bash
? Your public directory is the folder (relative to your project directory) that will contain Hosting assets to be uploaded with firebase deploy. If you have a build process for your assets, use your build's output directory.? What do you want to use as your public directory?
```

``` bash
./build
```

#### Question 3 

``` bash
? Configure as a single-page app (rewrite all urls to /index.html)? (y/N) 
```

``` bash
y
```

#### Question 4 

``` bash
? Configure as a single-page app (rewrite all urls to /index.html)? (y/N)
 ```

 ``` bash
 N
 ```

 Finally, you can deploy the website with 

 ``` bash
firebase deploy
```
