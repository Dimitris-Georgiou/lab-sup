# Technical Support Engineer Assesment
## Steps to Submit
1. Create an ssh key on your machine if you do not have one
1. Send us your ssh public key
1. Create a GitHub Account
1. Git Clone this repository to your local machine
1. Remove the current origin remote (git remote remove origin)
1. Create a new repository under your GitHub account (do NOT fork this repository)
1. Follow the instructions to push an existing repository from the command line...
1. Add answers to this Document (either to this document or create different for each question), commit your answers to the branch
1. Push your answers to your personal remote origin in your git account
1. Send a notification to us with a link to your repository
If any of the steps above is unclear, please try GitHub user guides.
The method of submission is part of the test (usage of Git)

## Questions
1. A customer has reached out to us that he cannot access our platform running on 45.33.22.50. Customer's complain is as follows:
- "Hello, It seems i cannot access http://45.33.22.50/test1"

2. A customer has reached out to us that he cannot access our platform running on 45.33.22.50. Customer's complain is as follows:
- "Hello, It seems i cannot access http://45.33.22.50:444/test2. When i access it seems that nothing happens"

## To Do
- For both above questions what are the actions you will take to evaluate customers request.
- Include questions we may need to ask to get additional information to ensure the best customer support.
- Add an explanation why you ask each question (what do you expect to receive back.
- Additionaly you need to ssh to the machine and troubleshoot the above scenarios
- Make sure you list in detail what are the steps you followed to identify and resolve the problem.

Hint: The platform runs on nginx and python

## Answers

'''I send my ssh key, I tried to ssh to the server but at the moment I do not have permission to connect. So the below answers are imaginary scenarios'''

Question 1:
1. First I will inform him that we are checking his request.
2. I will try to access the platform myself to check if everything its okay.
3. If I can access the platform, I will ask customer the following questions:
	a. To confirm that he has internet connection and from what device he is trying to access.
	b. If he has access to the internet I will ask which broswer is he using and what version, and to try to connect with a different browser.  
	c. If the issue persists  I will ask him to check if he has any  firewall that might blocking the connection.
	d. If he checks and confirm that it is not a firewall issue, I will escalate the issue, and I will inform him as soon as I have a response.
4. If i do not have access to the platform, I will check if the server is up
5. If the server is up i will connect and check if the service is running.
6. If the service is running i will escalate the issue. If the service is not running, I will start the service and check if I can access the platform.
7. If everything is okay from my side. I will ask customer to confirm that he can connect to the platform.

Question 2:
1. First I will inform him that we are checking his request.
2. I will try to access the platform myself to check if everything its okay. 
3. If I can access the platform, I will ask customer the following questions:
        a. To confirm that he has internet connection and from what device he is trying to access.
        b. If he has access to the internet I will ask which broswer is he using and what version, and to try to connect with a different browser.
        c. If the issue persists  I will ask him to check if he has any  firewall that might blocking the connection.
        d. If he checks and confirm that it is not a firewall issue, I will escalate the issue, and I will inform him as soon as I have a response.
4. If I cannot reach the platform, I will first check if the port 444 on the server is open.
5. If the port is closed I will open the port and I will try to connect - If its okay i will ask him to check again now.
6. 4. If i do not have access to the platform, I will check if the server is up
7. In case that the port is open and the service is running and I still can not access the platform I will escalate the issue, and I will inform customer about it. I will also inform him that as soon as I have a response I will get back to him.


PS: If i get access to the server i will change my answers before the deadline tomorrow

