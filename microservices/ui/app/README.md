# HPDF Team Task
## Webapp of T49 (ReactJS)

**This webapp lets you enter addresses of a source and a destination, and shows the following-**

1) Distance between the two.
2) Time taken to travel from the source to the destination.
3) A Google Maps link to show the directions.
   If only the coordinates are known, then convert the coordinates to its address first using the coordinates-to-address calculator available on the same webapp.

**To get this app to run, perform the following steps-**

>These are the steps to be followed to view the webapp version of this repository.

1) Go to https://hasura.io/ and create an account there. 
2) Download the hasura cli from https://docs.hasura.io/0.15/manual/install-hasura-cli.html .
3) Now go to git bash and type the command 
`hasura login`.
4) Next type the command `hasura quickstart hasura\hello-react`.
 The hasura quickstart command clones the project repository to your local computer, and also creates a free Hasura cluster, where the project will be hosted for free. A git remote (called hasura) is created and initialized with your project directory.
5) Now type the command `hasura cluster status`to get your cluster name. Make sure that you are in the hello-react folder by using the `cd hello-react` command.
6) Now modify the package.json file inside *microservices/ui/app/package.json*. Assign your cluster name to REACT_APP_CLUSTER_NAME environment variable.
7) Now replace the contents of your hello-react's *microservice/ui/app/src* folder with the contents of this repository's *microservices/ui/app/src* folder. Also replace the index.html file in *microservice/ui/app/public* with this repository's index.html file available in the same location.
8) Now we will push the contents of your hello-react folder to your cluster. To do this, type the command `git add . && git commit -m "First commit"` and then type `git push hasura master`.
9) Now run the command `hasura microservice open ui` to view this react app. 
