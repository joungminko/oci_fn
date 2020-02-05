## # OCI fn

### # Prerequisite
1. run docker deamon
2. install fn([instruction link](https://fnproject.io/tutorials/node/intro/)) as an environment
3. run fn(default port is 8080)
```
fn start
```
3.1. check the context(where the fn is going to run on)
```
fn list contexts
```
3.2. set the desire context
```
fn use context default
```
4. install fn([download_link](https://github.com/fnproject/cli/releases/)) as CLI binary file 
4.1. add to running PATH

### # example for node developer
1. create app by fn(it creates the sample of node.js app for fn)
```
fn create app nodeapp
```
2. deploy to docker(it deploys to the docker environment)
```
fn --verbose deploy -app nodeapp --local
```
2.1. check docker images to confirm fn app is properly added
```
docker images | grep nodeapp
```
2.2. also list by fn app criteria
```
fn list apps
```
2.3. list by fn functions 
