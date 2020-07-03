First of all you need to install Oracle Digital Assistant node sdk.

`npm install -g @oracle/bots-node-sdk`{{execute}}

Then, move into the same folder where the VSCode workspace is.

`cd ODAComponents`{{execute}}

Now you create the folder for our component.

`mkdir weather-component`{{execute}}

And go to that folder.

`cd weather-component`{{execute}}

Then you need to initialize our component. As it is a node.js application, you need to create package.json file.
'-y' options means no questions are asked and the file is created with default values (Just for the hands-on, in your real projects you will assign the right values)

`npm init -y`{{execute}}

Then you need to configure the SDK into our project.

`bots-node-sdk init`{{execute}}

Last but not least, in order to execute the component locally you need to install express module as a development dependency.

`npm install --save-dev express`{{execute}}









`bots-node-sdk service -P 3000`{{execute}}