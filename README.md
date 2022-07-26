1. This is the Parent repo which has its own github actions pipeline yaml with couple of steps to be executed in build
2. First step simply checksout the repo
3. Second step uses github POST request api to call another repository "child" github workflow yaml
4. The curl command expects a PAT token to be passed which you can create it using the steps detailed in https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
5. Construct API endpoint using syntax https://api.github.com/repos/<organizationName>/<repoName>/dispatches
6. Pipeline execution looks like below
    image.png