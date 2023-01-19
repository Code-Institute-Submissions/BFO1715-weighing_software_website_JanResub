# JWS Weighing Software

The JWS Weighing Software website is a site where visitors will learn about the versatility of our weighing software and uses in multiple industries and multiple pieces of equipment. It will provide the user with the suitability of our range of corresponding indicators or control systems that will best reflect their requirements. The website will also provide examples of how we intend to implement the desired solution, how we would support them post installation and testimonials from previous customers. Finally, it will allow the prospective client to fill their details into a form and submit for future contact.

<img src="assets/images/multi-device.png" alt="Multi Device" width="600" height="350">

<strong><u>STRATEGY</u></strong>

Focus - What’s worth doing?<br>
A site where a user can gain insight into what software can be available for their application and guide them into making the correct with JWS Software.<br><br>
Definition - What are we creating?<br>
Creating an intuitive way that a client can easily navigate through different software options to narrow down on their specific industry and product requirements and provide their contact details for follow up.
<br><br>
Value - What value does it provide?<br>
It provides the prospective client with information on the capabiltity and broad scope of our sotware and encourages them to engage with the company.


<strong><u>SCOPE</u></strong>

What features will be available?<br>
A Nav bar to easily move around website. Information on the capability of JWS in different industries and product ranges. A list of different software possibilities for the client to choose from based on their industry and product. Contact us form to fill in requesting further information and a clickable image linking to further JWS media.<br><br>
What content will there be?<br>
On the homepage there will be a detailed description of the industries and products we cover.
The software page will list the different options available to clients dependent on what industry they are in and what equipment they have. The software page will provide information on how we intend to implement the solution and support them post installation. The contact page will allow the user to provide their detail and also provide our own. 


<strong><u>STRUCTURE</u></strong>

How is the user interaction designed?<br>
At the top of the terminal will be the title of the application Weighing Data System. The user will then be asked to input the 5 inweights which will give an error if the values entered aren’t integers, over required weight or in the correct format. The user will then be notified if the inweight data has been successfully uploaded to google sheets. Next, the user will be asked to input 5 outweights which will also give an error if the values entered aren’t integers, over required weight or in the correct format. The user will then be notified if the outweight data has been successfully uploaded to google sheets. The app will then calculate netweight from outweights minus inweights and notify the user when the netweight data has been successfully uploaded to google sheets. The app will then calculate total load by adding the 5 netweights then printing each of the outweights, inweights, netweights and finally total load. 

<img src="assets/images/process_flowchart.png" alt="Process Flowchart" width="500" height="200"><br>

<strong><u>SKELETON</u></strong>

How will the interface be laid out?<br>
Command-line interface with step by step instructions for user to follow and notifications of outputs.<br>

<img src="assets/images/python_terminal_app.png" alt="Terminal Screenshot" width="400" height="225"><br>

<strong><u>SURFACE</u></strong>

What will the visual design look like?<br>
Heroku app with step by step instructions for user to follow and notifications of outputs.<br>

<img src="assets/images/app_demo.png" alt="App Demo" width="400" height="225"><br>

<strong><u>FUTURE RELEASES</u></strong>

What features would you like to have in the future?<br>
Allow the user to select how many vehicles they will have coming to and leaving site for the given period and select the minimum weight for the vehicle.

<strong><u>TECHNOLOGY</u></strong>

What technology was used?<br>
<ul>
<li>Gitpod - writing code on workspace.</li>
<li>Github - hosting repository.</li>
<li>Python - programming language used to write code.</li>
<li>Google API - interface used to allow integration between google sheets and program.</li>
<li>Heroku - platform used to deploy the app.</li>
</ul>

<strong><u>TESTING</u></strong>

How was the app tested and are there any bugs that have not been addressed?<br>
Tested code PEP8 on https://www.pythonchecker.com/ with no major errors and a 96% mark. 6 minor issues are no whitespaces around operators. Also tested code by running pylint run.py on the terminal with the following results:

<img src="assets/images/pylint_test.png" alt="Pylint Test" width="1000" height="225"><br>

Reviewed app on Heroku dashboard and zero errors found as per below:

<img src="assets/images/heroku_test.png" alt="Heroku Testing" width="400" height="225">

Tested app is working correctly by following the step by step instructions in order to spot errors or inconsistencies - none found as per below:

<img src="assets/images/app_first_test.png" alt="App First Test" width="400" height="225"><img src="assets/images/app_second_test.png" alt="App Second Test" width="400" height="225"><img src="assets/images/app_final_test.png" alt="App Final Test" width="400" height="225"><br>
<img src="assets/images/sheets_first_test.png" alt="Sheets First Test" width="400" height="225"><img src="assets/images/sheets_second_test.png" alt="Sheets Second Test" width="400" height="225"><img src="assets/images/sheets_final_test.png" alt="Sheets Final Test" width="400" height="225">

Tested possible common errors such as inputting a string instead of integer, not inputting 5 values and inputting values less than 7,500kg:

<img src="assets/images/app_str_error.png" alt="String Error Testing" width="400" height="225"><img src="assets/images/app_count_error.png" alt="Count Error Testing" width="400" height="225"><img src="assets/images/app_value_error.png" alt="Value Error Testing" width="400" height="225">


Bug was found upon opening workspace on different device after a previously successful test, commit and push.  Error messages - Unable to import gspread and Unable to import google.oauth2.service_account.<br>

<img src="assets/images/gspread_bug.png" alt="Gspread Bug" width="400" height="225"><img src="assets/images/google_oauth2_bug.png" alt="Google Auth Bug" width="400" height="225"><br>

Investigated on stack overflow and ran:
<ul>
<li>pip install --upgrade google-auth google-auth-httplib2 google-api-python-client</li>
<li>pip install gspread</li>
<li>uploaded creds.json </li>
</ul>

Program tested fine afterwards though this bug kept happening upon opening workspace on different devices . 

<img src="assets/images/bugs_fixed.png" alt="Bugs Fixed" width="400" height="225"><img src="assets/images/bug_fixed_testing.png" alt="Bug Fixed Testing" width="400" height="225"><br>

Program still requires the pip install gspread and creds.json upload upon opening workspace on new device.

<strong><u>DEPLOYMENT</u></strong>

How was the project deployed?<br>
The project was deployed using Github, Gitpod and Heroku. The steps to deploy are as follows:<br>
<ul>
<li>Open Gitpod via Github repository</li>
<li>Run python3 run.py to test program</li>
<li>Link Heroku to Githib and create new app</li>
<li>Add creds.json config</li>
<li>Add python buildpack</li>
<li>Add node.js buildpack</li>
<li>Link Heroku app to repository</li>
<li>Select Deploy</li>
</ul>

The live link can be found here https://weighing-data.herokuapp.com/

<strong><u>CREDITS</u></strong>

Code Institute - https://codeinstitute.net/<br>
Stack Overflow - https://stackoverflow.com/

 

