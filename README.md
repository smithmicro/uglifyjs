# uglifyjs
Docker image for uglifyjs based on Alpine

## Examples
Run the following Docker run commands to use this image:

This prints out the help screen:
```
docker run smithmicro/uglifyjs
```

This uglifies a single JavaScript file to STDOUT:
```
docker run -v $PWD:/file smithmicro/uglifyjs /file/test.js
```

This uglifies a JavaScript file to a .min.js file:
```
docker run -v $PWD:/file smithmicro/uglifyjs /file/test.js > test.min.js
```
This is equvalent to:
```
docker run -v $PWD:/file smithmicro/uglifyjs /file/test.js -o /file/test.min.js
```
