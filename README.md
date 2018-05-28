# uglifyjs
Docker image for uglifyjs based on Alpine

## Examples
Run the following Docker run commands to use this image:

This prints out the help screen:
```
docker run smithmicro/uglifyjs --help
```

This uglifies a single JavaScript file to STDOUT:
```
# using a volume
docker run -v $PWD:/file smithmicro/uglifyjs /file/test.js

# using STDIN
docker run -i smithmicro/uglifyjs < test.js
```

This uglifies a JavaScript file to a .min.js file:
```
# use a volume and STDOUT
docker run -v $PWD:/file smithmicro/uglifyjs /file/test.js > test.min.js

# use a volume and the output switch
docker run -v $PWD:/file smithmicro/uglifyjs /file/test.js -o /file/test.min.js

# use STDIN and STDOUT
docker run -i smithmicro/uglifyjs < test.js > test.min.js
```
