Geocoding is the process of converting addresses (like a street address) into geographic coordinates (like latitude and longitude).
This quickstart uses [**hello-react**](https://hasura.io/hub/project/hasura/hello-react/deployment-instructions) as a base to implement the backend and frontend services of the project along with react-native code.

## What does this come with?

* Custom service that integrates with the Google Maps Geocoding API: https://developers.google.com/maps/documentation/geocoding/start 

  *  Allow user to enter an address or a set of latitude/longitude coordinates.
   * Use the backend API to display a Google maps based interface that shows the directions between the source and destination and travel time.

## How to get it running?

### Reqirements

In order to get this app running, you must have the following:
1. [hasura CLI tool](https://docs.hasura.io/0.15/manual/install-hasura-cli.html) (hasura).

2. Expo client (XDE). Download from https://expo.io/tools

3. NodeJS

(For more such apps, check out https://hasura.io/hub)


## Deployment instructions

### Basic deployment:

* Press the **Clone & Deploy** button and follow the instructions.
* The `hasura quickstart` command clones the project repository to your local computer, and also creates a **free Hasura cluster**, where the project will be hosted for free.
* A git remote (called hasura) is created and initialized with your project directory.
* Now get your cluster name using `hasura cluster status` and modify the App.js file inside `microservices/ui/app/src` and change the cluster name in from airborne24 -> your cluster-name. 
* Modify the server.js file inside `microservices/api/src` and change the Api key
* Run `git add .`, `git commit`, and `git push hasura master`.
* Run the below command to open your shiny new deployed Geocoding app.
``` shell
$ hasura microservice open ui
```

### Opening the Mobile app (React-Native)

- Open Expo XDE, do a login/signup and click on `Open existing project...`. Browse to the Geocoding-T49 directory and open the react-native folder.
- Once the project loads, click on Share.
- Scan the QR code using the Expo app from your phone (Install from Playstore/Appstore)
- Fully working app will open on your phone

```
Note: You can open the app with any of your desired react-native simulators. We prefer Expo because of its simple onboarding for beginners.
```
## Web version of App (React-JS)

![React-JS](https://github.com/Ash-D23/Geocoding-T49/blob/master/readme-assets/react-js.png)

## Mobile Version of App (React-native)

![React-native](https://github.com/Ash-D23/Geocoding-T49/blob/master/readme-assets/React-native-2.png)

### Making changes and deploying

* To make changes to the frontend part , browse to `/microservices/ui/app/src` and edit the `App.js` file in the folder according to your app or if you already have an existing code migrate them on to the folder
*To make changes to the backend part, browse to `/microservices/ui/app/src` and edit the server.js file in the folder according to your app or if you already have an existing backend code replace them on to the folder 
* Commit the changes, and perform `git push hasura master` to deploy the changes.


## Local development

To test and make changes to this app locally, follow the below instructions.
* Open Terminal and `cd` into the project folder
* Run `npm install` to install all the project dependencies
* Run `npm start` and `npm build` in the terminal to build and run it.
* Make changes to the app, and see the changes in the browser

## View server logs

You can view the logs emitted by the ‘serve’ package by running the below command:

``` shell
$ hasura microservice logs ui
```
You can see the logs in your terminal, press `CTRL + C` to stop logging.

## Managing app dependencies

* System dependencies, like changing the web-server can be made in the Dockerfile
* npm/yarn deps can be managed by editing **package.json**.

If changes have been done to the dependencies, `git commit`, and perform `git push hasura master` to deploy the changes.

## Migrating your existing React.js app

* If you have an existing react app which you would like to deploy, replace the code inside `/microservices/ui/src/` according to your app.
** If you have an existing node app which you would like to deploy, replace the code inside `/microservices/api/src/` according to your app.
* You may need to modify the Dockerfile if your `package.json` or the build directory location has changed, but in most cases, it won't be required.
* Commit, and run `git push hasura master` to deploy your app.

## Adding backend features

Hasura comes with BaaS APIs to make it easy to add backend features to your apps.

### Add instant authentication via Hasura’s web UI kit

Every project comes with an Authentication kit, you can restrict the access to your app to specific user roles.
It comes with a UI for Signup and Login pages out of the box, which takes care of user registration and signing in.

![Auth UI](https://docs.hasura.io/0.15/_images/uikit-dark.png)

Follow the [Authorization docs](https://docs.hasura.io/0.15/manual/users/uikit.html) to add Authentication kit to your app.

### Addding Microservices

Hasura project is composed of a set of microservices. These include certain Hasura microservices like, postgres, nginx, data API, auth API and more but can also include your own microservices.

* [Adding Microservice](https://docs.hasura.io/0.15/manual/custom-microservices/index.html)

### Add data APIs

Hasura comes with set of Data APIs to access the Postgres database which comes bundled with every Hasura cluster.
Detailed docs of data APIs can be found [here](https://docs.hasura.io/0.15/manual/data/index.html).
