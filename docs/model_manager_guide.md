# OE Model Manager

It is a plugin for oe-studio that helps to manage all model related operations.
Here is the ***Landing Page***

![Model Management](/images/landing_page.png)

## ***Model Creation***
To create a model, please click on the button present at the bottom right of the screen.
It opens a list of options.Click on the first option from bottom of the list(which is create model), marked in the below image.

![Model Management](/images/Create_model.png)

The model creation page contains five tabs.
* Model Information

It is the starting page/tab that opens when model creation button is clicked.Enter model's name, base model from which the model will be derived, plural for the model, etc.

![Model Management](/images/model_information_page.png)

Fill in some data as below.

![Model Management](/images/model_information_with_data.png)

Once the required data is filled in this tab, click on next button to goto the next tab(the properties tab).

* Properties

Properties tab has the below landing page.
![Model Management](/images/model_properties_page.png)

Click on `Add Property` to add properties to the model.
Let us add two properties accountType and accountBalance.

![Model Management](/images/properties_inline_validation_page.png)

To add validations to any property click on `View Validation` button(hover on the property to see this button).
In above created properties, add `Min.` validation on accountBalance.

![Model Management](/images/properties_inline_validation_edit_page.png)

After adding properties and property level validations click on `NEXT` button to go to the next tab(Validations tab)

* Validations

This tab helps to add `oe-validations` to a model.

Let us add an `oe-validation` of type `custom` with the name transactionCheck and add ValidateWhen(if required) as well as Validation Expression.

![Model Management](/images/oe-validations_add_page.png)

Click on `NEXT` to go to Relations tab.

* Relations

We can add loopback relations to the model in this tab.
Click on `Add Relation` button to add a relation.

![Model Management](/images/relations_page.png)

We have already created a model named `Bank`, so let's create a relation from our current model(Account) to the existing Bank model.
![Model Management](/images/relations_add_page.png)

Click on `NEXT` to go to ACLs tab.

* ACL

Access Control Lists for the model can be defined here.

![Model Management](/images/acl_page.png)

Add ACLs to the model by clicking `Add ACL` button and define the ACLs.

![Model Management](/images/acl_add_page.png)

### Upload Model Schema

Models can be created by uploading a schema file from oe-model-manager.
Click on the highlighted button on the below image.
![Model Management](/images/create_model_upload_models_page.png)

Click on the `Browse` button to select a json file containing the model schema.
![Model Management](/images/model_creation_upload_file.png)

## ***Adding Relations***
Apart from adding relations while creating the model as explained in above section, relations cann be added by selecting the highlited button in the below image.

![Model Management](/images/create_relations_option_page.png)

Click on the models which you want to relate, so that they will be present in the model viewer.
As we have clicked on the `model relations` button highlited in above image, the models in the model viewer will have arrows enabled on them.Those arrows connect the model and define relations.(Blue to Orange arrow).
In the below image we opened Account and Bank models which already have a `belongsTo` relation defined(can be seen in the image).

![Model Management](/images/model_relation_arrows_page.png)

Lets add one more relation to those models.Click on the blue arrow of Bank model and join it to orange arrow of Account model.This will open a dialog box to define the relation.
Click on `Create` button to create the relation.

![Model Management](/images/model_relations_define_page.png)

## ***Model Views***

On the left side panel click on the search icon to search for any model.Once you hover on the model three buttons will appear on the right hand side of the model.On click of thode buttons different views of the model can be opened.

* Open in New View

Click on the first option/button to open the model in a new tab/view.
![Model Management](/images/model_new_view_page.png)

* Data Manager View

Click on the second option/button to open the data manager view of the model.Explained in the next section (Data Management)

* Detailed View

Click on the third option/button to open the detailed view of the model.
![Model Management](/images/model_detailed_page.png)

## ***Data Management***

Data management  view is used to POST some data in the model.
The below image shows the data manager view for Account model created above.
![Model Management](/images/data_manager_page.png)

Click on `+` button present in the top right hand side of the screen to add a record to the model.
Fill in the details/values for the properties and click on save to make an entry in the model's record.

![Model Management](/images/data_manager_post_data_page.png)

After the data is saved the data manager view will show the existing records of the model.

![Model Management](/images/data_manager_data_saved_page.png)

## ***Model Options***
The model view contains certain options.Once you hover over the model, a button with three dots(ellipses) will appear on top right corner.This button will open a list of options(operations).

![Model Management](/images/model_new_view_options_page.png)

The below image shows all the available options.
![Model Management](/images/model_new_view_options_list_page.png)

* Attach Workflow

Workflow can be attached to a model using this option.
Select the `OE Workflow` checkbox and then click on the `+` button to add an existing workflow to the model.

![Model Management](/images/attach_workflow_page.png)

* Add Personalization Rule

Service personalization rules can be attached to a model using this option.
Fill in the required fields like rule name, contributor and a value for it(press enter after filling up the value), then click on `Add Scope` to add the scope.
In the below example `device` is used as contributor with value mobile.

![Model Management](/images/personalization_rule_add_page.png)

Press on `NEXT` button to goto the next screen where we will define the rules.

All the service personalisation rules can be defined in this page.
Lets create a `Field Replace` rule for the `Account` model created above. Press on save button to save the rules defined in here.

![Model Management](/images/personalization_rule_define_page.png)

* Add Model Rule

Model rule provides the capability to attach default and validation rules to a model.

![Model Management](/images/model_rule_attach_screen.png)

Drag and drop the rules from left hand side `RulesList` on to `Default Rules` or `Validation Rules` tab.
Click on `Save Rule` button to save those rules.
![Model Management](/images/model_rule_attach_default_rules_validation_rules_screen.png)

* Define ACL

ACLs can be defined using this option.
Static ACL are those ACLs that goes into the model's schema, we have defined static ACL while creating a model under the ACL tab above.
Dynamic ACL goes into ACL model instead of model schema.

Click on the `+` icon to add ACL.
![Model Management](/images/model_acl_definition_page.png)

Fill in the details like access type, property, etc. and scroll down to click on the `SAVE` button available at bottom left corner of the screen to save the defined ACL.
![Model Management](/images/model_static_acl_add_page.png)

* Define Data ACL

Similiar to ACLs defined in above section one can add data level ACLs on the model.

![Model Management](/images/data_acl_page.png)

Click on the `+` button to define a data ACL.
Fill in the required details and click on `SAVE` button present on bottom left corner of the screen to save the defined data ACL.

![Model Management](/images/data_acl_definition_page.png)

* Edit Model

Edit model will open the same screen as the create model screen section.

One can edit any properties, validations, relations, etc. and save the model schema again.
To download the model schema please click on the download button.
(This can be done while model creation as well.)

![Model Management](/images/model_schema_download.png)

* Clone Model

Clone model optiona opens up the same screen as model creation, which helps to create a clone of the existing model.

* Delete Model

To delete a model this option can be used.
Once this option is selected a dialog asking to delete the model will open, on selecting `OK` the model will be deleted.

![Model Management](/images/delete_model_page.png)