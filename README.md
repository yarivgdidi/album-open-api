##### Note: make sure node lts is installed (currently 14.17.4)

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


