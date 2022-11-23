Robert Hassenmayer 

11/23/2022

# email sender app

I have accomplished most of my planning already and setup a default django project called email_sender_proj and django app called email_sender, I will complete this project in a Test Driven Development manner.

From this point lets get started looking at my planned flowchart and writing our first tests.

##  flowchart 1 steps

 > 1. The first part of flowchart is a unidirectional flowchart(flowchart without a loop), we will recieve a post request with form data and the URLconf will pass the request to a subscribe view, next we will get the subscribed check marks data and test if the value is true or false

### with step 1 I should write tests for:

- recieving the post request.
- checking that the view is getting the subscribe check mark data and user from the form.
- check that the view is sending a HttpResponseRedirect

 > 2. If the subscribed checkmark in request.POST returns true, then we add a subscribed field to the django auth user data model

### with step 2 I should write tests for:

- assure view is adding subscribed field to user, add and callback data in tests

## flowchart 2 steps

This flowchart breaks down how we will actually send those emails to subcribed users. , the most recently published email will be grabbed by the view then edited per subscribed user and 

 > 1. Create an email template model for the admin to add email templates too

### with step 1 I should write tests for:

- adding a template to database
- editing a template
- getting template data
- deleting a template

 > 2. Next we need to get our most recent template from the template model and save it to a  constant variable

### with step 2 I should write tests for:

- getting template data
- get list of all subcribed users and their emails

 > 3. finally create a loop that takes the template variable and creates a new temp variable,  swaps user names into temp variable replacing [name] in template add email and template to dict as email:key template:value then send to that users email.

### with step 3 I should write tests for:

- test that names are being swapped properly into temp template varible
- assure make sure the new template with user name is being send to correct user email. 