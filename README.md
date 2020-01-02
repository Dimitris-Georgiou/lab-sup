# Technical Support Engineer Assesment
## Steps to SubmitTT  


1. Create an ssh   key on your machine if you do not have one
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



Question 1:
1. First, the customer will be informed that we are dealing with his request.
2. I will access the server to see if the service is running.
3. I will check which ports ar open using: netsat -tnlp
4. Only the ports 443 and 22 are open in public. Customer is trying to access the platform with port 80.
5. Then i will check at etc/nginx/sites-enabled , to check if the service is running. 
6. the service is running on 443: 
server {
  listen 443  default_server;
  location /test1 {
        proxy_pass http://localhost:5000/test1;
  }

  root /var/www/html;
}
7. I will make an http request using curl to 45.33.22.50:443/test1 to check if the service is running. The service is running.
8. Then I will inform customer that the service is running on the port 443, so he has to connect to http://45.33.22.50:443/test1
9. The final step is to ask customer to confirm that the platform is reachable, and state that we remain at his disposal for further assistance.


Question 2:
1. First, I will inform customer that we are checking his request.
2. I will access the server to see if the service is running.
3. I will check which ports ar open using: netsat -tnlp
4. Only the ports 443 and 22 are open in public. Customer is trying to access the platform with port 444.
5. Then i will check at etc/nginx/sites-enabled. The file is not located at sites-enabled, it is located at etc/nginx/sites-available. So the service is not configured in nginx.
6. the file on sites-available :
server {
  listen 444 default_server;
  location /test2 {
        proxy_pass http://localhost:5000/test2;
  }

  root /var/www/html;
}
7. I will curl 45.33.22.50:444/test2 but there is no access. On localhost:5000/test2 there is access because the service locally runs at 5000.
8. At this point I will inform customer that the issue has been detected and that I will escalate it to the administrators to fix the issue and I will get back as soon as possible.
9. Then I will inform admins to configure the service to nginx and enable the port 444.
10. As soon as I have a response that the issue has been resolved. I will curl to 45.33.22.50:444/test2 to confirm it.
11. Finally I will ask customer to recheck now and to confirm that the platform is accessible. 



