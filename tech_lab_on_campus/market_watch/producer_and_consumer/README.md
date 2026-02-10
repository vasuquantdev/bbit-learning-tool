# Problem Definition: ✨Producer And Consumer✨

##  Instructions

In this section, you will collaborate with a partner to instantiate the producer and consumer classes. This is a paired programming exercise where you will work together using Git and GitHub for code sharing.

### Partner Workflow

**Setup (Do this together):**
1. **Decide who will be the fork owner** - This person will create the fork of the lab repository
2. **Fork owner**: Fork the repository to your GitHub account
    - Look for a "Fork" button in the top right corner of the main repo screen
    - After forking, it should take you to your fork of the repo. The repo name will be `<your_github_username>/bbit-learning-labs`
3. **Fork owner**: Add your partner as a collaborator:
   - Go to your fork's Settings → Collaborators → Add people
   - Enter your partner's GitHub username and send the invitation
4. **Partner**: Accept the collaboration invitation (check your email or GitHub notifications)
5. **Both students**: 
    - Codespaces: Create a codespace from the same forked repo
    - Local: Clone the same fork to your local machine using `git clone`
6. **Both students**: Ensure you can bring up the lab successfully

**Division of Work:**
- **Partner A**: Complete the `producer section` in the producer folder
- **Partner B**: Complete the `consumer section` in the consumer folder

**Sharing Code (Do this after completing your section):**
1. **Both students**: After completing your assigned section, commit your changes:
   - `git add .`
   - `git commit -m "Implement [producer/consumer] section"`
2. **Partner A**: Push your producer code first: `git push`
3. **Partner B**: Pull Partner A's changes, then push your consumer code:
   - `git pull` (to get the producer code)
   - `git push` (to share your consumer code)
4. **Partner A**: Pull Partner B's consumer code: `git pull`
5. **Both students**: Verify you both have the complete solution (producer + consumer)

**Important Notes:**
- Communicate frequently with your partner about your progress
- If you encounter merge conflicts, work together to resolve them
- Use the [git_commands.md](../resources/git_commands.md) file for Git command reference

**Testing Together:**
- Once both partners have pulled all changes, follow the `testing instructions below` to send and receive messages
- Both partners should be able to run the complete solution on their machines

   
`IMPORTANT!!!` Please utilize the [Functions.md](../Resources/Functions.md) file as it contains almost all the functions you will need for this lab. Also, other helpful information can be found under the Resources folder for Python, Git, and RabbitMQ details.

## Testing
In order to verify that the consumer and producer class was properly instantiated, we will use the provided  `consume.py`, and `publish.py` file from producer and consumer folder. Follow the below instructions:
1. In the terminal window, run the `consume.py` file from the consumer sectio using the python interpreter.
2. In another terminal window, run the `publish.py` file from the producer section using the python interpreter. This will publish a message using RabbitMQ. 
3. Return to the first terminal window with the consumer running. "Success! Producer And Consumer Section Complete." should now be displayed on your terminal if you instantiated & implemented the consumer class correctly.
* Note that if you are developing from the terminal in your IDE, inside the second terminal window you will need to step into the rmq_lab Docker container in order to access the python enviroment. We do this by first running the `docker exec -it [containterName\containerID] /bin/bash` command. Using the `docker ps -a` command will show all the running docker containers and their associated I.D and names. Your command could be `docker exec -it tech-lab-on-campus-rmq_lab-1 /bin/bash` or `docker exec -it 8a785d10fd7e /bin/bash`

