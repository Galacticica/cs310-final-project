# CS310 Final Project Report
By Reagan Zierke
## What was the purpose of this project in your own words?
The purpose of this project was for us to understand how to write a declarative configuration for a simple application.

## Describe each task. What did that task accomplish, how did you accomplish it. Use complete sentences.
### Bagisto / Grafana Playbook
These playbooks were able to pull down the correct image from docker and then restart docker with said image. We accomplished it by looking at the ansible documentation with the docker community package. To figure out the name of the image to pull, we went to dockerhub and found the manual command and used that name.

### Users Playbook
This playbook created the developer group and admin group and created users that were added to said groups. We accomplished this by looking at the ansible.builtin commands and found both the user and group options which we used. To give the admin group sudo access, we did some research and settled on using the copy command to create a sudoers configuration file that grants all members of the admin group sudo access.

## Explain 3 hurdles/misconceptions you encountered whilst working on the project. How did you overcome these hurdles?
### Hurdle 1
Our first hurdle was installing bagisto without declarative configuration. We were confused and thought we had to install the image manually and use the docker-compose file to write the configuration. We overcame this by restarting after being told we were wrong.

### Hurdle 2
Our second hurdle was not thinking to look for the documentation right away. Once we realized the documentation had all the answers we needed 🤦‍♂️, it was pretty smooth sailing from there.

### Hurdle 3
While not ultimately a big hurdle, I would say some things with Git were slightly annoying to work with. It worked fine on my computer and the server, but Heidi's kept making her reauthenticate any time she tried to push changes which was difficult to deal with.

## Explain 2 things you would do differently if you had to re-do this project?
1. I would make sure we are doing the correct thing from the get go so that we don't waste 3 hours doing it the wrong way again. (Though now we are "experts" with troubleshooting docker and removing/pruning orphans)
2. I think I would've done a better job at looking through the documentation for what we need. It would've been so much easier if we had just looked for it in the ansible docs or googled it from the get go.
   
## What is something that could be improved in this project?
I think the biggest improvement would maybe be going over how to use docker with ansible in class or providing the link to those docs because some of us may not immediately think of that, especially because it is at the end of the semester and our brains are fried from other classes.