### Link For Discussion/Doubts: [Discuss any doubts on this page](https://gdgnd.org/gdg-new-delhi/events/web-developer-days-1/session-discussions?speaker_resource=30)

## Steps for this CodeLab

### Pre-requisites
- Sign up on Google Cloud Platform(if you've not already)
- Activate the [GCP free trial](https://console.cloud.google.com/freetrial/signup/tos?_ga=2.84344729.-1032321293.1549865094)
- Install the [Cloud SDK](https://cloud.google.com/sdk/)
- Working NodeJS and Angular app from previous codelab
- A little familiarity with the Terminal/Powershell/Command Prompt

### Install the following (use google!)
- Node.js (version > 10)

### Adding the app.yaml file

Now before we move on to the deployment, there are a few changes we need to make to the current app:
1. Create a new file and name it as `app.yaml`.
2. Add the following code in it.
```
runtime: nodejs
env: flex
```
3. Now, in the `index.js` file, change the port to 8080 as the app engine runs the app on port 8080.
4. The next step involves adding the node version to the `package.json` file,
    Add the engine under the scripts key `"engines": { "node": ">=9.3.0" },`.
5. Next, we need to provide the starting point to the VM, add `"start": "nodemon index.js",` inside the `scripts`.


### Setting up a new project
As we are all set with the code changes, our app is now ready to get deployed. Follow the next steps in order to create a project on Google cloud console:
1. Log into the [GCP console](https://cloud.google.com/)
2. Create a new project. Make sure you give it a relevant name.

### Preparing for Deployment
1. There is a cloud shell icon on the navigation bar. Click on the icon to activate the in-browser shell. This is going to provide you a Virtual Machine to work on.
2. Now, clone your repository into the VM.
3. Make sure that the package.json contains "start" script.
4. Click on the hamburger icon and GOTO `Source Repositories`. 
5. Click on `Add repository` in front of the project name.
6. Choose the `Connect external repository` option and click on Continue button.
7. Add GitHub as the Git provider.
8. Check the checkbox giving consent to Gcloud to source your repositories from Github and Click on `Connect to GitHub` button.
9. Select the repo to be connected and click on `Connect Selected repository`.
10. After the repository is sourced in the Google Cloud, click on `Cloud Console` on the navbar.


### Deploying using Cloud Shell
1. Once you are onto the cloud console page, activate the Cloud Shell Machine by clicking on the 
`Activate Cloud Shell` icon on the right of the navbar.
2. Once the cloud shell is up and running, clone the repository using `https`.
`git clone <https://github.com/---->`
3. `cd` into the directory which was created as a result of the above step.
4. Here comes the final step: `gcloud app deploy`.
5. You will be provided the URL of the deployed app: `https://<project-id>.appspot.com/`
6. Hit it up in the browser and there you have your node application live!

    
### You can now find [ASSIGNMENT] tags in every file, try them on your own
 - Some links (look out for documentation in each)
    - Mongoose: https://mongoosejs.com/
    - Express.js: https://expressjs.com/
    - Node.js: https://nodejs.org/en/
    - MongoDB: https://www.mongodb.com/
