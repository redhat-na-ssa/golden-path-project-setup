## Install the MLFlow Plugin

Your plugin has been added to the example app in this repository, meaning you'll be able to access it by running yarn start in the root directory, and then navigating to /mlflow-frontend-dynamic. 

You can also serve the plugin in isolation by running yarn start in the plugin directory. This method of serving the plugin provides quicker iteration speed and a faster startup and hot reloads.
It is only meant for local development, and the setup for it can be found inside the /dev directory.

To install the mlflow plugin, you need to identify the project janus-idp-gitops in gitlab.

From the Trusted Application Pipeline, Log into GitLab.

![](/images/log-into-gitlab2.gif) <br><br>

From the 'Projects' page change into the 'gitops/janus-idp-gitops' directory.

![](/images/gitlab-projects-page.gif) <br><br>

Under janus-idp-gitops/charts/backstage/templates directory, replace dynamic-plugins-npmrc.yaml 

![](/images/replace1.gif) <br><br>

with rhdh-mlflow-plugin-frontend/TAPDemoChanges/ dynamic-plugins-npmrc.yaml. 

Note:  that the TAPDemoChanges directory is in a different gitlab location:  https://gitlab.consulting.redhat.com/ai-odyssey-2025/na-hobbyists

![](/images/replace2.gif) <br><br>

The easiest way to replace the file, is to download the rhdh-mlflow-plugin-frontend/TAPDemoChanges/ dynamic-plugins-npmrc.yaml file onto your PC.

Then open the janus-idp-gitops/charts/backstage/templates/dynamic-plugins-npmrc.yaml file and select the 'Replace' button.

![](/images/replace3.gif) <br><br>

When the 'Replace dynamic-plugins-npmrc.yaml' file appears, select the 'upload' hyperlink.

![](/images/upload-file.gif) <br><br>

The File Manager will appear for your PC, select the dynamic-plugins-npmrc.yaml file that you downloaded earlier to your PC.

![](/images/select-file.gif) <br><br>

Once the file has been uploaded, select the 'Replace File' button.

![](/images/replace-file2.gif) <br><br>

Your file will be replaced.  Notice that the namespace 'backstage' has been added, and the data '.npmrc' content has changed.

![](/images/file-changes.gif) <br><br>

<BR><BR><BR>
Next, we will use the Golden Path Template.  

<p align="center">
<a href="docs/04-deploy-golden-path.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/06-using-golden-path.md">Next</a>
</p>