## Github Action Workflow(Here both CI-CD pipeline)
- Flask App (Also applying/creating unit test cases)----> Build Test -----> Deploy -----> Docker Hub
- Here firstly we are building flask app and then the follow up. Once i push the code into the main branch my unit test cases should run and it should also build. After creating the flask app we build the entire artifact and do the unit testing as we go ahead.
- In github action workflow our first step is Build and Test here we are basically going to implement our continious integration. After we do build an test , in this build and test we will also create our docker image(docker image will be created for this entire application).
- Entire docker image will be created in a container , specifically considering linux(it depends on what kind of os u want to use as a container for building this entire docker image).
- Once we create , validate this docker image --> once everything is working fine ---> next we deploy(here our continious deployment will work).
- Where we need to deploy this ??
- This docker image will specifically be deployed in docker hub. Docker hub is the public repository for the docker image. Once we deploy in this docker hub then anybody can pull this particular docker image and can probably execute in the local machine(if they have docker installed).
- Whenever we are doing deployment we need to create some secret keys : 1. Docker Username 2. Docker Password(we will ty to generate a token from the docker hub itself).
- We automate this entire developer workflow(which includes CI and CD both).
- Tools we are using here:
- git , github , dockers , pytest(for unit testing) , flask(to develop our application).

## Note:
- If we really need to identify all the unit tes cases we need to probably create ur file name beginning with test(for pytest to identify it).
- Any file or any folder u probably begin with test it is automatically going to consider that as a unit testing files.
- We name the file : test_app.py ----> here we will create our unit testing things.
- All code related to unit testing will be developed over here.

## Setting Up Github Repo
- Go to github and create ur repo.
- In ur current directory create README.md file.

## Follow up with commands:
- git init
- git add README.md  ---> its already added manually.
- After this use command : git add . ----> It will get all the files in the current directory.
- git commit -m "first commit"    ----> all the files will be commited to the remote repository
- git branch -M main
- git remote add origin https://github.com/Amritanshu160/GITHUB-ACTION-WORKFLOW.git  ---> configure our remote repository to this particular origin.
- git push -u origin main
