## Using the Golden Path Template

There are 4 steps we will use to test and update our model:

1. Test the baseline model
1. Update the model without guardrails
1. Update the model with smoke tests
1. Update the model with approval gates
<BR><BR>

## 1 - Test the baseline model
1. Go to the “Hatter Maps” backend UI and view the live traffic feed
1. To test the model, submit a low traffic image and a high traffic image 
1. We see that the model correctly categorizes both images, but it gives the low traffic image a score of “C” when we think it should score an “A”. <br><br>

![](/images/upload-image.gif) <br><br>

## 2 - Update the model without guardrails
1. One of the data scientists makes a change to the model and then pushes the change to production. Unfortunately, their math was wrong and the model is miscategorizing high traffic images as no traffic.


1. Go back to the “Hatter Maps” backend UI, submit the high traffic image again and see that it miscategorizes the image as an “A”.


1. Imagine the real world consequences to our customers (stuck in traffic, missed appointments, ambulances and first responders impacted) of this incorrect prediction. <BR><BR>

![](/images/congestion-grade-A.gif) <br><br>


## 3 - Update the model with smoke tests

1. Using our approach, we are able to wrap modern SDLC practices around the model development process without impeding the work of the data scientists.

1. First, to fix the model error, we go to source control to see the lines of the model that were modified and we reverse the change.

1. Next, we implement smoke tests to catch these mathematical errors and implement them in our CI/CD pipeline.

1. We attempt the same “bad” code push and see that the smoke test fails and the pipeline job errors out. <BR><BR>

![](/images/model-with-smoke-tests.gif) <br><br>



## 4 - Update the model with approval gates

1. Next, we make a new code change because we still want to improve the accuracy of the low traffic image prediction.


1. We make the change and submit our merge request - an approval gate is needed to merge the code change. Only after the change is reviewed and approved does the CI/CD pipeline kick off to deploy the new model.


1. Go back to the “Hatter Maps” backend UI and submit the low traffic image. Now it correctly categorizes it as an “A” (no traffic delays) and we have successfully improved the accuracy of our model on a platform with modern SDLC controls. <BR><BR>

![](/images/model-with-approval-gates.gif)

<br>
<p align="center">
<a href="docs/05-install-mlflow-plugin.md">Prev</a>
</p>