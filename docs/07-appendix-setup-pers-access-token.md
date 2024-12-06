## Appendix A - Set up a personal access token

Here are the steps to set up a personal access token.

From your gitlab repository, select the setting's icon.  From the drop down menu, choose 'Preferences'

![](/images/select-preferences.gif) <br><br>

Next, select 'Access tokens'.  Then select 'Add new Token'

![](/images/add-new-token.gif) <br><br>

1. Give the token a name.  
1. Set the expiration date (e.g. 1 month).
1. Select 'api', 'read repository' and 'write repository'
1. Select the 'Create personal access token' button.

![](/images/create-access-token.gif) <br><br>

Your new personal access token will appear.  Copy it to notepad as we will need it in a moment.

![](/images/new-pers-access-token.gif) <br><br>

Once you have the token, go to the gitlab instance in your cluster.  Select the janus-idp-gitops project

![](/images/your-gitlab-instance.gif) <br><br>

Go into the 'charts/backstage' directory, and select the 'backstage-rhtap-values.yaml' file. 

![](/images/backstage-rhtap-values.gif) <br><br>


Open the file and search for 'integrations'.

![](/images/search-for-integrations.gif) <br><br>

Inside the 'Integrations' section, there will be a gitlab section.  It will automatically fill in one of the sections which is this instance of gitlab.

![](/images/autofill-section.gif) <br><br>

We need to add another section, which is the consulting gitlab which is the AI Odyssey gitlab.  The API, base url and host are all going to be the same every single time because it's static.  The 'token' is going to be the 'token' we saved earlier.

![](/images/earlier-token.gif) <br><br>

Next, go to OpenShift.  Choose Networking->routes, and choose the openshift gitops project.

![](/images/choose-gitops.gif) <br><br>

We want the routes.  Note: this argocd-server is different that the one listed on the demo platform console.  Click on it's associate 'location' link.

![](/images/associated-location.gif) <br><br>

You will see the Argo instance.  In this page you will see different applications running.  Click into 'backstage'

![](/images/select-backstage.gif) <br><br>

Select the 'tiny triangle' on the end of the 'Refresh' button, until it shows the text 'hard refresh'.  Click on the 'hard refresh' text.  This will start things to cycle.

![](/images/click-tiny-button.gif) <br><br>

Go to your OpenShift dashboard.  Choose Workloads -> ConfigMaps and look for the 'backstage' project.

![](/images/backstage-project.gif) <br><br>

You will see the backstage-developer-hub-app-config.  Select the link so that you can see the details.

![](/images/backstage-developer-hub-app-config.gif) <br><br>

Click the YAML option.  This YAML should look familiar, because it is the YAML that we updated in gitlab.

![](/images/updated-yaml.gif) <br><br>

And finally here is the new section we added.  This is how we verify that our changed have actually rolled out.  You can select the 'Cancel' button to exit.

![](/images/verify-changes.gif) <br><br>

Next go back to the OpenShift dashboard and select Workloads -> Pods.  You'll see the backstage initializing and spinning up.  It will take a few minutes as the init container does a lot of installs.

![](/images/backstage-spinning-up.gif) <br><br>

Once everything is set, you can go back to 'backstage', and click the 'create' button.

![](/images/click-the-create-button.gif) <br><br>

Log in through the Backstage Authentication Realm.

![](/images/backstage-authentication-realm.gif) <br><br>

Authorize Key Cloak

![](/images/authorize-key-cloak2.gif) <br><br>


Register the existing component.

![](/images/register-existing-component.gif) <br>
![](/images/register-existing-component2.gif) <br><br>

Go back to backstage-rhtap-values.yaml and look at 'Integrations'

![](/images/backstage-integrations.gif) <br><br>

Open the demo project (back in our AI Odyssey gitlab) and open the file 'template.yaml'

![](/images/select-template-yaml.gif) <br><br>

Copy the URL for this file, exactly as it appears.

![](/images/copy-url.gif) <br><br>

Go back to 'Register an existing component' and paste the url in the 'Select URL' text box.  Click the 'Analyze' button and the defaults should appear.

![](/images/paste-url.gif) <br>

<br>
<p align="center">
<a href="docs/06-using-golden-path.md">Prev</a>
