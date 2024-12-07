## Using the Golden Path Template

From Developer Hub, select the 'ai-app' application that we created previously in section 04 - deploy-golden-path.

![](/images/select-ai-api.gif)<BR><br>

In the 'Links' section, choose 'OpenShift Dev Spaces'.<br>

![](/images/ai-api-contents.gif)<BR><BR>

You may need to log back into OpenShift. <br>

![](/images/ai-api-login-ocp.gif)<BR>

![](/images/ai-api-login-ocp2.gif)<BR><br>

You will be asked if you trust the authors of this repository.  Select 'Continue'<br>

![](/images/trust-authors.gif)<BR><BR>

Dev Spaces will request access to your account on Gitlab community.  Select 'Authorize Devspaces' to continue.<br>

![](/images/devspaces-request-access.gif)<BR>

YOu will be asked if you trust the authors, select 'Yes, I trust the authors'. <br>

![](/images/trust-authors2.gif)<BR><br>

The 'Dev Spaces' dashboard will appear. <br>

![](/images/devspaces-workspace.gif)<BR><br>

Excluding the 'base-image', the content in the devspaces 'workspace/ai-app/common' should match the content in the /ai-odyssey-2025/na-hobbyists/cv-demo repository location.<br>

Note:  the 'base-image' folder is necessary for the builds.

![](/images/content-match.gif)<BR><br>


Let's discuss the environments available.  We have 4 different environments:
1. Dev
1. Test
1. Beta
1. Prod
<br>

If you look at 'Tags' in this repository, you will have Dev, Test, Beta and Prod.  <br>

![](/images/look-at-tags.gif)<BR><br>

If you follow through with one of the tags (e.g. prod) and follow the commit it references, <br>

![](/images/commit-tag-references.gif)<BR>
![](/images/prod-tag-referenced.gif)<BR><br>

then these are the files it uses (in Repository) directory. <br>

![](/images/prod-repository-files.gif)<BR><br>

You do not have to worry about cv-demo-gitops as there are no changes there. <br>

![](/images/cv-demo-gitops.gif)<BR><br>

Let's now go to OpenShift to look at the builds.<br>

![](/images/build-configs.gif)<BR><br>

If you 'Start Build', that will build and publish out the images for training and evaluation.  

![](/images/build-out-images.gif)<BR><br>

Note: Training and evaluation both use the Training-base image. <br>


While that is running, you can oc apply service account permissions rolebinding_build.yaml. It will allow the demo pipelines to pull those images across the namespaces. 

![](/images/role-binding-build.gif)<BR><br>


Everything else gets copied into the templated project that was created by the Golden Path. <br>

![](/images/pulled-by-golden-path.gif)<BR><br>


To actually run the Demo UI there is one more respository that we have to work with and that is 'trafficui'. <br>

![](/images/traffice-ui-repo.gif)<BR><br>

In order to deploy the UI, run the following commands highlighted in traffic-ui. <br>

![](/images/deploy-to-ocp.gif)<BR><br>

Now when you check everything in, it will automatically kick off the build. 

From the OpenShift console, choose Pipelines->Pipeline details. 

![](/images/pipeline-build.gif)<BR><br>

You have a pipeline run and eventually everything will be all green when it finishes progressing.

Select the 'build name'.  This build is triggered off of running the commit in git.

![](/images/pipeline-run-details.gif)<BR><br>

There are 2 other pipelines in here.  You will need to run the train-and-evaluate step. Choose 'Start' to start building the pipeline. <br>

![](/images/train-and-evaluate.gif)<BR><br>

This will take care of pulling in the model, shutting it off in MLFlow and tagging it so that it can be run. <br>

Once that is in place the health on everything should start to self resolve because there are health checks on the existence of the model. <br>















<br>
<p align="center">
<a href="docs/05-install-mlflow-plugin.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/07-appendix-setup-pers-access-token.md">Next</a>
</p>