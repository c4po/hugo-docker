# hugo in Docker

fork from [git-sync demo](https://github.com/kubernetes/contrib/tree/master/git-sync/demo/hugo)

`hugo` is a container that convert markdown into html using [hugo static site generator](http://gohugo.io/).

## Usage

```
# build the container
docker build -t hugo .

# run the hugo container
docker run -d -e HUGO_BUILD_DRAFT=true -v /git-data:/src -v /html:/dest bonesoul/hugo

# start the nginx
docker run -d -p 8080:80 -v /html:/usr/share/nginx/html nginx 

```


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/contrib/git-sync/demo/hugo/README.md?pixel)]()
