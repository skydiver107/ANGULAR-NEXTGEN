# Perfectice Web
## RULES
1. Do not commit code to master branch.
2. Do not commit constant.js file.
3. Follow code format setting and coding conventions.
4. Use a new branch to develop a new feature.
## Main Git branches:
- `master`: latest production code.
- `AWS_PROD/AWS_CODEMODE`: deployed code in production server.
- `develop`: active develop code.
- `hotfixes`: production hot fixes. Code in this branch will be merged to develop for testing first then merge to production branch for deployment.

## Setup local develop environment
1. Install nodejs@18:  
https://nodejs.org/en/download/
2. Install angular:  
`npm install -g angular-cli`
3. Checkout dev branch:  
`git checkout develop`
4. Install packages:  
`npm install`
5. Tell git to not track `src/constant.js` file:  
`git update-index --skip-worktree ./src/constant.js`
6. Open file `src/constant.js`, change apiKey and baseUrl to your api server.

## Start local server
Run `ng serve` or `npm run start-large` to start dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Build
Run `npm run build local` to build the project in local. The build artifacts will be stored in the `dist/` directory.

## QA Deploy
1. Remote to QA server.
2. Execute command:  
`pf-deploy-ngweb`  
*this command will deploy both api and web
3. Check deployment progress:  
`tail ngdeploy.out -n 100`