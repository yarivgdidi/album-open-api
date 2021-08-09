##### Note: make sure node lts is installed (currently 14.17.4)

This assignment was done using open-api (swagger)

1. A YAML file representing the API CRUD operations and DTO - Data Transfer Object model.
```https://github.com/yarivgdidi/album-open-api```  
The command line to generate both Server template and client Axios API  is available in this repository README.md


2. A node js server was generated, then the crud logic was implemented in the services
```https://github.com/yarivgdidi/album-api-server```  
*NOTE* - there are typescript node JS generators, but these are at early stages, so the project is not in Typescript yet.


3. A react app was created using npx create-react-app album-app --template redux-typescript
An Axios API client was then generated based on the same YAML used for the server.
```https://github.com/yarivgdidi/album-react-app```


4. the project was deployed to Heroku using GitHub connection  
```http://album-api-server.herokuapp.com/api-docs/```   
```https://album-react-app.herokuapp.com```

5. To run locally, clone the album-api-server and album-react-app and type in each of them:  
```
npm i
npm run local
```



### for full petstore implementation (example)
```
npx @openapitools/openapi-generator-cli generate -i petstore.yaml -g nodejs-express-server -o  ../petstore-server
```


### generate album-api-server
```
npx @openapitools/openapi-generator-cli generate -i album.yaml -g nodejs-express-server -o  ../album-api-server
```

then:
- cd ../album-api-server
- npm i
- npm start
- start server implementation

go to http://localhost:3000/api-docs for openapi (swagger) docs

### generate album-api-client
```
npx @openapitools/openapi-generator-cli generate -i album.yaml -g typescript-axios -o ../album-app/src/openApiClient --skip-validate-spec --additional-properties packageName=AlbumClient
```

