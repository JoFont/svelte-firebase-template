
# Svelte Firebase Template

This is a project template for [Svelte](https://svelte.dev) apps integrated with [Firebase](https://firebase.google.com/). It was forked from the [original template project for Svelte](https://github.com/sveltejs/template) and all the necessary configuration for Firebase has already been done.


## Installation

Please create a project on Firebase beforehand by going to the [Firebase Console](https://console.firebase.google.com), clicking create a new Project. Next create an app inside the Firebase project by clicking +Add app and following the wizard. *The app and the project can have different names, this will not interfere with the proccess*

Lastly, configure Firestore and Hosting inside your newly created app.

*This is essential because preconfigured apps cannot be deployed before you choose the location of specific resources for your project, in creating a Firestore DB instance, it'll prompt you to choose a location, therefore completing the setup. [Learn More about this](https://firebase.google.com/docs/projects/locations)*


To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):
```bash
npm i -g firebase-tools
firebase login
npx degit JoFont/svelte-firebase-template svelte-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

Configure Firebase project by editing ```.firebaserc``` like so:
```bash
{
  "projects": {
    "default": "<THE-EXACT-NAME-OF-YOUR-FIREBASE-PROJECT>"
  }
}
```

*Note that this is the name of the project and not the app inside of the project.*

...then start [Rollup](https://rollupjs.org) & Firebase Server:

```bash
npm run dev
```

*Avoid using other development servers when using Firebase as it can only run on localhost with the built in server unless, other forms of integration are used wich, are besides the scope of this template.*

Navigate to [localhost:3000](http://localhost:3000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.


## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

Deploy with:

```bash
npm run deploy
```

