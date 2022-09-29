# LocalScriptureRenderingPipeline
Run the scripture rendering pipeline locally

# Prerequisits

- Docker and Docker Compose
- Azure Storage Explorer https://azure.microsoft.com/en-us/products/storage/storage-explorer/
- A copy of the live reader templates, styles, and scripts from https://github.com/WycliffeAssociates/read.bibletranslationtools.org
- Some sort of REST client that can issue a POST requst

# Running
- Run `docker compose up`
- Open the Azure storage explorer and connect to the local emulator
- Create the template and web blob containers
- Copy the css, js, and font folders as well as the index.html if desired from the output of the live reader build into the web container you created
- copy all of the templates out of the templates folder into the template blob container
- The website will be running on port 80 and the webhook will be running on port 8080
- To render a project send a simulated webhook POST to http://localhost:8080/webhook
- A page will be generated at http://localhost/u/(RepoUser)/(RepoName)

You can look at a repos's previous requests to find a request to send to the api

